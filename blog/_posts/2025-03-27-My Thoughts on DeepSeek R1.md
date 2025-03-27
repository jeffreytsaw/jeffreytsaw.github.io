---
layout: post
title: DeepSeek R1 - What's the big deal? My very unqualified take
draft: false
---

So this is not going to be another one of the blog posts/articles walking you through DeepSeek R1, there are plenty of those out there. I did, however, want to share some of my thoughts on the hype/discussion around R1. I don't really know how to format this so I'm just going to pretend it's a fake interview where I'm the interviewer interviewing myself. Yea I know this is cringe, but whatever.

Discliamer: the opinions shared are my own and do not represent the opinions of my employer. I am also not an expert on LLMs, ML, or AI, so take everything I say at face value.

<br>

_Open AI already came out with o3-mini. Grok-3 is better than o1-preview too. R1 isn't close to SOTA anymore, so who cares?_

I see a lot of questions/comments like this, and I think they're missing the point. R1 was groundbreaking because of its simplicity. It showed that the fancy chain of thought reasoning that was so tightly guarded by companies like OpenAI could be ellicited in a simple RL setup.

I think what struck me was just how simple the setup was. A lot of literature I'd seen previously revolved aroudn process reward models and figuring out good ways to reward desired reasoning steps. This in itself is a really hard problem, and what was crazy about R1 was that they showed this was completely the wrong approach. I mean R1-zero was as simple as it gets, it was a simple training loop that takes outputs of the LLM and optimizes its weights using a pretty simple variation of PPO. No special sauce required.

What thsi told me was that anyone can create their own specialized reasoning model fairly easily. Take a powerful LLM, say llama-3 or Deepseek v3, a problem space where you have LLM inputs and a clear determining success or failure, and with enough compute, you could train a highly specialized state of the art reasoning model.

I know Deepseek R1 technically had a special SFT pre-training phase and a whole procedure to generate high quality reasoning data, but I think the more impressive result by far what they showed was possible with minimal effort.

<br>

_Wow, thay's amazing! Why hasn't this been done before? I mean, RL and LLMs have been around for a while, right?_

I don't really have a good answer for this one. On one hand, the idea of eliciting scaling test time compute and improving performance the more tokens an LLM generates is pretty new. I think that and the problem setup of LLM training and RL is different. When training LLMs it's setup like a supervised learning problem. You take an input, say part of a sentence, and predict a known output, the next word in the sentence. In RL, though, the setup usually involves an environment, and an agent. The agent observes the environment, takes an action, which in turn updates the environment. They seem like fundamentally different setups, and it's totally non obvious (at least to me) that an LLM can be trained successfully in this kind of RL setup. Yea I know RLHF is a thing, but that to me is more preference optimizations than actually eliciting novel behaviour out of the LLM.

I think the other reason I can think of is it seems crazy that this setup would work, so people hadn't ever really tried it. The rewards feel like they'd be so sparse, and there's no notion of environment, so there's not really an obvious policy, so using PPO, or the variant of they used GRPO as an optimization algorithm in the R1 setup, to me, feels absurd.

<br>

_So what does this all mean for the AI industry?_

To be honest I don't see this dramatically shifting the industry in its current state. I'd imagine players like OpenAI, Anthropic, Google, etc will continue to produce better and better closed source models that are easy to integrate and adopt. These companies will continue to do what they've been doing all along: pushing for general intelligence. What I do see happening, is more and more companies experiment with tuning their own reasoning models for their specific use cases. The big caveat here is that tuning these models requires a lot of compute and can only be applied to a domain with obvious ways to determine success or failure. There aren't a ton of these use cases off the top of my head, but I'm sure we'll see people much smarter than me figuring out how to overcome this.

<br>

_So, what's next? Where does R1 go from here?_

I've actually spent a bit of time thinking about this. So far, this setup reminds me of old school RL models applied to Atari-like games. In these setups, the state is the game screen pixels, and the agent uses this to determine the next action. In the years that followed, a lot of algorithms developed to improve their performance on various Atari games, including DQN, PPO, A3C, Go-explore, etc. Then came Google's Dreamer v1. What they showed that it was better to for a model to predict actions in a latent space rather than pixel space. This ended up being a huge breakthgrough, as subsequent their followup model Dreamer v2 became the first model to achieve human level performance across all 55 Atari games.

Ok, so how does this relate to R1? Well, if you think about it, using language tokens to reason feels a lot like determining next actions in pixel space. So, much like how Dreamer v1 showed reasoning in latent space was better, I'd imagine that reasoning models will begin to shift away from language tokens and reason in some sort of latent space. There's already some [work](https://arxiv.org/abs/2412.06769) on this space, but I think we'll see more and more of this in the future.

---
layout: post
title: What I've been up to...
draft: false
---

"Here's to a long and lasting blog!"

These were the last words on my very first blog post, and like Aang the last airbender, I disappeared. But just like McDonald's McRib when you missed it most, I'm back (hopefully)! I wanted to kick off my return by talking about where I've been and how I got to where I am now.

Our story starts in Fall 2022, when COVID was finally in our rear view mirro, but just barely.

## Fall 2022: I graduated!

It's Fall 2022 semester, and I'd recently decided I was abandoning my plan to be a hardware engineer. I spent 3 months the previous year on a DV (design verification) team at Apple and found the whole thing kinda drab. I was learning a lot and it was super interesting, but just not for me.

### Next Stop: PhD?

The highlight that semester was the research project I picked up during the summer. Something about being able to work on my own cool idea, and believing I was on the cusp of the next big breakthrough just made it seem like the perfect job. Being able to work and travel when I wanted was definitely a plus too.

Ok that's it, I've decided, I'm gonna do my PhD!

But then it came time to submit the paper. The PI started getting more agitated and demanding, and even after submitting, reading comments on OpenReview of our paper and other papers were pretty eye-opening. I saw reviews would say things along the lines of "this isn't a significant contribution", or "this paper makes claims are too strong and corroborated by their experiments". Yea, pretty brutal stuff.

I guess academia isn't this beautiful place where you can work on your own stuff whenever you want. It's a bloodthirsty battleground where students are forced produce paper faster than our hair grows. With thousands of researchers worldwide, it's not only a race to get our idea out before someone else does, it's a race to beat your peers and publish the best papers, so you can get the best postdoc, so you can get the best professorship, so you can get tenure, ... and so on. You get the idea.

Yea, no. I think I'll get a job instead.

I like to think I made this decision for the reasons above, but maybe it's just cope cause I didn't think I was good enough to get into a good program.

### Recruiting

I don't have that much to say here. Recruiting is a fat grind. Here are some random things I remember from that time

- I interviewed at Nextdoor and asked what they least like about their platform. They said they wished the platform was less toxic. Wasn't sure what to say to that.
- I applied to a company called Lucid thinking it was the EV company. When they reached out I was really confused since the recruiter's email was from a lucidchart.com domain. Took a couple more emails to realize the company I applied to did not make EVs.
- I did my first systems design interview. I remember feeling completely lost learning about SQL vs NoSQL databases, CDNs, load balancers, sharding, etc. Turns out college really does not teach you what real world software is about.
- I was blown away by my interviewer at Green Hills Software. I remember he said he worked on some way of saving and replaying state of your software system beyond just CPU state. Don't remember the details but I remember thinking it sounded super cool and complex.
- panic learned C++ for an interview. Proceeded to immediately forget the syntax during the interview. Did not get the offer lol.

I was fortunate enough to learn about a lot of really cool companies. Here is a short list of some that stood out to me (in no particular order):

- Zipline - autonomous delivery drones. I remember their perception stack relied on using sound. Really innovative stuff.
- Armstrong Robotics - robotic dishwasher. Really impressive capabilities based on a demo they showed me. It could clean off plates properly, throw out deformable objects (like napkins), empty out cups in the sink, etc, all before loading the actual dishware into the dishwasher.
- Crusoe - started off doing carbon negative bitcoin mining. Since moved to opearting a GPU cloud based off renewable energy. Might be biased since I worked here :).

I ended up with an offer from Crusoe as a SWE, and another AI company as an MLE. I went back and forth for a bit. On one hand working as an MLE would keep me up to date with the latest ML research should I change my mind about a PhD, but the company had a questioanble work culture. On the other hand, Crusoe was pretty small, so responsibilities were much bigger; the downside being the work is unrelated to ML.

In the end, I was drawn by the fact Crusoe was small, so projects up and down the stack were abundant and the scopes were big. The team itself having a sizeable amount of young engineers also helped.

## Crusoe - First Job!

I started at Crusoe in March 2023. The engineering team was maybe 30 people at the time, mostly based out of SF. This was my first time working out of a real office. They gave me a monitor, keyboard, mouse, but I'm so used to working from my laptop I just never used the other stuff. People also find the 2 finger zoom I like really weird (it's the accessibility thing on macs, where you can zoom the entire screen not just the window you're on), so it was amusing to everyone when someone took over to help me debug stuff, and proceeded to struggle to do anything.

I started on the GPU cloud team mostly doing small feature stuff for their cloud product. This was fine for a bit, since I was still giddy and doe-eyed about working for a real company. Eventually I got bored, and fortunately, my manager was cool with letting me switch to the Bitcoin mining team.

After 6 years of education I was finally ready to become what I was always destined to be... A crypto chad.

### Becoming a "Crypto Bro"

I'd like to dedicate this section to tell you why Bitcoin is the future and why I've put all my life savings into it.

Jokes aside, the switch was a really exciting time for me. As a bit of background, the Bitcoin mining business was the original cornerstone of Crusoe's business. The idea was to bring big generators to oil sites that flare a lot of gas, and divert the flared gas through the generators to power a datacenter's worth of Bitcoin miners. The problem itself is complex, and not gonna lie, it made me happy to say I was contributing to a carbon negative business.

I ended up taking over an existing project on the team building Bitcoin miner firmware. The project was motivated by Bitcoin miners being flaky and weren't designed for fine grained control that we wanted. The goal was to reverse engineer the communication system to the actual ASICs, and then build software around it.

"You have a strong low level software and hardware background right?"

"Yes, I think I can make progress on this" I said despite not having thought about embedded software in the last 2 years.

The project ended up being really fun. I learned a lot about working with custom control boards, and replay attacks, and got a chance to build something pretty cool. We ended up building a PoC and was ready to scale up before the project got cancelled. I won't get into it, but in the end the costs outweighed the benefits and a strong third party alternative emerged.

### Moving on?

By early 2024, Crusoe was doing great. The company was growing insanely quickly. We had moved to a bigger office, hired a ton more people, and split teams into specialties. My commute went from the (slightly) sketchy streets of the Mission to the shiny skyscrapers in the Financial District. While this was great for the company, it felt less great for me. I enjoyed working the most when it felt like a scrappy startup and I was shipping important features often, but Crusoe was rapidly outgrowing that stage. I still loved the company and the people I worked with, and while I wasn't ready to leave, I did start to think about what I'd do next.

## Moving on

One of my good friends got into YC for the winter 2024 batch. While I was incredibly happy for him, I'd be lying if I said I wasn't a little jealous. _Dang he's building his own company. That's wild._

So when a coworker at Crusoe mentioned he'd been thinking of starting his own thing, I _subtly hinted_ that I might be interested. It'd been a while since I was properly excited at work, so the idea of embarking on this uncertain, difficult, stressful, depressing journey of building a company was super exciting to me.

Only thing was we needed an idea.

And money.

After putting our heads together and coming up with some banging ideas, we eventually found one we all would be willing to work on for at least 5 years, and applied to YC a few days after the deadline.

This post is already getting long so I'll leave most of the details out for a future post.

The gist is somehow we ended up getting in and in a whirlwind few months we:

- quit our jobs (after a slightly precarious visa situation)
- came up with a name and incorporated our new company
- had to change names after an excisting YC company with the same name kindly suggested to change it.
- went through YC and _built something that people wanted_
- jk we built something that no one wanted but still ended up with a few paying customers
- raised a bit of seed money
- moved to a new office

## Winter 2025

That brings us to today! We're building some exciting things at Parity. There's a lot I can say about the last 6 months, but I'll leave that for a future post.

So, that's roughly what I've been up to. 5 years ago I never would have guessed where I'd be today. That was always my goal, so I'm glad I got there.

Speaking of goals, though, one of mine for this year is to actually post here, so, to quote me from 4 years ago:

"Here's to a long and lasting blog!"

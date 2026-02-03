---
layout: post
title: 2025 - A Year in Review
draft: false
---

2025 has felt like the shortest year so far since I graduated college. Its scary to think that this is my 5 year college reunion, and we're a year away from my 10 year high school reunion. To help future me reminisce and unpack what happened last year, I wanted to take the time to break down the last year and share some highlights.

# January

The start of the month was hectic. Started the month skiing in great conditions at Whistler for a few days. I got back from Vancouver, had friends fly in and stay with me that night, then drove to Tahoe to ski a day later. We got a reservation at San Ho Wan, after being told they were closing, although we were wrong and it was actually Sam Wo that was closing lol. I also flew back to Vancouver to spend Lunear New Year with my parents which was nice!

On a work note I spent the month building some cool AI enabled workflows for Kubernetes investigations. The main meat here was figuring out how to represent the state of a Kubernetes cluster, and how to collect this data quickly. This information is then filtered to individual workflows that independently process this data and look for signals as to whether a misconfiguration, networking, resource, etc issues exist. A big chunk of the work here was making things look good in Slack and our chat UI. I do not miss hardcoding Slack blocks and markdown strings

<div class="photo-grid grid-1">
  <a href="/img/blog/2025-review/january_1.JPG" target="_blank"><img src="/img/blog/2025-review/january_1.JPG" alt="January"></a>
</div>

# February

Building off of last month, I mostly improved the custom workflow feature, creating a way to automatically, or through user overrides, determine which subset of workflows to run given a specific issue. Also `o3-mini` was the hot new model we were using (crazy that was SOTA compared to what we have now).

I got to ski Alta and Snowbird with some friends which was super cool. Almost lost my rental car keys falling in some deep snow out of bounds, had to dig our car out in the middle of a blizzard, only to crawl our way down LCC over 4+ hours, but hey, small price to pay for that fresh Utah pow.

<div class="photo-grid grid-2">
  <a href="/img/blog/2025-review/february_1.JPG" target="_blank"><img src="/img/blog/2025-review/february_1.JPG" alt="February"></a>
  <a href="/img/blog/2025-review/february_2.JPEG" target="_blank"><img src="/img/blog/2025-review/february_2.JPEG" alt="February"></a>
</div>

# March

Our pilot was picking up and I spent the month building a system for surfacing relevant documentation for new alerts. This involved me building out a RAG + ingestion pipeline for notion docs and slack threads. A chunk of this time was spent comparing vector DB solutions: pgvector vs pgvetorscale vs LanceDB vs Pinecone. We went with pgvectorscale. I also built a separate service for a self-hosted embedding model because of data exfiltration constraints. We ended the month attending SRECon down in Santa Clara and met some cool people.

March also featured a few friends from college visiting. I got to try Beep's, which was supposed to be the best burger in SF. I thought it was ok but surely there's a better burger in SF right? I made some big (for me) and irresponsible bets on March Madness and subsequently lost. In my defense it was the first year since 2017 no team seeded 13 or lower advanced to the second round. SRECon was the end of the month - gave me a taste for commuting down to south bay and it was not fun, even if I were to stop at Zareen's for dinner everyday.

<div class="photo-grid grid-1">
  <a href="/img/blog/2025-review/march_1.jpg" target="_blank"><img src="/img/blog/2025-review/march_1.jpg" alt="March"></a>
</div>

# April

KubeCon London! This was the first time I had been apart of a conference as a sponsor. We had a booth and were giving away tote bags to people who were curious about our product. Definitely a unique experience. Highlight for me was talking to the CTO of a large neocloud, not realizing it was the CTO, and asking if he was an SRE. Outside of KubeCon I worked mostly on improvements to features from the last few months. I improved the context gathering of the clusters for investigations, and the RAG tool. Also o4-mini and gpt-4.1 came out. Not really a huge unlock but we'll take incremental improvements on latency and intelligence.

Pretty slow month outside work. Biggest thing was the SF Moma after dark event they put on every year that I went to with the same group as last year. It's definitely a cool event and unique way to experience the museum.

<div class="photo-grid grid-1">
  <a href="/img/blog/2025-review/april_1.jpg" target="_blank"><img src="/img/blog/2025-review/april_1.jpg" alt="April"></a>
</div>

# May

This was probably the busiest month of the year so far. I improved our chatbot and got rid of the routing layer and just exposed everything as tools to a single LLM. I ended up building a MCP-esque interface that exposed internals of the platform so users could ask any questions and execute any workflow without needing to pass context around manually.

About mid month we made the difficult decision to pivot away from the existing idea and began exploring AI generated Minecraft mods. I worked a lot on the generation side of this, figuring out how to make this system reliable. By the end of the month we built ways to generate new mobs and items with a pretty high success rate. The end of the month was spent improving things, adding tools to allow the agent to see function signatures of obfuscated code, adding observability to the generation traces, etc.

Outside of that stuff, a lot of firsts happened this month. Our first intern started this month, I played my first adult league tennis match, joined and played in my first street hockey league game, and got ordained and asked to officiate a friend's wedding! Karate Kid Legends came out this month and they gave out wrist bands at the AMC to everyone watching this movie, which I'm still weaering it as of today :) (January 2026)

<div class="photo-grid grid-2">
  <a href="/img/blog/2025-review/may_1.JPG" target="_blank"><img src="/img/blog/2025-review/may_1.JPG" alt="May"></a>
  <a href="/img/blog/2025-review/may_2.jpg" target="_blank"><img src="/img/blog/2025-review/may_2.jpg" alt="May"></a>
</div>

# June

We had an issue early in our system where we needed `xvfb-run` to load minecraft which was absolutely eating CPU. First thing this month was finding another way of smoke testing generated mods without this task. Most of the beginning of the month was also focused on mod generation for Minecraft Bedrock edition.I built some of the early scaffolding but mostly handed it off to our new intern, who killed it! The other big feature I built was the ability to edit mods and add new features or make fixes. I also added some other static analysis of generated code to prevent long build cycles, improved the logging and observability during generation. Claude 4 Sonnet came out which was a pretty big step up for us.

Pride month! I signed up for a ping pong tournament with a friend of mine. I am not ping pong player but talked my way into the intermediate bracket even though I have no business being there. Other highlights include being invited to a box for a Giant's game, supporting my friend DJing for a pride event, and going to [Good Times](https://www.theco.site/good-times).

<div class="photo-grid grid-2">
  <a href="/img/blog/2025-review/june_1.JPEG" target="_blank"><img src="/img/blog/2025-review/june_1.JPEG" alt="June"></a>
  <a href="/img/blog/2025-review/june_1.jpg" target="_blank"><img src="/img/blog/2025-review/june_1.jpg" alt="June"></a>
</div>

# July

Big things this month were improving the edit experience. I extended this feature for Minecraft Bedrock, allowed it to create arbitrary kinds of items / mobs. Outside of this I also extended item generation for Java to be able to create placeable and interactable blocks.

Spent 4th of July week in NYC and got a chance to go skeet shooting with some friends! Played in the ping pong tournament I signed up for last month. Lost every game and won exactly 1 set lol. 10/10 experience would do it again. Also ended up signing up for a softball league with a friend despite never having played any form of baseball or softball before. I like throwing and catching but I am very much clueless out there.

<div class="photo-grid grid-1">
  <a href="/img/blog/2025-review/july_1.JPG" target="_blank"><img src="/img/blog/2025-review/july_1.JPG" alt="July"></a>
</div>

# August

Biggest win this month was improving mob retexturing. We switched from an approach that was built generating a fresh UV texture hoping it would turn out properly, to a pipeline that was guaranteed to produced proper UV maps for every mob type. We also started allowing user uploaded reference images when editing mods, and improved some of the observability integrations. We saw a few attempts at users generating malicious mods so we beefed up our safety rails against that too (lol). I also added a stage to the generation pipeline that made tool tips for items. Little did I know this would pretty significantly increase latency on generations but more on that later :) Also gpt-5 came out (this is kinda crazy to me since it's almost half a year ago from me writing this).

Played squash with the interns, which served as the only social event we did before they left. I also saw F1, which was undoubtedly the movie of the year for me. We also had a work trial come in for a few days and work with us, which was a thing. My street hockey team had playoffs - we got hard carried by one of our players and lost a tight one in the finals. Final game was pretty chippy and competitive and borderline not enjoyable. There was a lot of yelling, an almost fight and a lot of penalties. Ended the month with a trip to Japan!

<div class="photo-grid grid-3">
  <a href="/img/blog/2025-review/august_1.PNG" target="_blank"><img src="/img/blog/2025-review/august_1.PNG" alt="August"></a>
  <a href="/img/blog/2025-review/august_2.jpg" target="_blank"><img src="/img/blog/2025-review/august_2.jpg" alt="August"></a>
  <a href="/img/blog/2025-review/august_3.jpg" target="_blank"><img src="/img/blog/2025-review/august_3.jpg" alt="August"></a>
</div>

# September

Started the month in Japan. Despite that still managed to get a bunch of work done. Used what we learned about generating mob textures to generate armor textures. This means we now support generating armor pieces as apart of the generate item option. Claude Sonnet 4.5 came out which was a slight step up from Sonnet 4. The big thing this month was we were starting to be bludgeoned by costs. That tooltip thing from last month added a bunch of extra LLM calls with already large contexts for almost no reason, so that was consolidated. We had a few other places where we could consolidate similarly so I mostly worked on that to get costs down a bit.

Japan was great! My only complaint was that it was exceptionally hot. Highlights for me were definitely visiting Uji and spending a ton on matcha, climbing in local gyms in Tokyo and Kyoto, and just being in such a sprawling bustling city at night. On my way back to SF, I met up with some friends in Vancouver to climb in Squamish. It was my first time and I was pretty blown away by the density of stuff at the Grand Wall. Definitely would like to make it a yearly visit. After I got back, I had a few college friends visit and stay for the Laver Cup. The event itself was great we got the full 4 matches even if Zverev got whipped by Fritz in the last one.

<div class="photo-grid grid-4">
  <a href="/img/blog/2025-review/september_1.jpg" target="_blank"><img src="/img/blog/2025-review/september_1.jpg" alt="September"></a>
  <a href="/img/blog/2025-review/september_2.jpg" target="_blank"><img src="/img/blog/2025-review/september_2.jpg" alt="September"></a>
  <a href="/img/blog/2025-review/september_3.jpg" target="_blank"><img src="/img/blog/2025-review/september_3.jpg" alt="September"></a>
  <a href="/img/blog/2025-review/september_4.jpg" target="_blank"><img src="/img/blog/2025-review/september_4.jpg" alt="September"></a>
</div>

# October

Costs did not come down and I spent the month mostly trying to fix that. Started with realizing prompt caching was broken for models on AWS Bedrock because their documentation is completely unclear as to what is proper prompt caching and what isn't. Took a bit of investigation but got it working and it helped but not enough. Spend most of the month data wrangling trying to fine tune our own model with varying degrees of success. In the end we decided not to put all our eggs in one basket and adjusted a bunch of things to bring costs down to a manageable level.

It was tough working this month since I spent most of it home in Hong Kong. I ended up working local hours, but had handoffs late at night to the team, and would sync up again in the early morning. Being home was nice, gave me a chance to focus on spending time with family and really slow everything down. Had a few friends from SF come visit for a few days, which gave me a chance to experience and appreciate being a tourist in my hometown again.

<div class="photo-grid grid-2">
  <a href="/img/blog/2025-review/october_1.jpg" target="_blank"><img src="/img/blog/2025-review/october_1.jpg" alt="October"></a>
  <a href="/img/blog/2025-review/october_2.jpg" target="_blank"><img src="/img/blog/2025-review/october_2.jpg" alt="October"></a>
</div>

# November

After spending last month working on lowering costs, I went back to implementing some new features. I shipped support for a very hotly requested version of Minecraft. This involved a pretty big refactor of our generation code and meant creating a common interface that each Minecraft version would implement. After shipping that I moved on to work on structure generation. Difficult part here wasn't creating the structure, it was mapping the colours in it to a palette of blocks in Minecraft that maintains consistency. Small deviations in RGB values would lead to pretty wild changes in block chosen. Ended up getting something that _mostly_ worked but we weren't totally happy with it. In other news, Opus 4.5 came out and it's by far the best model I've used to date.

Month in general was pretty busy. I was climbing a lot and playing a lot of tennis. Spent Thanksgiving with some friends of friends and discovered a really cool card game called Dutch Blitz.

<div class="photo-grid grid-2">
  <a href="/img/blog/2025-review/november_1.jpg" target="_blank"><img src="/img/blog/2025-review/november_1.jpg" alt="November"></a>
  <a href="/img/blog/2025-review/november_2.jpg" target="_blank"><img src="/img/blog/2025-review/november_2.jpg" alt="November"></a>
</div>

# December

We revamped our 3D pipeline with some cool new tech that came out. We redid our structure generation pipeline and rather than mapping RGB values to existing blocks, we created a custom block with that RGB value (approximately) instead. There was a lot of issue with alignment that we had to solve, and translating a 3D object with a certain camera view to one that showed up aligned along block boundaries in Minecraft was actually a very difficult problem. Once we had solved this for structures, we applied a similar method to creating custom objects.

Did a bunch of stuff with one of my friends this month since they were moving to NYC soon. This included going to his DJ event in a cave, an escape room, and just hanging out at his office before he left his job.I spent the holidays in Vancouver with my family and even got a chance to ski a few days at Whistler. Huge difference in conditions considering it hasdn't snowed in Tahoe yet lol. Celebrated the new year with one of my cousin's and his friends.

<div class="photo-grid grid-4">
  <a href="/img/blog/2025-review/december_2.jpg" target="_blank"><img src="/img/blog/2025-review/december_2.jpg" alt="December"></a>
  <a href="/img/blog/2025-review/december_3.jpg" target="_blank"><img src="/img/blog/2025-review/december_3.jpg" alt="December"></a>
  <a href="/img/blog/2025-review/december_4.jpg" target="_blank"><img src="/img/blog/2025-review/december_4.jpg" alt="December"></a>
  <a href="/img/blog/2025-review/december_5.jpg" target="_blank"><img src="/img/blog/2025-review/december_5.jpg" alt="December"></a>
</div>

Overall a year that passed by a bit too fast, so hoping to savor 2026 just a _little_ more.
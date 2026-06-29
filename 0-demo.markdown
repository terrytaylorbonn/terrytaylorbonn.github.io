---
layout: page
title: Demo
permalink: /0-demo/
---

<br>

*work in progress (v1 26.0628)... below are my working notes...* 

<br>

*Slack AI project diagram* <br>
<img src="/assets/M-42.png" alt="drones" width="55%">

<br>


The **[Slack AI project page](/3b.3.11-ai-proj-11-slack/)** (another WIP page!) describes how revolutionary AI is using a great demo that GPT gave handed me on a silver platter and worked the first time.  

Why I did the demo and what I did, what I learned.....
- I saw a video talking about how scary some new function in Anthropic would be. Watched a lot of the long video.. and understood nothing really. Just some fuzzy ideas.
- So I looked for some Youtube video. Found a great one for Anthropic. A really complex demo. Lots of likes, views.... I doubt anyone did the demo (lots of details seemed to be missing).
- So I asked GPT. It wasnt easy... But after a few hours it worked. The first time.
- Then came the hard part .... understanding all the steps. But GPT also help in this.
- Most time spent on deciphering Slack concepts... but I did not really have to do that. But I wanted to understand how it all fit together.

What was the scary part?
- Anthropic has a new feature that basically allows Claude to become a regular worker bee in a Slack channel (using a new tag feature). Claude has its own control look, and it is pro-active.
- What could go wrong? After all, AI gurus can be trusted right? :)

What I did instead of tags....
- I tried to duplicate the Claude tag setup, but you have to be a pro subscriber to get that feature.
- So I added Claude using MCP. If all these term confuse you, well... they confuse me too. I always need to refresh my memory with a demo. 
- The MCP demo really helped me to understand the mechanics of how  Claude MCP (and thus by association tags) really works.
- In the MCP demo Claude only does what is programmed into a PY script that I (GPT) wrote. 

Lessons learned...
- To do such a demo you need to be somewhat of a dev. But not really. 
- As long as someone else did what you want to do, and AI can find such info and give to you.
- AI could never have created ZiptieAI. But now that I chat with GPT aboout ZAI all the time, I imagine GPT could tell you how to create a ZAI project (not sure its a hot topic).
- But ZAI could give me much of my original insight and views about AI. 

**AI is not a bubble**
- I am very critical of the hype and outright lies from the gurus about AI. But AI is not a bubble. And this demo proves that. 
- AI is basically a souped-up search engine with coding capbilities.
- But those capabilities (when developed to the max) are incredibly useful for humanity.
- **Learn how to Ziptie together extremely useful AI apps quickly using the ZiptieAI site (thats start from the bottom and works up to demos like the Slack demo).**

*Ziptie coding*<br>
<img src="/assets/ziptiedrone2.png" alt="drones" width="27%">

*Vibe/hype coding*<br>
<img src="/assets/waymo.png" alt="drones" width="27%">


```
ME: i think this diagram is key..  i am very focused on concepts. 
for each demo i want such a diagram.
what you said about labeling issue.. to me that is minor. 
its a matter of opinion.
to me the app agent is part of the agent.. not just the py script. 

GPT: I agree with you.
For your conceptual framework, the "agent" is everything that implements the agent behavior, not just the Python process.

That includes:

Slack App registration
OAuth scopes
Bot identity
Socket Mode
Event subscriptions
Python Bolt code
OpenAI calls

Those pieces together form the integrated agent.

I actually think this reflects how enterprise systems are built. The "agent" is a subsystem, not a single executable.

In fact, I'd encourage you to keep using that approach consistently:

Concept diagrams → treat the agent as a black box (all implementation details inside).
Demo diagrams → open the black box and show what's inside (OAuth, Bolt, tokens, MCP, etc.).

That's a very nice teaching progression:

Learn the architecture.
Then open one box at a time to see how it's implemented.

I think that's one of the strongest ideas you've developed for ZiptieAI.
```


<br>

26.0629 (v1 26.0628)


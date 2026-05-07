---
layout: page
title: ZiptieAI History
permalink: /history/
---


<br>

AI tech is evolving quickly. ZiptieAI is evolving along with it. What began as a drone-focused project has become an exploration of practical AI systems. The diagram below shows the project stages. 


<img src="/assets/zai_evolution.png" alt="smol" width="27%"> 

<!--
<img src="/assets/6_main_diagram.png" alt="drones" width="40%"> 
 <img src="/assets/ai_project_diagram_7.png" alt="drones" width="40%"> -->


<br>

#### **(1) [AI Drones](/aidrones/)**

This was the first phase of ZiptieAI (the name was inspired by the zipties Ukraine used to quickly configure drones). This phase included drone flight simulation, hardware builds, AI, and flight tests (the first flight tests were in my kitchen). AI capabilities centered on:
- Object recognition using onboard cameras
- Autonomous flight support (AI-generated flight plan modifications)

My original plan was to spend the majority of my time on the drone AI (the drones were only meant to be carrier platforms). But I ended spending most of my time on building drones because of quality and usability issues with the open source software and components.   

<br>

#### [Tech Stacks & Docs](/tech-stacks/)

I documented my AI drone activities in detail. My original plan was to build my own ZiptieAI DIY drone website, wiki, and blogs (Substack and Youtube). The first step was a refresher course on the latest doc tools (MERN stacks and REST/GraphQL APIs/docs). For the first time I started using the latest AI tools for coding. I was amazed by how much these AI tools simplified development.   

<br>

#### CNNs

CNNs (convoluted neural networks) were used for drone oject recognition. Studying CNNs was good preparation for studying the much more complex LLMs.

<br>


#### **(2) [LLMs](/sandbox/)**

My focus shifted to LLMs (large language models)
  - Transformers (the LLM neural network) *(see the wiki page [AI concepts](https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts) for my explanation of GPT-3 transformer algorithms)* 
  - API-based model usage (major frontier models)
  - Local and remote model deployment (smaller models)
  - Fine-tuning
  - RAG, MCP, and tools

<!-- I became particulary interested in the claims about AI having intelligence (and emotions, consciousness, etc). AI runs on clocked binary circuits (nothing like the neurons in the brain). Theoretically you could build a "mechanical" GPU (based on EM relays) and run AI on it (it would require perhaps years to generate a token). The only difference between the electronic and mechanical GPU would be the execution speed.

I had read that up to 95% of AI projects failed. That meant that 20x more money than necessary was being spent on AI projects. The value of a firm grasp of AI fundamentals was obvious. -->


My goal was to understand the core concepts and how to build practical applications.

<br>

#### (3) [Robotic AI](/robotic-ai/)

AI makes mistakes. For chatbots this is no big deal. But robots (especially those around humans, such as cars and humanoids) must not make mistakes. Yan LeCun's claims that JEPA would provide real robotic intelligence intrigued me. So I did a lot of hands-on JEPA demos. I think what he is selling is not fundamentally different from LLMs. GPT agreed. 

In any case, the time spent doing hands-on demos (for representational learning, prediction-based systems, belief tracking, control loops, planning under uncertainty, etc) was well spent. Many of the concepts (such as estimation and autonomy) were related to earlier drone work.

<br>

#### **(4) [Agentic AI](/agentic-ai/)**

AI agents are the deterministic control loops (often written in Python) that are the core of AI applications. "Autonomous" AI agents perform complex tasks with limited (but critical) human intervention. My interest in AI is primarily in this area.  I became particulary interested in Palantir's AI systems because 
- (1) they are very effective and 
- (2) they can be used for a vast array of non-military purposes (logistics, manufacturing, healthcare, defense, operations, business intelligence)

There were claims that Palantir's systems could become the real world [SkyNet](https://en.wikipedia.org/wiki/Skynet_(Terminator)) *(see my substack post [#73 Understanding Palantir Maven / Why AI will never become Skynet](https://ziptieai.substack.com/p/73-understanding-palantir-maven-through))*. But Palantir's systems are assisted by AI, not controlled by AI. AI is simply a "helpful assistant". AI does not press any buttons. The core control loop is traditional non-AI deterministic programming. AI is used for 
- Input and output (of "messy" human language representations)
- Task planning (breaking up complex human language tasks into smaller deterministic tasks)
- Rule injection (by AI into the main loop)

Agentic AI (with it's helpful AI assistants) will be one of the fastest-growing segments of AI in the future. The success of Palantir shows that such systems are already viable AI applications.

<br>

#### **(5) [AI dev tools](/AI-dev-tools/)**

The goal of this section is to demo
- AI dev tools/IDEs (Codex, Cursor, etc) and 
- related plugins (like the Render plugin for Codex)


<br>

#### **(6) [AI projects](/AI-projects/)**

After learning the AI dev tools and plugins you can "spin up" quickly complex projects. The goal of this section is to create demos of real-world AI projects that were spun up fast. 

<br>

<!--
# CLAUDE VERSION 26.0503 =======================

<!-- INTRO: Tightened. Same idea, fewer words. 
<br>

AI tech is evolving quickly. ZiptieAI is evolving with it. What began as a drone project has become an exploration of practical AI systems — from hardware to agents to real-world apps.

<img src="/assets/zai_evolution.png" alt="smol" width="27%"> <img src="/assets/6_main_diagram.png" alt="drones" width="40%"> 
<!-- <img src="/assets/ai_project_diagram_7.png" alt="drones" width="40%"> -->

<!-- ![ZiptieAI evolution diagram](/assets/zai_evolution.png) ![AI project components diagram](/assets/6_main_diagram.png) 

<br>

#### (1) [AI Drones](/aidrones/)

<!-- PERSONAL: Kept the kitchen detail — it's good. Fixed "convoluted" → "convolutional", "oject" → "object" 

The name ZiptieAI was inspired by the zipties Ukraine used to rapidly configure battlefield drones. This first phase covered simulation, hardware builds, AI, and flight tests — including early tests in my kitchen.

AI capabilities:
- Object recognition using onboard cameras (CNNs)
- Autonomous flight (AI-generated flight plan modifications)

In practice I spent more time building drones than doing drone AI — open source software and components had significant quality and usability issues.

<br>

#### [Tech Stacks & Docs](/tech-stacks/)

<!-- NOTE: This section felt out of sequence in the original — it's a side activity, not a phase. Kept brief. -

Documenting the drone work led to a refresher on MERN stacks, REST/GraphQL APIs, and modern doc tools. First serious use of AI coding tools. The productivity difference was immediately obvious.

**CNNs** — convolutional neural networks for drone object recognition. Good conceptual preparation for the more complex transformer architectures in LLMs.

<br>

#### (2) [LLMs](/sandbox/)

<!-- TRIMMED: List was fine, just cleaned up -

Focus shifted to large language models:
- Transformer architecture *(see [AI concepts](https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts) wiki page for GPT-3 deep dive)*
- API-based usage (frontier models)
- Local and remote model deployment
- Fine-tuning, RAG, MCP, tool calling

Goal: understand core concepts well enough to build practical applications.

<br>

#### (3) [Robotic AI](/robotic-ai/)

<!-- JEPA: Removed "GPT agreed" — your opinion stands on its own. Sharpened the critique (matches our earlier conversation). -

Robots around humans — cars, humanoids — cannot make mistakes the way chatbots can. LeCun's JEPA claims of "real robotic intelligence" were worth investigating.

Conclusion after hands-on demos: JEPA is a useful architecture with real engineering advantages, but the "true intelligence" framing is overstated. The distinction between predicting in embedding space vs. pixel space already exists in CNNs and LLMs — it's not the philosophical breakthrough LeCun suggests.

The demos themselves (representational learning, belief tracking, control loops, planning under uncertainty) were valuable — many concepts overlapping with earlier drone autonomy work.

<br>

#### (4) [Agentic AI](/agentic-ai/)

<!-- PALANTIR: This is your best section. Minor trimming only. Fixed "particulary". -

AI agents are the deterministic control loops — typically Python — that form the core of AI applications. This is where my primary interest lies.

Palantir's systems are a useful reference point:
- Highly effective in practice
- Applicable far beyond military use (logistics, manufacturing, healthcare, business intelligence)

The "Palantir as SkyNet" concern misunderstands how these systems work. *(See Substack post [#73: Understanding Palantir Maven / Why AI will never become Skynet](https://ziptieai.substack.com/p/73-understanding-palantir-maven-through).)*

AI in these systems is a helpful assistant, not a decision-maker. The core loop is traditional deterministic code. AI handles:
- Input/output normalization (messy human language → structured data)
- Task planning (breaking complex requests into deterministic steps)
- Rule injection into the main loop

Agentic AI is one of the fastest-growing segments. Palantir proves these systems are already viable.

<br>

#### (5) [AI Dev Tools](/AI-dev-tools/)

<!-- STUB: Original was too short. Gave it a bit more substance without over-expanding. --

Hands-on demos of AI IDEs and tools — Cursor, Codex, and related plugins (e.g. Render plugin for Codex). Focus on what these tools actually change about the development workflow, not just what they claim to do.

<br>

#### (6) [AI Projects](/AI-projects/)

<!-- STUB: Same — gave it one more sentence of context. --

With solid AI dev tools, complex projects can be spun up fast. This section demos real-world AI pipelines built rapidly — the kind of end-to-end systems (ingest → normalize → store → query → deliver) that reflect how production AI applications actually work.

<br>  -->


26.0506

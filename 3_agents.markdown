---
layout: page
title: "3 Agents"
permalink: /3_agents/
---

<br>

**If you want to get started ASAP with agentic AI (TL;DR)**, then these are the core pages you need:
- **[(4) Agentic AI](/agentic-ai/)**. Core concepts and basic demos. 
- **[(5) AI dev tools](/AI-dev-tools/)**. Cursor, Codex, VSC, Claude (no IDE), etc.
- **[(6) AI projects](/AI-projects/)**. Demos (with Github repo and docs).

*This diagram appears throughout this site. The agent and the IDE dev tools are front and center (the LLM is a helpful assistant)*. <br>
<img src="/assets/6_main_diagram.png" alt="drones" width="45%"> 

<br> <br> <br> <br> <br> <br> 

-------------------------------------------
-------------------------------------------
-------------------------------------------
-------------------------------------------

<br> 
*TODO: integrate this text from other pages*


#### **(4) [Agentic AI](/agentic-ai/)**

**AI agents are the deterministic control loops (often written in Python) that are the core of AI apps**. My interest in AI is primarily in this area.  I became particulary interested in Palantir's AI systems because 
- (1) they are very effective and 
- (2) they can be used for a vast array of non-military purposes (logistics, manufacturing, healthcare, defense, operations, business intelligence)

<!--  "Autonomous" AI agents perform complex tasks with limited (but critical) human intervention.  -->

There were claims that Palantir's systems could become the real world [SkyNet](https://en.wikipedia.org/wiki/Skynet_(Terminator)) *(see my substack post [#73 Understanding Palantir Maven / Why AI will never become Skynet](https://ziptieai.substack.com/p/73-understanding-palantir-maven-through))*. But Palantir's systems, like **all agentic AI systems, are assisted by AI (not controlled by AI)**. The LLM is simply a "helpful assistant". **LLMs control nothing, push no buttons**.

 The core control loop is traditional non-AI deterministic programming that performs
- Input and output (of "messy" human language representations)
- Task planning (breaking up complex human language tasks into smaller deterministic tasks)
- Rule injection (by AI into the main loop)

Agentic AI (with it's helpful LLM assistants) will be one of the fastest-growing business segments in the future. 

***My depiction** of the agent (external) in the LLM ecosystem*<br>
<img src="/assets/GPT_agent.png" alt="desc" width="55%"> 

<!-- <img src="/assets/4_agentic.png" alt="drones" width="45%"> -->

<br>

#### **(5) [AI dev tools](/AI-dev-tools/)**

The section focuses on 
- AI dev tools/IDEs (VSCode, Codex, Cursor, etc) and 
- related plugins (like the Render plugin for Codex)

The main topics are
- Overview, intros, videos
- Overall effectiveness (ease of use, reliability, "hallucinations", cost, etc). For example, **Claude restarts daily and all previous conversations are lost**. Rather inconvenient (this might be because I am using the free version with API credits).
- **Security issues**. For example, Cursor pasted a secret from my .env file in a chat. Cursor later alerted me that I need to **change all my secrets** because the system detected secrets in the chat and **Cursor could not tell me exactly what secrets were compromised or when**. 


*AI IDE and the components it creates*<br>
<img src="/assets/5_IDEs.png" alt="drones" width="22%"> 

<br>

#### **(6) [AI projects](/AI-projects/)**

This section focuses on "spinning up" real-world projects quickly with minimal code analysis or manual coding. Currently there are 2 demos
- #2 Jobradar project using Cursor/Claude. Ingests data from different sources and uses LLM to find matching data and summarize. The results are then sent by email, google docs, etc. Runs locally and on Cursor. Spun up in 4 days. **I did not even look at the code (not necessary). This is probably how such apps will be done in the future.** 
- #1 A simple Codex/VSC demo: Data input (UI, n8n local), sanitization, storage to a DB, and viewing in UI. Local and Render. I did analyze the code and manual modify a few times.

*A complete project (IDEs and LLMs can be switched quickly)*<br>
<img src="/assets/6_projects.png" alt="drones" width="45%"> 

<br>
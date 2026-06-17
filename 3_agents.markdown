---
layout: page
title: "3 Agents"
permalink: /3_agents/
---

<br> 

Conceptual summary of agents:
- Agent = any external (to the LLM) program that calls the LLM API. Basically plays the role of a human during chat (but can do much more).
- AI Agent = an agent that can exploit the higher level abilities of LLM.
- AI Agents provide
  - reliable workflows built around models, tools, and automation. 
  - tolerance of AI faults and unpredictable outputs

<br>

*3 Agents in the master diagram* <br>
<img src="/assets/M-15-3x.png" alt="drones" width="80%">

<br>

### **[3.0 Concepts (was 3.2.1 Intro)](/3.2.1-ai-agent-intro/)**

<br>

### **[3.1 n8n demos (docx \#603)](/3.1-agentic-n8n/)**

**1) n8n local**
- N1 cloud n8n / TTBO gmail 26.0408 (BINGO)	
- N2 n8n_local install / test (json) 26.0409 (BINGO)
- N3 n8n_local (ttbo) / Gmail (jk) read many (set'd up GCP_jk) (BINGO)
- N4 py script replaces n8n app (Win11/jk) (BINGO)
- N5 py script adds PAL (BINGO) 26.0409
- NX TODO	

<br>

### **[3.2 (3.2.5) PAL demos (openAI/Gemma) (docx \#603)](/3.2.5-ai-agent-pal-demos/)**

<!-- Simple demos are the best way to understand agentic AI systems. -->

PAL (Palantir) demos focus on:
- ontology systems
- semantic workflows
- deterministic execution
- LLM-assisted planning
- structured outputs
- external orchestration

**2) pal** 
- [2.1] pal v1 (BINGO) 26.0326
- [2.2] pal v2 (BINGO) 26.0327
- [2.3] pal v3 (BINGO) 26.0327
- [2.4] pal v4 (BINGO) 26.0328
- [2.4b] pal_v4 deploy to render (BINGO) 26.0329-30
- [2.5a] pal_v5 add mongodb (BINGO) 26.0330	
- [2.5b] pal_v5 (with mongo) deploy (NEW) to Render (BINGO) 26.0330
- [2.6] pal_v6 S0-S4 (BINGO) 26.0331-0401	
- [2.7] pal_v7 useful functions (BINGO) 26.0401	
- [2.8] pal_v1 with local Gemma-4 (win11/gpu) 26.0411 (BINGO)

<br>

### **[3.3 (3.1) Agent PAL_core demos (AI ???) (docx \#603)](/3.1-agentic/)**

The core control loop is traditional non-AI deterministic programming

from #603 and in pic
- === 3) pal core ==============================	9
- [3.1] pal_core_01.detect.py (BINGO) 26.0411 (01 events / alerts)	313
- 3.1 ids?????????????????
- [3.2] pal_core_02_predict.py (BINGO) 26.0411 (02 road network / prediction)	288
- [3.3] pal_core_03_allocate.py (BINGO) 26.0411 (03 resources / allocation)	269
- 3.5 ?????????????
- [3.6] (WIP) pal_core_06: simplest demo of all core LLM roles 26.0416	130
- 1-8 
- 3.6-2, 3.6-3, 3.6-4
- 3.6 no LLM codex1?????
- [3.7] pal_core_07_gmail_alerts.py // real emails as sensor stream (BINGO) 25.0423	114
- [3.8] pal_core_08_plan.py // natural language → plan JSON → controlled execution (BINGO) 26.0423	81
- [3.9] — pal_core_09_optimize.py // improved allocation / optimization (BINGO) 26.0427	23
- 2.6 v6 s_hard_prompts ????

<br>

### **[3.4 (3.2.4) TF semantic demos (AI) (docx \#606)](/3.2.4-ai-agent-basic-demos/)**
(docx #606)
Very basic demos that show how **deterministic agents use TF/UFA semantic capabilities**. 
- 1 Basic tool
- 3 Filesystem
- 5 RAG
- 6c MCP + LLM tool choice. 

<br>

26.0617 (0524)


<!-- *Agentic AI in ZiptieAI evolution ([about this diagram](/0.1-zai-evolution/))* <br>
<img src="/assets/zai_evolution7.png" alt="drones" width="42%"> -->

<!-- 
### **[3.3 Agentic AI projects](/3.3-ai-projects/)** (full demo projects (WIP) with Github repo and docs)

"Spinning up" real-world projects quickly with minimal code analysis or manual coding. 

<br> 

-->
<!-- ### [3.2 Agentic + AI](/3.2-agentic-ai/). Core concepts and basic demos -->

<!-- 
Just like iAgent and TF work together internally, the **extAgent and LLM must work together externally**.

- 1 Deterministic agents existed before AI
- 2 TF/UFA semantic capabilities made modern agentic systems practical
- 3 extAgent orchestrates deterministic execution
- 4 LLM provides semantic functionality
- 5 Model Interface Layer (MIL)

 Just like iAgent and TF work together, so **must extAgent and LLM work together**.
- 1 Agents existed long before AI
- 2 Agentic AI (LLMs designed for agents)
- 3 AI'ic agents
- 4 Model interface layer (MIL) 

<br>

### [3.2.2 Diagrams](/3.2.2-ai-agent-diagrams/)
Core diagrams (my own) that explain the architecture.
- 1 Ecosystem
- 2 extAgent <> LLM interface
- 3 Workflow diagram / simple
- 4 Workflow diagram / detailed

<br>

### [3.2.3 AI infrastructure](/3.2.3-ai-agent-ai-infrastructure/)
Agents require external orchestration layers that augment the TF/UFA semantic engine capabilities (such as Tools, Filesystem access, RAG,MCP, APIs, and Workflow orchestration).

- new commands that made them **"agents with AI support"**.
- Connect to LLM
- Send prompts and process responses
*The term "AI-ic agents" is my own. I chose it for several reasons: 
- (1) Agents need AI support, 
- (2) the awkward formulation reminds us of the limitation of human language (that we are bound to and LLMs must process), and 
- (3) its a very short term that accurately (and clearly) defines the meaning ("agentic AI" does not). 

-->


<!--
- **[3 Agents](/3_agents/)** (the focus of this site). Concepts and demos for
  - [3.1 Agentic (no AI)](/3.1-agentic/), 
  - [3.2.4 Agentic + AI (basic)](/3.2.4-ai-agent-basic-demos/), 
  - [3.2.5 Agentic + AI (basic Palantir-style)](3.2.5-ai-agent-pal-demos/), and 
  - **[3.3 Agentic + AI (real-world projects)](/3.3-ai-projects/)** (the end goal of this site). 
-->

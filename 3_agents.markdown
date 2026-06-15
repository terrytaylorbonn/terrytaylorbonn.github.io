---
layout: page
title: "3 Agents"
permalink: /3_agents/
---

<br> 

Conceptual summary of agents:
- Agent = any external (to the LLM) program that calls the LLM API. Basically plays the role of a human during chat (but can do much more).
- Agent + AI = an LLM is used as a useful assistant.
- Provide reliable workflows built around models, tools, and automation. 
- Provide tolerance of AI faults and unpredictable outputs

*3 Agents in the master diagram* <br>
<img src="/assets/M-15-3.png" alt="drones" width="72%">

<!-- *Agentic AI in ZiptieAI evolution ([about this diagram](/0.1-zai-evolution/))* <br>
<img src="/assets/zai_evolution7.png" alt="drones" width="42%"> -->



<br>

### [3.1 Agentic (no AI)](/3.1-agentic/). Core concepts and basic demos

The core control loop is traditional non-AI deterministic programming

<br>

<!-- ### [3.2 Agentic + AI](/3.2-agentic-ai/). Core concepts and basic demos -->

## **3.2 Agentic + AI**

The core control loop is traditional non-AI deterministic programming that performs **(with the help of an LLM)**
- Input and output (of "messy" human language representations)
- Task planning (breaking up complex human language tasks into smaller deterministic tasks)
- Rule injection (by AI into the main loop)

**Conceptual summary**: Traditional deterministic agents existed long before AI, but were rigid and difficult to scale because human language and semantic relationships required hardcoded logic.

Modern TF/UFA systems made such agents vastly more practical by providing semantic capabilities such as:

- Semantic interpretation of human language
- Structured constrained outputs (JSON, schemas, workflows)
- Contextual reasoning over long token sequences
- Task decomposition / workflow synthesis
- Ontology alignment / semantic normalization
- Generalization beyond explicit hardcoded rules

The core control loop itself remains ordinary deterministic software (“extAgent”), while the LLM provides semantic functionality.


<!-- The core control loop is traditional non-AI deterministic programming that performs (with the help of an LLM) for example:
- Input and output (of “messy” human language representations)
- Task planning (breaking up complex human language tasks into smaller deterministic tasks)
- Rule injection (by AI into the main loop) -->


<br>

### [3.2.1 Intro](/3.2.1-ai-agent-intro/)
Just like iAgent and TF work together internally, the **extAgent and LLM must work together externally**.

- 1 Deterministic agents existed before AI
- 2 TF/UFA semantic capabilities made modern agentic systems practical
- 3 extAgent orchestrates deterministic execution
- 4 LLM provides semantic functionality
- 5 Model Interface Layer (MIL)

<!-- Just like iAgent and TF work together, so **must extAgent and LLM work together**.
- 1 Agents existed long before AI
- 2 Agentic AI (LLMs designed for agents)
- 3 AI'ic agents
- 4 Model interface layer (MIL) -->

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

<!-- new commands that made them **"agents with AI support"**.
- Connect to LLM
- Send prompts and process responses
*The term "AI-ic agents" is my own. I chose it for several reasons: 
- (1) Agents need AI support, 
- (2) the awkward formulation reminds us of the limitation of human language (that we are bound to and LLMs must process), and 
- (3) its a very short term that accurately (and clearly) defines the meaning ("agentic AI" does not). -->

<br>

### [3.2.4 Basic demos](/3.2.4-ai-agent-basic-demos/)
Very basic demos that show how **deterministic agents use TF/UFA semantic capabilities**. 
- 1 Basic tool
- 3 Filesystem
- 5 RAG
- 6c MCP + LLM tool choice. 

<br>

### [3.2.5 PAL demos](/3.2.5-ai-agent-pal-demos/)

<!-- Simple demos are the best way to understand agentic AI systems. -->

PAL (Palantir) demos focus on:
- ontology systems
- semantic workflows
- deterministic execution
- LLM-assisted planning
- structured outputs
- external orchestration

<br>



<!-- 
### **[3.3 Agentic AI projects](/3.3-ai-projects/)** (full demo projects (WIP) with Github repo and docs)

"Spinning up" real-world projects quickly with minimal code analysis or manual coding. 

<br> 

-->

26.0614 (0524)

<br>

-------------------------------
-----------------------------
------------------
---------------------

<br>


#### **from "qs" 26.0615**
The center of the Agentic AI universe is the AI agent. 

<img src="/assets/0_projects2.png" alt="drones" width="35%"> 

The agent and LLM together can doing amazing things. But they also have severe limitations. "Tuning" then to work together is the core focus. 

<img src="/assets/readfile3.png" alt="drones" width="60%" style="border: 1px solid black;">





<!--
- **[3 Agents](/3_agents/)** (the focus of this site). Concepts and demos for
  - [3.1 Agentic (no AI)](/3.1-agentic/), 
  - [3.2.4 Agentic + AI (basic)](/3.2.4-ai-agent-basic-demos/), 
  - [3.2.5 Agentic + AI (basic Palantir-style)](3.2.5-ai-agent-pal-demos/), and 
  - **[3.3 Agentic + AI (real-world projects)](/3.3-ai-projects/)** (the end goal of this site). 
-->

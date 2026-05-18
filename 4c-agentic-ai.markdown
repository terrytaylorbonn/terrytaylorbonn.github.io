---
layout: page
title: "3.2 (4c) Agents + AI"
permalink: /4c-agentic-ai/
---

<br>

*TOC NEW (WIP; I am reorganizing 26.0518-19) See [#606_ai_ides_.docx (on Gdrive)](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO) chapters "Agentic AI DEMOS" and "3.2 Agents + AI" for content to be add to these pages.*


<br>

**Conceptual summary**: The core control loop is traditional non-AI deterministic programming that performs (with the help of an LLM) for example:
- Input and output (of “messy” human language representations)
- Task planning (breaking up complex human language tasks into smaller deterministic tasks)
- Rule injection (by AI into the main loop)


<br>

### [3.2.1 Intro](/3.2-ag-ai-1-intro/)
Just like iAgent and TF work together, so **must extAgent and LLM work together**.
- 1 Agents existed long before AI
- 2 Agentic AI (LLMs designed for agents)
- 3 AI'ic agents
- 4 Model interface layer (MIL)

<br>

### [3.2.2 Diagrams](/3.2-ag-ai-2-diagrams/)
Core diagrams (my own) that explain the core concepts.
- 2.1 Ecosystem
- 2.2 Agent <> LLM interface
- 2.3 Workflow diagram / simple
- 2.4 Workflow diagram / detailed

<br>

### [3.2.3 Agentic AI functionality](/3.2-ag-ai-3-ag-ai-func/)
It was only realistically possible for an agent (Python script, etc) to send prompts and receive response **after AI became agentic**:
- LLMs provided API support
- LLMs could process agent messages reliably
- and send messages with content and format as specified in the prompts

<br>

### [3.2.4 AI'ic agents functionality](/3.2-ag-ai-4-ai-ag-func/)
Agents likewise required new commands that made them **"agents with AI support"**.
- Connect to LLM
- Send prompts and process responses

*The term "AI-ic agents" is my own. I chose it for several reasons: 
- (1) Agents need AI support, 
- (2) the awkward formulation reminds us of the limitation of human language (that we are bound to and LLMs must process), and 
- (3) its a very short term that accurately (and clearly) defines the meaning ("agentic AI" does not).

<br>

### [3.2.5 AI'ic agents demos](/3.2-ag-ai-5-ai-ag-demos/)
Very basic demos that show how **agents perform basic AI tasks with an LLM** (GPT API). Code on GIT.
- 1 Basic tool
- 3 Filesystem
- 5 RAG
- 6c MCP

<br>

### [3.2.6 PAL demos](/3.2-ag-ai-6-pal-demos/)

Simple demos are the best way to understand the core of agentic+AI apps. For details see the lab notes doc **#603\_PAL\_.docx** (PAL = Palantir) on my **[Gdrive](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**.  

<br>

*Notes: [4a chat about iAgent and eAgent](/4a-chat-about-iAgent-and-eAgent/) 26.0514*

<!-- #### **[4c.3 Agent <-> LLM functional overview](/4c.3-agent-llm-func-overview/) (temp working file)** -->

<br>


26.0518
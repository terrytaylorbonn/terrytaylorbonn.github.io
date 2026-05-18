---
layout: page
title: "3.2 (4c) Agents + AI"
permalink: /4c-agentic-ai/
---



<!-- *TOC NEW (WIP; I am reorganizing 26.0518-19) See [#606_ai_ides_.docx (on Gdrive)](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO) chapters "Agentic AI DEMOS" and "3.2 Agents + AI" for content to be added to these pages.* -->


<br>

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

### [3.2.1 Intro](/3.2-ag-ai-1-intro/)
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

### [3.2.2 Diagrams](/3.2-ag-ai-2-diagrams/)
Core diagrams (my own) that explain the architecture.
- 1 Ecosystem
- 2 extAgent <> LLM interface
- 3 Workflow diagram / simple
- 4 Workflow diagram / detailed

<br>

### [3.2.3 Agentic AI (TF/UFA semantic) functionality](/3.2-ag-ai-3-ag-ai-func/)

It was only realistically possible for an agent (Python script, etc) to send prompts and receive response **after AI became agentic**, after LLMs were able to reliably  
- process incoming human language agent messages and 
- respond with the requested content and format constraints (as specified in the prompts)

**Modern TF/UFA systems provide semantic capabilities that made practical agentic systems possible**. These systems can
- A. **Comprehend, remember** (Generalization / approximation, Context tracking, Semantic abstraction, Human-language robustness)
- B. **Explain** (Ontology alignment / normalization, Explanation / summarization)
- C. **Deduce, plan** (Structured constrained outputs, Semantic interpretation / inference, Hierarchical planning / workflow synthesis)


<br>

### [3.2.4 AI infrastructure / helpers](/3.2-ag-ai-4-ai-ag-func/)
**Agents likewise required external orchestration layers that augment the TF/UFA semantic engine capabilities** (such as Tools, Filesystem access, RAG,MCP, APIs, and Workflow orchestration).

<!-- new commands that made them **"agents with AI support"**.
- Connect to LLM
- Send prompts and process responses
*The term "AI-ic agents" is my own. I chose it for several reasons: 
- (1) Agents need AI support, 
- (2) the awkward formulation reminds us of the limitation of human language (that we are bound to and LLMs must process), and 
- (3) its a very short term that accurately (and clearly) defines the meaning ("agentic AI" does not). -->

<br>

### [3.2.5 AI'ic agent demos](/3.2-ag-ai-5-ai-ag-demos/)
Very basic demos that show how **deterministic agents use TF/UFA semantic capabilities). 
- 1 Basic tool
- 3 Filesystem
- 5 RAG
- 6c MCP + LLM tool choice. 

Code on GitHub. More demos to follow soon.


<br>

### [3.2.6 PAL demos](/3.2-ag-ai-6-pal-demos/)

Simple demos are the best way to understand agentic AI systems.

PAL demos focus on:
- ontology systems
- semantic workflows
- deterministic execution
- LLM-assisted planning
- structured outputs
- external orchestration

For details see the lab notes docx **#603\_PAL\_.docx** on the **[Gdrive](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**.  

<br>

*Notes: [4a chat about iAgent and eAgent](/4a-chat-about-iAgent-and-eAgent/) 26.0514*

<!-- #### **[4c.3 Agent <-> LLM functional overview](/4c.3-agent-llm-func-overview/) (temp working file)** -->

<br>


26.0518
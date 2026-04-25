---
layout: page
title: "(4) Agentic AI"
permalink: /agentic-ai/
---

<br>

See the [Wiki page](https://github.com/terrytaylorbonn/auxdrone/wiki/Agentic-AI) for more info.

<br>

#### 1) Demos are the best way to learn agentic AI

A typical definition of agentic AI would be "systems that plan, reason, and act autonomously to achieve goals." The only way you can decipher such a statement is if you have hands-on experience. The wiki page [Agentic AI demos](https://github.com/terrytaylorbonn/auxdrone/wiki/4%E2%80%902-Agentic-AI-demos) provides a very structured set of detailed demos of core concepts. 

<br>

#### 2) All LLMs have an internal agent

The LLM has 2 main components:

1. A transformer (TF) that performs GPU-based computing to analyze human language input (a prompt) to determine what the output (response) should be. The TF is simply input/output (no loop).
2. An internal agent ("iAgent", a deterministic CPU-based program) that interfaces between the TF and the outside world. This internal agent is the central control loop that manages complex tasks such as conversation history, structure, user interface, etc.

<br>

#### 3) "Agentic AI" refers to an external (to the LLM) agent

This program is the central loop of the entire application in which the LLM plays a supportive ("helpful assistant") role.

![Agentic AI ecosystem](/assets/ecosystem.png)

The (external) agent performs the following functions (sometimes with the assistance of the LLM): 
- Data integration and analytics
- Tools (function calling, APIs, external integrations)
- Workflows (multi-step agent pipelines, orchestration)
- Planning systems (task decomposition, ReAct, chain-of-thought)"

<br>

#### 4) My focus on Palantir agentic AI

Palantir is a well known company with a very successful line of products. Palantir was founded in 2003 with early backing from the CIA — when there was no AI as we understand it today. Palantir was founded (with government backing) to prevent events like 9/11 by connecting data points to detect hidden threats. There were warning signs for 9/11 (foreign nationals wanting to learn to fly airliners on simulators). But collecting and analyzing such signals back then required a lot of manpower. Palantir's tools are nowadays being used in many other business segments (other than defense). 

Only relatively recently has AI played a major (useful assistant) role in Palatir's products. Palantir's AIP (Artificial Intelligence Platform) "enables organizations to securely deploy Large Language Models (LLMs) and artificial intelligence within their private networks, connecting generative AI directly to operational data (the Ontology) and workflows. It allows users to automate tasks, generate insights, and take action securely across various sectors."

AIP probably offers a set of functionality similar to the following:
- **Standardization of "messy" inputs**. AI creates outputs with specific structures and data types. 
- **Planning.** AI breaks up a "messy" plan into a set of standard subtasks that can be verified.
- **Rule injection.** AI can add "rule" keywords to the list of keywords used by the deterministic agentic loop to modify the execution logic.

<br>

*Diagram from Substack post [#75 The Real Job of AI in Enterprise Apps](https://ziptieai.substack.com/p/75-the-real-job-of-ai-in-enterprise) shows how AI is only used to generate a plan ("08b AI")*

<img src="/assets/aiplan.png" alt="AI planning" width="85%">

<br>

#### 5) Lessons learned from the demos


Very "basic" demos of such functionality are listed on the wiki page [Agentic AI demos](https://github.com/terrytaylorbonn/auxdrone/wiki/4%E2%80%902-Agentic-AI-demos). Complete documentation with all the steps is on the Gdrive. The  goal of these very simple demos is to show basic core concepts that apply to AI systems of any size. For example:
- Palantir will not become [SkyNet](https://en.wikipedia.org/wiki/Skynet_(Terminator)). The central agent control loop is not AI-controlled and presses no buttons (humans are required).
- SW programming jobs will not disappear. Such systems require very capable product experts preferably with extensive SW experience. Programming is just becoming higher level. 


<!-- 
A few things you will notice if you do thOne of my major goals in studying AI has been to refute the hype (that I recognized early). The AI titans and gurus were feeding the public nonsense about how their inventions could think, have consciousness, have feelings, and even surpass human intelligence.

This is utter nonsense. All of an AI system (CPU and GPU based parts) are on the lowest level clocked binary circuits. This has absolutely nothing to do with the neurons in the human brain. AI tools cannot see, hear, sense touch, smell, have feelings, consciousness, or think. In short, they have no intelligence. -->





<br>

26.0425

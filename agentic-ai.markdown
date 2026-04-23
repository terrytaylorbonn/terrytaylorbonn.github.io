---
layout: page
title: "(4) Agentic AI"
permalink: /agentic-ai/
---

<br>

See the [Wiki page](https://github.com/terrytaylorbonn/auxdrone/wiki/Agentic-AI) for more info.

<br>

#### 1) The typical agentic AI blurb defining "agentic AI"

"Systems that plan, reason, and act autonomously to achieve goals." Good luck in figuring that one out. This page provides a better explanation. The best way to understand agentic AI is by doing demos. The wiki page [Agentic AI demos](https://github.com/terrytaylorbonn/auxdrone/wiki/4%E2%80%902-Agentic-AI-demos) shows hands-on demos.

<br>

#### 2) All LLMs have an internal agent

The LLM has 2 parts:

1. A **Transformer (TF)** that uses a vast amount of GPU-based computing to analyze human language input (prompt) to determine what the output should be (response). The TF has no loop — it is simply input/output.
2. An **internal deterministic (CPU) program** (an internal agent — iAgent) that connects the TF to the outside world. This internal agent is the central control loop that manages complex tasks such as conversation history, structure, user interface, etc. It is a traditional non-AI program using languages such as Python.

<br>

#### 3) "Agentic AI" means the external agent

What is typically meant by agentic AI is an external (to the LLM) CPU program. This program is the central loop of the entire application in which the LLM plays a supportive ("you are a helpful assistant") role.

![Agentic AI ecosystem](/assets/ecosystem.png)

Basically the external agent performs the following functions, with the assistance of the LLM. 
- Data integration and analytics
- Tools (function calling, APIs, external integrations)
- Workflows (multi-step agent pipelines, orchestration)
- Planning systems (task decomposition, ReAct, chain-of-thought)"

<br>

#### 4) Why my focus on Palantir for agentic AI

To really understand the list of agentic AI functions above, you need a demo system with specific goals. I chose Palantir for this role because Palantir recently got a lot of publicity for its very successful role in the Iran war. This recently publicity makes it easy to find recent information about its systems.

Buts its a company thats been around for more than a generation, and was created to solve a very complex and important problem ... before AI was a factor. This suggests that AI plays more of a supportive/assistant role.

Palantir was founded in 2003 with early backing from the CIA — when there was no AI as we understand it today. They wanted to prevent events like 9/11 by connecting data points to detect hidden threats. There were many warning signs for 9/11. Just before 9/11, all of a sudden there were Saudi nationals wanting to learn how to fly large airliners — something that had never happened before. It was a warning that should have been picked up by the CIA or other services. But they did not have the manpower to (1) collect and (2) analyze all possible activities all over America that might suggest something unusual was occurring.

<br>

#### 6) Palantir's central mission

Palantir's central mission is to detect hidden threats; it now focuses on "data-backed decision-making" for national security and industry. It does this through automation of (1) data gathering and (2) analysis. These are also core tasks in many other business segments. And these segments also need systems that generate intelligence from vasts amounts of data.

<br>

#### 7) The recent addition of AI

Only relatively recently has AI played a major (useful assistant) role. Palantir's AIP (Artificial Intelligence Platform) enables the use of AI in these systems. From Palantir: "AIP enables organizations to securely deploy Large Language Models (LLMs) and artificial intelligence within their private networks, connecting generative AI directly to operational data (the Ontology) and workflows. It allows users to automate tasks, generate insights, and take action securely across various sectors."

I would assume that AIP does the following:

- Provides an **MMI (man-machine interface)** that allows human language (HL; text, audio, etc) input/output.
- This makes possible the **ingress/egress of complex unpredictable data sources**. The LLM is used to standardize the format of these sources.
- **Planning.** An LLM can break up tasks into subtasks.
- **Rule injection.** A human can use HL to add new rules to the system agent workflows. The LLM does this by adding "rule" keywords to the list of keywords that the agentic loop is constantly using in searches.

All of these basic functions are demonstrated in the demos listed on the wiki page [Agentic AI demos](https://github.com/terrytaylorbonn/auxdrone/wiki/4%E2%80%902-Agentic-AI-demos). I don't have access to Palantir systems, but I did have GPT create (very simple) demos of Palantir core functions.

<br>

#### 8) Palantir will not become Skynet

One of my major goals in studying AI has been to refute the hype (that I recognized early). The AI titans and gurus were feeding the public nonsense about how their inventions could think, have consciousness, have feelings, and even surpass human intelligence.

This is utter nonsense. All of an AI system (CPU and GPU based parts) are on the lowest level clocked binary circuits. This has absolutely nothing to do with the neurons in the human brain. AI tools cannot see, hear, sense touch, smell, have feelings, consciousness, or think. In short, they have no intelligence.

This is important because once you understand this, you understand that it's impossible for such tools to become Skynet.

<br>

#### 9) Programming jobs will not disappear

The nature of programming has changed — it has become higher level. The gurus who tell us that we no longer need programmers know that what they are saying is nonsense. Profitable nonsense for them, if you don't understand the facts.


<br>

26.0423

---
layout: page
title: "(4) Agentic AI"
permalink: /agentic-ai/
---

See the [Wiki page](https://github.com/terrytaylorbonn/auxdrone/wiki/Agentic-AI) for more info.

---

#### 1) Agentic AI definition (GPT)

Agentic AI covers systems that plan, reason, and act autonomously to achieve goals.
Topics include:

- Palantir-style data integration and analytics platforms
- Tool use — function calling, APIs, external integrations
- Workflows — multi-step agent pipelines, orchestration
- Planning systems — task decomposition, ReAct, chain-of-thought

---

#### 2) The typical agentic AI blurb definition of "agentic AI"

"Systems that plan, reason, and act autonomously to achieve goals." Good luck in figuring that one out.

---

#### 3) All LLMs implement agentic AI internally

The LLM has 2 parts:

1. A **Transformer (TF)** that uses a vast amount of GPU-based computing to analyze human language input (prompt) to determine what the output should be (response). The TF has no loop — it is simply input/output.
2. An **internal deterministic (CPU) program** (an internal agent — iAgent) that connects the TF to the outside world. This internal agent is the central control loop that manages complex tasks such as conversation history, structure, user interface, etc. It is a traditional non-AI program using languages such as Python.

---

#### 4) The typical meaning

What agentic AI typically means is an external (to the LLM) CPU program. This program is the central loop of the entire application in which the LLM plays a supportive ("you are a helpful assistant") role.

![Agentic AI ecosystem](/assets/ecosystem.png)

The wiki page [Agentic AI demos](https://github.com/terrytaylorbonn/auxdrone/wiki/4%E2%80%902-Agentic-AI-demos) shows hands-on demos of this concept.

Palantir systems are extremely complex (and I have no hands-on experience with them). But you can be sure that in their core they work the same way.

---

#### 5) Palantir's mission

Palantir was founded in 2003 with early backing from the CIA — when there was no AI as we understand it today.

Why CIA? They wanted to prevent events like 9/11 by connecting data points to detect hidden threats. There were many warning signs for 9/11. Just before 9/11, all of a sudden there were Saudi nationals wanting to learn how to fly large airliners — something that had never happened before. It was a warning that should have been picked up by the CIA or other services. But they did not have the manpower to (1) collect and (2) analyze all possible activities all over America that might suggest something unusual was occurring.

---

#### 6) The Palantir solution

Automate (1) data gathering and (2) analysis. Palantir's central mission is to detect hidden threats; it now focuses on "data-backed decision-making" for national security and industry.

---

#### 7) The recent addition of AI

Only relatively recently has AI played a major (useful assistant) role. Palantir's AIP (Artificial Intelligence Platform) enables the use of AI in these systems.

From Palantir: "AIP enables organizations to securely deploy Large Language Models (LLMs) and artificial intelligence within their private networks, connecting generative AI directly to operational data (the Ontology) and workflows. It allows users to automate tasks, generate insights, and take action securely across various sectors."

I would assume that AIP does the following:

- Provides an MMI (man-machine interface) that allows human language (HL; text, audio, etc) input/output.
- This makes possible the ingress/egress of complex unpredictable data sources. The LLM is used to standardize the format of these sources.
- **Planning.** An LLM can break up tasks into subtasks.
- **Rule injection.** A human can use HL to add new rules to the system agent workflows. The LLM does this by adding "rule" keywords to the list of keywords that the agentic loop is constantly using in searches.

All of these basic functions are demonstrated in the demos listed on the wiki page [Agentic AI demos](https://github.com/terrytaylorbonn/auxdrone/wiki/4%E2%80%902-Agentic-AI-demos). I don't have access to Palantir systems, but I did have GPT create (very simple) demos of Palantir core functions.

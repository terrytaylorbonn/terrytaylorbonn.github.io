---
layout: page
title: "(2) LLMs"
permalink: /sandbox/
description: Last edit 26.0426
---

This page describes 
- **1 LLM stack demos**. I planned to spend a lot of time on this, but at some point came to the conclusion that time would be better spent elsewhere. In any case, knowing the basic is quite important. Its not that difficult to install a smaller model on your local PC, and it does have benefits.
- **2 LLM transformer (TF) training**. Training is something most of us will never do (Palantir uses standard models; they do no customized training). But its the main driving factor in the design of LLM transformers. 
- **3 LLM internal Agent**. A deterministic (non-AI, not GPU-based) control loop inside the LLM that is the interface between the LLM transformer (TF) and the outside (of the LLM) world.  
- **4 LLM (GPT-3) TF (transformer) algorithm**. Its a lot of work to grasp the entire algorithm, but a basic study of the major steps helps you to appreciate just how much computation is involved in GPT-3 generation of a single token (and GPT-3 much smaller than the latest models)

See also: 
  - **[Core AI (LLM) concepts](https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts)** (wiki page) explains in detail GPT-3 transformer algorithms. 
  - **[Core AI (LLM) misconceptions](/llm-tf-misconceptions/)** describes a chat that GPT and I had recently.



<br>

### 1 LLM stack demos

My focus at one point was on LLMs. I thought that that was going to be the market focus. There is a lot of value in being able to deploy and fine-tune your own LLMs, but for most of us these skills will not be used often. 

The wiki page [**"AI LLM stacks"**](https://github.com/terrytaylorbonn/auxdrone/wiki/AI-stacks) (a bit chaotic after a recent wiki reorganization) lists the following subpages are of interest:

- [2.2 Demo deployments (HF, CloudFlare, etc)](https://github.com/terrytaylorbonn/auxdrone/wiki/LLM-stacks-%5C-2-Demo-deployments)
- [2.3 Youtube demos](https://github.com/terrytaylorbonn/auxdrone/wiki/LLM-stacks-%5C-3-Youtube-demos). I did a lot of YouTube demos. Way back then (2025, a long time ago in AI-time) I had still not make the transition to working totally with LLMs (GPT) to learn new tech.
- [2.4 GPT/Copilot demos (a few demos)](https://github.com/terrytaylorbonn/auxdrone/wiki/LLM-stacks-%5C-4-CPLT-demos)
- [2.6 Agent/LLM input docs (RAG demo)](https://github.com/terrytaylorbonn/auxdrone/wiki/LLM-stacks-%5C-4-CPLT-%5C-4.0b-Platforms-and-tools)
 
<img src="/assets/smol.png" alt="smol" width="65%">


<br>

### 2 LLM transformer training (WIP, will add diagrams)

*See also [Core AI (LLM) misconceptions](/llm-tf-misconceptions/) (website page) describes a chat that GPT and I had recently that started off about training misconceptions.*


Training is something most of us will never do (Palantir uses standard models; they do no customized training). But its the second heading for a good reason: Training is the defining aspect of model transformer (TF) design (section 4 below describes GPT-3 TF design). 

Training is actually a complex programming process (it is not training in the human sense). Input data is fed through the TF, and the the TF internal parameters (weights and biases) are adjusted so that the output more closely matches the intended output. The input and required output are all taken from huge sets of human generated text. 

The main point is: No human does any of the programming. No human is deciding the values of weights and biases. Its all automated. And training can fail. Since its a neural network (NN), the neurons are all interconnected. When you change the value of a weight and/or bias (there are 175 billion of them in GPT-3), it can effect the input/output combinations you trained earlier. Its as much of an art than a science. 

This is important to understand for several reasons. (1) You appreciate that a TF is a universal function approximator (UFA). It can take an input combination that it was never trained on and (after a massive number of statistical calculations) compute the best matching output (based on its training). (2) The tradeoff is that the TF is approximating. That's why LLMs always warned you that they can make mistakes.

This, by the way, (3) has nothing to do with how human process language. Understanding this is not useless theory. Its vital for understanding what you can expect from AI in an application. This is why in Palanatir AI is a "helpful assitant", not the (a) central control loop or (b) the human who actually makes critical final decisions.  

<br>

### 3 LLM Internal Agent (WIP, will add diagrams)

The term "agent" normally means a deterministic (non-AI, not GPU-based) control loop that is the "caretaker" or interface between the LLM model and the outside world. However, there is also an agent (what I call an internal agent or "iAgent") in the LLM that is the interface between the transformer (TF) and the outside (of the LLM) world. Again, as with training, understanding this helps to understand the core nature of what an LLM and an agent is. An (external) agent is to some extent just an extension or a partner of the internal agent. 

<br>

### 4 LLM (GPT-3) TF (transformer) algorithm (WIP; need to add text for #1-#9)

The following shows selected screenshots from the wiki page [**Core AI concepts**](https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts). These diagram are my own, and depict my interpretation of the GPT-3 algorithm. Its much more complex than what these few diagrams depict. But it gives you an appreciation of the vast complexity of TF calculations.

#1 The main TF loop generates tokens.

<img src="/assets/llm01_tokens.png" alt="01" width="40%">

#2

<img src="/assets/llm02_tf123.png" alt="02" width="45%">

#3

<img src="/assets/llm03_tfs1s6.png" alt="03" width="45%">

#4

<img src="/assets/llm04_tfahinfomix.png" alt="04" width="25%">

#5 "Neurons" in the FFN

<img src="/assets/llm05_tfffnneurons.png" alt="05" width="25%">

#6 An example of matrix math

<img src="/assets/llm06_tfhlayerdetection.png" alt="06" width="50%">

#7 How complex logic (for detection) is implemented in the FFN

<img src="/assets/llm07_tfxor.png" alt="07" width="50%">

#8 

<img src="/assets/llm08_tfh1h2.png" alt="08" width="45%">

#9 A simplified diagram of how the hidden layers evolve over time

<img src="/assets/llm09_tffinalstate.png" alt="09" width="45%">
 


<br>

26.0426

<!-- 
25.0310b ([Doc URLs](https://github.com/terrytaylorbonn/auxdrone/wiki/Main-doc-deployments)) ([Stack URLs](https://github.com/terrytaylorbonn/auxdrone/wiki/Stack-deployments)) ([Lab notes (Gdrive)](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)) ([Git](https://github.com/terrytaylorbonn?tab=repositories)) -->


<!--
The main goals of the AI/tech stack sandbox are

- [Deployments](https://github.com/terrytaylorbonn/auxdrone/wiki/Deployments)
  - [Stacks](https://github.com/terrytaylorbonn/auxdrone/wiki/Stack-deployments) (with APIs and API-docs (Swagger/GraphiQL))
  - [Docs](https://github.com/terrytaylorbonn/auxdrone/wiki/Main-doc-deployments) including: 
    - 4.1 [Websites](https://github.com/terrytaylorbonn/auxdrone/wiki/Website-deployments)
    - 4.2 [API docs](https://github.com/terrytaylorbonn/auxdrone/wiki/API-doc-deployments)
    - 4.4 [AI docs: CHAT](https://github.com/terrytaylorbonn/auxdrone/wiki/AI-docs) 
    - 4.3 [AI docs: REASON-GEN](https://github.com/terrytaylorbonn/auxdrone/wiki/AI-docs-reasoning-generate)
    - 4.6 [AI test/maintenance](https://github.com/terrytaylorbonn/auxdrone/wiki/AI-test-maintain)


- Sandbox lab notes 
  - [Gdrive](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)
  - Wiki pages
    - [2 Stacks/frameworks](https://github.com/terrytaylorbonn/auxdrone/wiki/2-Stacks-and-frameworks)
    - [1 APIs/API-docs](https://github.com/terrytaylorbonn/auxdrone/wiki/1-APIs-and-API-docs) 
    - [3 Deployment](https://github.com/terrytaylorbonn/auxdrone/wiki/3-Deployment) (Render, etc)
    - [4 Non-stack SITES/DOCS/AI](https://github.com/terrytaylorbonn/auxdrone/wiki/4-Doc-sites)
    - [5 API management](https://github.com/terrytaylorbonn/auxdrone/wiki/5-API-management)

 - Hands-on experience with a wide range of tools -->

<!-- ![image](https://github.com/user-attachments/assets/187576ca-6ca9-41cc-9629-39a0db97581c) -->



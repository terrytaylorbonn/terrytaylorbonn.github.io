---
layout: page
title: "(2) LLMs"
permalink: /sandbox/
description: Last edit 25.0715
---

This page describes 
- **LLM stack demos**. I planned to spend a lot of time on this, but at some point came to the conclusion that time would be better spent elsewhere. In any case, knowing the basic is quite important. Its not that difficult to install a smaller model on your local PC, and it does have benefits.
- **LLM (GPT-3) TF (transformer) algorithm**. Its a lot of work to grasp the entire algorithm, but a basic study of the major steps helps you to appreciate just how much computation is involved in GPT-3 generation of a single token (and GPT-3 much smaller than the latest models)

<br>

### LLM stack demos

My focus at one point was on LLMs. I thought that that was going to be the market focus. There is a lot of value in being able to deploy and fine-tune your own LLMs, but for most of us these skills will not be used often. 

The wiki page [**"AI LLM stacks"**](https://github.com/terrytaylorbonn/auxdrone/wiki/AI-stacks) is bit chaotic (I reorganized the wiki and moved a lot of the TOC entries into the wiki page). For LLMs the following wiki subpages are of interest:

- [2.2 Demo deployments (HF, CloudFlare, etc)](https://github.com/terrytaylorbonn/auxdrone/wiki/LLM-stacks-%5C-2-Demo-deployments)
- [2.3 Youtube demos](https://github.com/terrytaylorbonn/auxdrone/wiki/LLM-stacks-%5C-3-Youtube-demos). I did a lot of YouTube demos. Way back then (2025, a long time ago in AI-time) I had still not make the transition to working totally with LLMs (GPT) to learn new tech.
- [2.4 GPT/Copilot demos (a few demos)](https://github.com/terrytaylorbonn/auxdrone/wiki/LLM-stacks-%5C-4-CPLT-demos)
- [2.6 Agent/LLM input docs (RAG demo)](https://github.com/terrytaylorbonn/auxdrone/wiki/LLM-stacks-%5C-4-CPLT-%5C-4.0b-Platforms-and-tools)
 
![Smol](/assets/smol.png)

<br>


### LLM (GPT-3) TF (transformer) algorithm

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

26.0425

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



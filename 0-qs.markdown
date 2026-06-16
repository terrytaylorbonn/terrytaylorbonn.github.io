---
layout: page
title: QS
permalink: /0-qs/
---

<br> 

<!-- 
**The ONLY way to understand AI is by doing examples.** This page currently is an overview of all the demos on this site. But it will slowly morph into a Quick Start with specific demos to focus on. 

**TOC**
- **1 Master diagram**
- **2 NN demos**
- **2b Model demos**
- **3 Agent demos**
- **3b Projects**  -->

This QS (quick start) follows the organization of this site as shown in the site "master diagram" (below).
- **2 NN, CNN, TF**
  - **Core NN (CNN dense, TF FFN)** is the core NN in all demos (except agent only demos with no AI).
  - **CNN convolute, TF QKV (context)** is an extra NN in CNNs and LLM transformers (TFs).
  - Note that these run (normally) on a GPU. But they run on a CPU.
  - These NNs only know FP numbers as input and output. So if you have any type of other data, you must encode and then decode.
- **2b Model**
  - Contains the **NNs** and an **"internal" agent (iAgent)** that has sole access to the NN. iAgent and NNs **only** communicate with tokens.
  - iAgent often implements an **API** that allows external access.
- **3 External agent (py script)** uses the model as a helful assistant.
- **3b Project** usually provides integrates AI into existing digital infrastructure.

Note that **there are many variations of this setup**, and I will try to provide the version of this diagram for each demo (v1 of this diagram created 26.0615).

*Master diagram*<br>
<img src="/assets/M-15.png" alt="drones" width="78%">

*Note: Old demos are available on [Wiki](https://github.com/terrytaylorbonn/auxdrone/wiki), [Github](https://github.com/terrytaylorbonn?tab=repositories), [Gdrive](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO) (docx lab notes).*



<br>

### **[2 NN demos](/2_models/)**

- **[2.1 Core NNs (dense/FF)](/2.1-predictive-nns/)**. Basic neural network demos.<br>
<img src="/assets/classification.png" alt="drones" width="15%"><br> <br> 
- **[2.2 CNNs (convolution)](/2.2-cnns/).**<br>
<img src="/assets/d4_alexnet.png" alt="drones" width="12%" style="border: 1px solid black;"><br> <br> 
- **[2.3.6 Transformers](/2.3.6-llm-demos/).**<br>
<img src="/assets/d5_0.png" alt="drones" width="32%"><br> <br> 
- **2.5 Robotic AI ([wiki](https://github.com/terrytaylorbonn/auxdrone/wiki/Robotic-AI-demos))**<br>
<img src="/assets/robotic_ai.png" alt="smol" width="25%" style="border: 1px solid black;"><br> 

<br>

### **[2b Model demos](/2b_models/)**

- ([2b.1b 2025 demos](/2b.1b-2025-llm-demos/))<br><img src="/assets/smol.png" alt="smol" width="35%"><br> <br>
- **[2b.2 Tiny demos](/2b.3.6-llm-demos/)**<br> <br>
- **[2b.2b Building models](/2b.2b-build-models/)**<br> <br>
- **[2b.3 Modifying models](/2b.3-modify-models/)**<br> <br>
- **[2b.4 Running models locally](/2b.4-run-models-locally/)**<br> <br>

<br>

### **[3 Agent demos](/3_agents/)**

The center of the Agentic AI universe is the AI agent.  The agent and LLM together can doing amazing things. But they also have severe limitations. "Tuning" then to work together is the core focus. 

- **[3.1 Agentic (no AI)](/3.1-agentic/)** <br> 
<img src="/assets/4_5_3x.png" alt="drones" width="20%"> <br><br>
- **[3.2.4 Agentic + AI / Basic demos](/3.2.4-ai-agent-basic-demos/)**. <br>
<img src="/assets/calc1b.png" alt="drones" width="35%"> <br><br>
- **[3.2.5 Agentic + AI / PAL demos](/3.2.5-ai-agent-pal-demos/)**.   <br>
<img src="/assets/4_6_2x.png" alt="drones" width="20%">  <br>
<img src="/assets/4_5_3x_bbb.png" alt="drones" width="20%"><br><br> 

<br>

### **[3b Projects](/3.3-ai-projects/)**

This section focuses on "spinning up" real-world projects quickly with minimal code analysis or manual coding. 

<img src="/assets/6_main_diagram.png" alt="drones" width="40%"> 


<br>

26.0616 (v1 26.0527)


<!-- **I wasted so much time going down so many rabbit holes when studying AI**. AI is an awesome technology. Without AI tools (GPT) I never could have accomplished 5% of what I have done on the ZiptieAI project. But **AI chatbots only produce the output they are programmed to produce, and much of that about AI itself is misleading hype (or outright lies)**. The very term "artificial intelligence" is a perfect example. AI is not intelligent, and the very concept of "man-made" intelligence shows a basic lack of understanding of what intelligence is. 

**Code does not lie**. Do this QS and see for yourself what AI really is. Then go to the **[concepts section](/0b-demos/)** to get a firm conceptual grasp of the big picture. You need to do the QS first because otherwise you will struggle greatly to understand much of the **AI lingo (which can be quite misleading)**.
-->

<!-- **Studying code for basic AI demos** (NNs, CNNs, LLMs, etc) is the **only way to really understand AI** (and AI hype). And its **not that difficult** nowadays, because AI tools (GPT, Sonnet, etc) do all the difficult coding and debugging for you. But **you have to supply the right prompts**. 

- **1 Drone demos**
 -->

 
<!-- 
### **1 [Drone demos](/1-drones/)**

This site does not really focus on drones anymore. But I include it because it was the first project I did where I used AI (object recogntion). Note that drones dont need AI to fly (like cars need AI to drive on roads). 

*My AI drone build*<br>
<img src="/assets/airborne2.png" alt="drones" width="40%"> <img src="/assets/6cjnano.png" alt="6c" width="23%"> 

<br>
-->

<!-- *AlexNet CNN (left) and LLM transformer (right)*<br>
<img src="/assets/cnn2.png" alt="desc" width="35%">  <img src="/assets/tf_S1-S6.png" alt="desc" width="40%"> -->


<!-- <img src="/assets/0_projects2.png" alt="drones" width="35%"> -->

<!-- <img src="/assets/readfile3.png" alt="drones" width="60%" style="border: 1px solid black;"> -->

<!-- - **[3.3 Agentic AI projects](/3.3-ai-projects/)**. Complete business segment projects (main long-term focus).<br> 
<img src="/assets/6_main_diagram.png" alt="drones" width="25%"> <br><br>
-->


<!-- <img src="/assets/lucius.png" alt="drones" width="55%"> -->

<!-- This page will be a list of demos. Basically a start to finish AI/agents course.

<img src="/assets/classification.png" alt="drones" width="20%"> 

I often see Facebook ads about learning AI. They promise you will **understand AI in 30 days spending only 15 minutes a day studying** (some courses are even better; they only require 10 minutes a day). I ain't smart enough to create such a course. Or a course that demos the "intelligence" of AI. Unfortunately I also **ain't smart enough to make such demos that require no programming skill**. The great AI gurus and AI titans promised us that programming skills would go away (they are even smarter than those folks making the Facebook ads). 

My demos are **mechanistic**, because that's what AI tools are: **Binary, deterministic, mechanistic.** 

-->

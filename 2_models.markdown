---
layout: page
title: "2 Models"
permalink: /2_models/
---

<br>

- [(2) UFAs](/UFAs/)
- [(3.1) CNNs](/cnn/)
- [(3.2) LLMs](/sandbox/)
- [(3.3) Predictive](/2b-6-predictive/)
- [(3.4) Robotic AI](/robotic-ai/)


<br> <br> <br> <br> <br> 


------------------------
--------------------------
-----------------------
--------------------------

<br> 
*TODO: integrate this text from other pages*


The following 2 pages explain **the core of how AI really works** (especially (2b)):
- **[(2) LLMs](/sandbox/)**. An LLM consists of an (1) internal agent and a (2) transformer (TF). The TF is the core computational engine behind modern AI systems and the mechanism that enables modern LLM behavior.
  - [Core AI (LLM) concepts](https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts) (wiki page) explains in detail GPT-3 transformer algorithms. 
  - [Core AI (LLM) misconceptions](/llm-tf-misconceptions/).
  - [Core AI CNN (object recognition) concepts](/cnn/)
- **[(2b) UFAs](/UFAs/)**. A TF implements a Univeral Function Approximator (UFA) algorithm. Understanding what a UFA is is the key to understanding what AI really is. And **when you understand how AI really works,  you will understand why agentic AI works in systems like Palantir Maven (and in many many other business segments), but will never be safe enough for self-driving cars and home humanoids**. That's my personal opinion (backed up by over a decade of empty self-driving car promises). 
- [(3) Robotic AI](/robotic-ai/). JEPA, belief tracking, control loops, autonomy.

<!-- - **[(2b) UFAs](/UFAs/)**. Univeral function approximator. **Understanding UFAs is the key to truly understanding AI.**   
- **[(2) LLMs](/sandbox/)**. Local and API-based LLMs, transformers, RAG, MCP, tools, fine-tuning, and AI app design. See also: -->



*How a UFA determines if a location is in the Netherlands or Belgium*.<br>
<img src="/assets/belgium1.png" alt="drones" width="75%"> 

<br>

### **AI models**

**UFAs**. xxxxx xxxx xxxxxxxxxx

**[CNNs](https://ziptieai.com/cnn/)**. The AI in the AI drones was object recognition using CNNs (convoluted neural networks) running on the Nvidia Jetson Nano and on the PI computer. **Studying CNNs is a good first step for studying the much more complex LLMs.** Note: **"My depiction"** below means I have not seen such a diagram elsewhere.

**(2) [LLMs](/sandbox/)**. After understanding the gist of CNNs, **my focus shifted to LLMs (large language models)**:
  - Transformers (TF, the LLM neural network) *(see the wiki page **[AI concepts](https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts)** for **my explanation of GPT-3 transformer algorithms)*** 
  - API-based model usage (major frontier models)
  - Fine-tuning
  - RAG, MCP, and tools
  - Local and remote model deployment (smaller models)


**My goal was to understand** the core concepts, how to build practical applications, and (perhaps most of all) **the AI hype** (claims that AI has real intelligence, AI actually thinks, AI can learn, AI will soon surpass human intelligence, etc etc). The first diagram below shows the TF is nothing but a token sequence generator. That's it. The iAgent (internal agent) is deterministic (python style) code. No intelligence anywhere. It took me months of filtering out the endless hype to figure this out. 

That may seem impossible when you use an LLM that can intelligenty converse with you. But **the LLM intelligence simulation is based on (1) massive computing power and speed and (2) very basic binary computing structures**. The PC does the same trick. 


#### (3) [Robotic AI](/robotic-ai/)

When I first heard Yan LeCun's talks about how JEPA would provide real robotic intelligence I was fascinated. I totally agreed with what he said about the limitations of LLMs, and he was one of the very few gurus actually saying such things. But after doing a lot of hands-on JEPA (and robotics) demos, **I came to the conclusion that LeCun's version of JEPA was a lot of hype**. What he was selling was not fundamentally different from LLMs. GPT agreed.

Yan was claiming that what he would build would give machines real intelligence. It won't. They may be harmless for chatbots, but **AI robot "hallucinations" could be catastrophic** (especially for robots around humans, such as cars and humanoids).

In any case, the time spent doing hands-on demos (for representational learning, prediction-based systems, belief tracking, control loops, planning under uncertainty, etc) was well spent. Many of the concepts (such as estimation and autonomy) were related to earlier drone work.



***My depiction** of how the AlexNet CNN works*<br>
<img src="/assets/cnn2.png" alt="desc" width="40%"> 


***My depiction** of the main loop of an LLM transformer (GPT-3)*<br> 
<img src="/assets/tf_S1-S6.png" alt="desc" width="50%"> 

<br>

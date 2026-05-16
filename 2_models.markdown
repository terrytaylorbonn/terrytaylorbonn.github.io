---
layout: page
title: "2 Models"
permalink: /2_models/
---

<br>

**Goals of this section:** 
- Convey the core concepts of models (my take), 
- show how to build practical applications (demos), 
- and to dispel AI hype.

That last point is essential for successful AI projects. **Models run on clocked binary circuits**. They no intelligence. You could run LLMs on electro-mechanical relays (it would take years to generate a token, but it theoretically possible). **LLM intelligence simulation is based on (1) binary computing structures and (2) massive computing power/speed**. The more you understand how LLMs work, the better you can use them in AI projects. 


<br>

**Conceptual summary of models**:
- **2.X Gist of LLMs** is that they (1) convert prompt+response input tokens into large (12288) vector language (just set of FP numbers), (2) massive calculations are performed on the VL to determine the complete meaning of the input, and (3) select a new vocab token. **The algoritm of LLM inference is the mirror image of the algorithm used to program ("train") the LLM.**
- **2.0 UFA** (universal function approximator) is the core of AI. **A UFA only knows numbers. It has absolutely no info about the real world.** It is trained to output a number(s) based on the input numbers. 
- **2.1 CNN UFA** computes the most probable label for a set of pixels.
- **2.3 Predictive** and **2.4 Robotic** UFAs can often be small and locally trained.
- **2.2 LLM transformer (TF) UFA** generates the probabilities of all vocabulary token candidates for next token (a set of numbers) from the token sequence input.  



<!-- 

That last point is essential for successful AI projects. I first took an interest in understanding the core of **what makes models tick** when I started hearing all the hype from AI gurus about how AI could really think and even have emotions. **Models run on ticking clocked binary circuits**. You don't have to be very bright to understand that ticking mechanisms (clocked state machines) dont think. That may seem impossible when you use an LLM that can intelligenty converse with you. But **LLM intelligence simulation is based on (1) binary computing structures and (2) massive computing power/speed**. Your PC does the same kind of trick.

-->

<br>

### **[2.X Qualitative gist of language models (LLMs)](/gist-LLM/)**

Describes in concise detail gist of what an LLM model does without describing complex algorithms or architectures. 

<br>


### [2.0 UFAs](/UFAs/)

A TF implements a Univeral Function Approximator (UFA) algorithm. Understanding what a UFA is is the key to understanding what AI really is. And **when you understand how AI really works,  you will understand why agentic AI works in systems like Palantir Maven (and in many many other business segments), but will never be safe enough for self-driving cars and home humanoids**. That's my personal opinion (backed up by over a decade of empty self-driving car promises). 

<br>

### [2.1 CNNs](/cnn/)

The AI in the AI drones was object recognition using CNNs (convoluted neural networks) running on the Nvidia Jetson Nano and on the PI computer. **Studying CNNs is a good first step for studying the much more complex LLMs.** Note: **"My depiction"** below means I have not seen such a diagram elsewhere.

<br>

### [2.3 Predictive](/2b-6-predictive/)

<br>

### [2.4 Robotic AI](/robotic-ai/)

JEPA, belief tracking, control loops, autonomy.

When I first heard Yan LeCun's talks about how JEPA would provide real robotic intelligence I was fascinated. I totally agreed with what he said about the limitations of LLMs, and he was one of the very few gurus actually saying such things. But after doing a lot of hands-on JEPA (and robotics) demos, **I came to the conclusion that LeCun's version of JEPA was a lot of hype**. What he was selling was not fundamentally different from LLMs. GPT agreed.

Yan was claiming that what he would build would give machines real intelligence. It won't. They may be harmless for chatbots, but **AI robot "hallucinations" could be catastrophic** (especially for robots around humans, such as cars and humanoids).

In any case, the time spent doing hands-on demos (for representational learning, prediction-based systems, belief tracking, control loops, planning under uncertainty, etc) was well spent. Many of the concepts (such as estimation and autonomy) were related to earlier drone work.

<br>

<!-- *How a UFA determines if a location is in the Netherlands or Belgium*.<br>
<img src="/assets/belgium1.png" alt="drones" width="75%"> 

<br> -->


### [2.2 LLMs](/sandbox/) (iAgent + TF)

After understanding the gist of CNNs, **my focus shifted to LLMs (large language models)**:
  - Transformers (TF, the LLM neural network) *(see the wiki page **[AI concepts](https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts)** for **my explanation of GPT-3 transformer algorithms)*** 
  - API-based model usage (major frontier models)
  - Fine-tuning
  - RAG, MCP, and tools
  - Local and remote model deployment (smaller models)

An LLM consists of an (1) internal agent and a (2) transformer (TF). The TF is the core computational engine behind modern AI systems and the mechanism that enables modern LLM behavior.
  - [Core AI (LLM) concepts](https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts) (wiki page) explains in detail GPT-3 transformer algorithms. 
  - [Core AI (LLM) misconceptions](/llm-tf-misconceptions/).
  - [Core AI CNN (object recognition) concepts](/cnn/)

<br>


<!-- 

***My depiction** of how the AlexNet CNN works*<br>
<img src="/assets/cnn2.png" alt="desc" width="40%"> 


***My depiction** of the main loop of an LLM transformer (GPT-3)*<br> 
<img src="/assets/tf_S1-S6.png" alt="desc" width="50%"> 

-->

26.0516

---
layout: page
title: "2 AI (models)"
permalink: /2_models/
---

<br> 

-----------------

<br>

## Concepts

<br>

**A "model" in this section is anything that has a neural network (NN) at its core**. It may a lot of other stuff wrapped around it (for CNNs convolution, for LLMs Attention heads, etc) but **the core pattern matching and statistical probability runs on the NN**. The differences are mainly architecture, training, orchestration, and use case. **All models are first (1) trained** (internal NN params are SW programmed) and **then (2) used to infer output from input.**  

**Models ARE MECHANICAL. They run on clocked binary circuits**. They have no intelligence. You could run even the most sophisticated LLMs on electro-mechanical relays (it would take years to generate a token, but it theoretically possible). **AI intelligence simulation is based on (1) binary computing structures and (2) massive computing power/speed**. The more you understand how AI models work, the better you can use them in AI projects. 

Other sources about models (wiki pages):
- **[LLM transformer algorithm description](https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts#4-llm-transformer-tf)**
- **[LLMs in general](https://github.com/terrytaylorbonn/auxdrone/wiki/AI-stacks)**

<br>

*"2 Models" in the Agentic AI evolution ([diagram](/0.1-ai-evolution-diagram/))* <br>
<img src="/assets/zai_evolution6.png" alt="drones" width="50%">

<br>


### [2.0 NN UFA concepts](/2.0-ufas/)

The core of every model is the NN that implements a UFA (Univeral Function **Approximator**) that **generates an output based on pattern matching of the input**. The patterns were programmed ("trained") by setting NN parameters (weights and biases) during training.

<br>

-----------------

<br>

## 3 groups of models:
- 2.1 core (no convolution/tf) 
- 2.2 convolution
- 2.3 tf

3 phases of model demos for each model group:
- P1 DIY (doit yourself) models (phase1) understand mechanics
- P2 OTS (offtheshelf) models (phase2) 
- P2 OTS fine-tuned (phase3)


<br>

-----------------

<br>


### [2.1 Core NNs](/2.1-predictive-nns/)

Predictive NNs are small customized NNs for specific recognition tasks (if you create a DIY model, the first one will be something like a simple predictive NN).

<img src="/assets/brain1.png" alt="drones" width="14%">

<br>

### [2.2 CNNs (convolution)](/2.2-cnns/)

A CNN computes the most probable label ("dog", "airplane", etc) for a set of pixels. Studying CNNs is great preparation for studying more complex LLMs.

<img src="/assets/brain1a.png" alt="drones" width="17%">

<br>

### [2.3 LLMs (transformers)](/2.3-llms/) (iAgent + TF)

An LLM (1) inputs a sequence of tokens, (2) computes the probabilities of all vocabulary tokens as the next token, (3) outputs the selected new token, and finally (4) adds the new token to the next input sequence. An LLM consists of an (1) internal agent and a (2) transformer (TF) NN. The TF is the core computational engine behind modern AI systems and the mechanism that enables modern LLM behavior.

<img src="/assets/brain1b.png" alt="drones" width="22%">  <img src="/assets/brain1c.png" alt="drones" width="26%">


<br>


-----------------

<br>

## Robotic AI = future topic

*26.0526: This section does not really belong on this "2 Models" page, because this is not a different model type. I originally put it here because I believed LeCun's hype about his version of JEPA that would be a fundamentally different type of AI platform that would fix the fundamental limitations of LLMs (it doesnt, and never will). I might move this section somewhere else in the future. Right now this does not interest me too much... robotic AI (that claims to be able to do what humans can do) is about as realistic as FSD or colonizing Mars.*

*A Waymo "self-drives" into a flooded street.* <br>
<img src="/assets/waymo.png" alt="drones" width="26%"> 


### [2.5 Robotic AI](/2.5-robotic-ai/)

I spent a couple of months doing demos for basic robotic AI. I was intrigued by LeCun's claims about JEPA and his new venture that would basically go beyond the LLMs that were already becoming obsolete. After a few demos and chats with GPT, I felt like I had been scammed. 

Drone AI is something that works, because drones operate in very forgiving environments (in the air, far from other objects; actually they dont even need AI to fly, they need it for object recognition, terrain guidance, etc). But self-driving cars (robots) are another story. Its been over a decade of (empty) promises that FSD was just a year away. Its simply too dangerous for unintelligent robots to operate on complex and congested roadways. 

In any case, its inevitable that AI will pair up with humanoid robots in the home and workplace. Just like with agentic AI, there will be applications where the lack of any real intelligence can be tolerated. 

<br>

26.0526

<!-- *How a UFA determines if a location is in the Netherlands or Belgium*.<br>
<img src="/assets/belgium1.png" alt="drones" width="75%"> 
<br> -->
<!-- 
***My depiction** of how the AlexNet CNN works*<br>
<img src="/assets/cnn2.png" alt="desc" width="40%"> 
***My depiction** of the main loop of an LLM transformer (GPT-3)*<br> 
<img src="/assets/tf_S1-S6.png" alt="desc" width="50%"> 
-->
<!-- 
**TOC**:
- **2.0a Overview of model evolution**.
- **2.0b UFAs**. Basic UFA concepts. 
- **2.1 Predictive NNs** are small customized NNs for specific recognition task.  
- **2.2 CNNs** (object recognition). A CNN computes the most probable label ("dog", "airplane", etc) for a set of pixels. CNNs are great for your first deep dive into AI, because they are much more intuitive and simpler than LLMs.
- **2.3 LLMs** are the main focus of this site. An LLM generates the probabilities of all vocabulary token candidates for next token (a set of numbers) from the token sequence input.  
- **2.4 Agentic LLMs** are LLMs with extra functionality to support agentic AI.
- **2.5 Robotic NNs** (such as JEPA, LeCun's new projects, etc) are specifically for robots. **LeCun seems to generating a lot of hype**. I did some demos, lost interest for now in this.
-->
<!--
- **2.X Gist of LLMs** is that they (1) convert prompt+response input tokens into large (12288) vector language (just set of FP numbers), (2) massive calculations are performed on the VL to determine the complete meaning of the input, and (3) select a new vocab token. **The algoritm of LLM inference is the mirror image of the algorithm used to program ("train") the LLM.**
- **2.0 UFA** (universal function approximator) is the core of AI. **A UFA only knows numbers. It has absolutely no info about the real world.** It is trained to output a number(s) based on the input numbers. 
That last point is essential for successful AI projects. I first took an interest in understanding the core of **what makes models tick** when I started hearing all the hype from AI gurus about how AI could really think and even have emotions. **Models run on ticking clocked binary circuits**. You don't have to be very bright to understand that ticking mechanisms (clocked state machines) dont think. That may seem impossible when you use an LLM that can intelligenty converse with you. But **LLM intelligence simulation is based on (1) binary computing structures and (2) massive computing power/speed**. Your PC does the same kind of trick.
-->

<!-- 

- **2.1 predictive = basic NN**
- **2.2 CNN adds convolution**

<img src="/assets/brain1a.png" alt="drones" width="20%">

<br>

- **2.3 Chat LLM adds attention heads (extra stuff for language)**. This could be compared to adding grey matter in the brain.

<img src="/assets/brain1b.png" alt="drones" width="25%">

<br>

- **2.4 Agentic LLL adds extra "intelligence" to the NN**. To support "deduction", "reasoning", etc.

<img src="/assets/brain1c.png" alt="drones" width="32%">

<br>
-->

<!-- 
### [2.0a Overview of model evolution](/2.0a-model-evolution/)

An analogy between the brain and models. The main importance of understanding this is to 
- realize that the claims that AI has one iota of real intelligence are nonsense.
- gain an intrinsic understanding of how to exploit the incredible computing capabilities of models while minimizing the (substantial) limitations.

<br>

### [2.0b DIY models](/2.0b-diy-models/)

(TODO / v1 26.0524) How to create your own (do it yourself) models. For now just an idea. There are advantages to creating your own models (you select the training pattern data and you can ensure honesty and integrity of responses). The challenges are significant, but will lessen with time. In any case, understanding the steps involved for a practical demo will be very helpful in understanding how AI really works.
-->

<!--

### **[2.4 Agentic LLM (TF/UFA semantic) functionality](/2.4-agentic-llms/)**

Agentic LLMs (all major LLMs are agentic) are LLMs programmed with the required functionality and training data to support complex interaction with external agents (usually Python scripts). A few examples of agentic LLM functionality: 
- constrain response content/format as specified in prompts  
- build complex responses based on an analysis of prompt content (for example, breaking down a complex process description into planning steps that an agent can reasonably process)


<img src="/assets/brain1c.png" alt="drones" width="27%">

<br> -->



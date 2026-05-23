---
layout: page
title: "2 AI (models)"
permalink: /2_models/
---

<br> 


<!-- **Goals of this section:** 
- Convey the core concepts of AI
- show how to build practical applications (demos), 
- and to dispel AI hype.
That last point is essential for successful AI projects. -->

**Models run on clocked binary circuits**. They have no intelligence. You could run LLMs on electro-mechanical relays (it would take years to generate a token, but it theoretically possible). **LLM intelligence simulation is based on (1) binary computing structures and (2) massive computing power/speed**. The more you understand how LLMs work, the better you can use them in AI projects. 


*Agentic AI evolution ([about this diagram](/0.1-ai-evolution-diagram/))* <br>
<img src="/assets/zai_evolution6.png" alt="drones" width="50%">


<br>

### [(optional) 2.0 UFA concepts](/2.0-ufas/)

*("optional" = you might want to skip this page)*. Univeral Function **Approximator** (UFA) basic concepts. The neural networks (NN) in each of the model types below implements a UFA that **approximately matches input to patterns the NN was programmed ("trained") on**.

<br>

### [2.0a Overview of model evolution](/2.0a-model-evolution/)

An analogy between the brain and models.

<br>

### [2.1 Predictive NNs](/2.1-predictive-nns/)

Predictive NNs are small customized NNs for specific recognition tasks.

<img src="/assets/brain1.png" alt="drones" width="14%">

<br>

### [2.2 CNNs](/2.2-cnns/)

A CNN computes the most probable label ("dog", "airplane", etc) for a set of pixels. Studying CNNs is great preparation for studying more complex LLMs.

<img src="/assets/brain1a.png" alt="drones" width="17%">


<br>

### [2.3 LLMs](/2.3-llms/) (iAgent + TF)

An LLM generates the probabilities of all vocabulary token candidates for next token (a set of numbers) from the token sequence input. An LLM consists of an (1) internal agent and a (2) transformer (TF). The TF is the core computational engine behind modern AI systems and the mechanism that enables modern LLM behavior.

<img src="/assets/brain1b.png" alt="drones" width="22%">

<br>

### **[2.4 Agentic LLM (TF/UFA semantic) functionality](/2.4-agentic-llms/)**

Agentic LLMs** are LLMs with extra functionality to support agentic AI. It was only realistically possible for an agent (Python script, etc) to send prompts and receive response **after AI became agentic**, after LLMs were able to reliably  
- process incoming human language agent messages and 
- respond with the requested content and format constraints (as specified in the prompts)

<img src="/assets/brain1c.png" alt="drones" width="27%">


<br>

### [2.5 Robotic AI](/2.5-robotic-ai/)

JEPA, belief tracking, control loops, autonomy. Robotic NNs (such as JEPA, LeCun's new projects, etc) are specifically for robots. **I came to the conclusion that LeCun's version of JEPA was a lot of hype**. What he was selling was not fundamentally different from LLMs. GPT agreed.


<br>

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

26.0522

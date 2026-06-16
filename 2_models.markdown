---
layout: page
title: "2 NNs"
permalink: /2_models/
---

<br> 

<!-- *NNs (inside the models)* <br>
<img src="/assets/zai_evolution7.png" alt="drones" width="42%"> -->

*2 NNs in the master diagram* <br>
<img src="/assets/M-15-2x.png" alt="drones" width="80%">



<br>

**TOC**

- 2.0 Concepts
- 2.1 Core NNs 
- 2.2 Convolution
- 2.3 Transformers (TFs)
- 2.5 Robotic AI NNs
- 2.7 TF training algorithms (TODO)

<br>

### [2.0 Concepts](/2.0-ufas/)

The core of every model is the NN that implements a UFA (Univeral Function **Approximator**) that **generates an output based on pattern matching of the input**. The patterns were programmed ("trained") by setting NN parameters (weights and biases) during training.

<br>

### [2.1 Core NNs](/2.1-predictive-nns/)

Small NNs for specific tasks. **Includes DIY demos that give you a real understanding of the core of NNs**.

- D1: [2.1.1 Predictive NN 01 sine (D1)](/2.1.1-predictive-nn-01-sine/) (26.0524-25)
- D2: [2.1.2 Tiny classifier NN (D2)](/2.1.2-classifier-nn/) (26.0524-25)
- D3: [2.1.3 Tiny classifier NN on Render (D3)](/2.1.3-classifier-nn-render/) (26.0527)
- D6 [2.1.4 Pattern detector NN](/2.1.4-pattern_detector-nn/) (26.0604)
- D7: [2.1.5 Anomaly detector NN](/2.1.5-anomaly-detector-nn/)  (26.0605)
- D8: [2.1.6 Forecasting NN](/2.1.6-forecasting-nn/) (26.0605) (also D8b: 2.1.6 Forecasting NN noisy)

<img src="/assets/M-17.png" alt="drones" width="24%">


<br>

### [2.2 CNNs (convolution)](/2.2-cnns/)

A CNN computes the most probable label ("dog", "airplane", etc) for a set of pixels. **Studying CNNs is great preparation for studying more complex LLMs**.

- D4: [2.2.1 D4 CNN image classifier](/2.2.1-d4-cnn-image-classifier/) (26.0528)
- D4b: [2.2.1b D4 CNN algorithm details](/2.2.1b-d4-cnn-algorithm-details/) (26.0528)
- D9: [2.2.2 D9 CNN defect detector](/2.2.2-d9-cnn-defect-detector/) (26.0606)
- D10: [2.2.3 D10 CNN feature map visualization](/2.2.3-d10-cnn-feature-map-viz/) (26.0606)

<img src="/assets/M-18.png" alt="drones" width="40%">

<br>

### [2.3 TFs (transformers)](/2.3-llms/)

An LLM (1) inputs a sequence of tokens, (2) computes the probabilities of all vocabulary tokens as the next token, (3) outputs the selected new token, and finally (4) adds the new token to the next input sequence. An LLM consists of an (1) internal agent and a (2) transformer (TF) NN. **The TF is the core computational engine behind modern AI systems and the mechanism that enables modern LLM behavior**.

- D5: [2.3.1 D5 Tiny TF](/2.3.6.1-d5-tiny-tf/) (26.0529)
- D5b: [2.3.1b D5 tiny TF algorithm details](/2.3.6.1b-d5-tiny-tf-algorithm-details/) (26.0602)
- D11: [2.3.11 Tiny TF classifier](/2.3.11-d11-tiny-tf-classifier/) 
- D12: [2.3.12 Tiny TF sentiment detector](/2.3.12-d12-tiny-tf-sentiment-detector/)
- D13: [2.3.13 Tiny TF sequence predictor](/2.3.13-d13-tiny-tf-sequence-predictor/)

<img src="/assets/M-19.png" alt="drones" width="40%">

<br>

### [2.5 Robotic AI NNs](/2.5-robotic-ai/)

I no longer believe LeCun's hype about his version of JEPA that will supposedly be a fundamentally different type of AI platform (that fixes the fundamental limitations of LLMs; it doesnt, and never will). I have put this section on pauses. ***Robotic AI (that claims to be able to do what humans can do) is about as realistic as LLM intelligence, FSD, or colonizing Mars.**

See the **[Wiki page](https://github.com/terrytaylorbonn/auxdrone/wiki/Robotic-AI-demos)** for list of demos.

*A Waymo "self-drives" into a flooded street.* <br>
<img src="/assets/waymo.png" alt="drones" width="22%"> 

<br>

### [2.7 Training algorithms](/2.7-ai-models-training-algos/)

TODO

<br>

26.0616 (v1 26.0526)


<!-- 3 phases of model demos for each model group:
- P1 DIY (doit yourself) models / understand mechanics
- P2 OTS (offtheshelf) models 
- P3 OTS fine-tuned -->
<!-- <img src="/assets/brain1.png" alt="drones" width="14%"> -->
<!-- <img src="/assets/brain1a.png" alt="drones" width="17%"> -->

<!-- <img src="/assets/brain1b.png" alt="drones" width="22%"> -->

<!-- Note: The following diagram shows the **extra functionality ("reasoning", etc) that LLMs added later that enabled [agentic AI](/3.2-agentic-ai/)**.

<img src="/assets/brain1c.png" alt="drones" width="20%"> -->

<!--
### **[3.1 NNs](/2_models/)**

The NN is the core of AI "intelligence". A NN provides a pattern matching algorithm. The the NN is controlled by Python code ("agent").

- **3.1.1 Tiny NN demo (D2ccc) INFERENCE**
- **3.1.1b Tiny NN demo (D2ccc) TRAINING**
- **3.1.2a ALEXNET CNN** (this is a good example to study before doing the Tiny CNN demo)
- **3.1.2b Tiny CNN demo (D4)**
- **3.1.3 Tiny TF demo (D5)**
-->


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

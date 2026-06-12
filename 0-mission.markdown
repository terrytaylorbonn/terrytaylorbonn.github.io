---
layout: page
title: Mission
permalink: /0-mission/
---

<br>

This page describes the **ZiptieAI mission**. 

<br>


**TOC**
- **1 Recognizing what works**
- **2 And what doesnt work**
- **3 Providing core insights (via demos)**. For details see the **[QS demos](/0-qs/)**.  
- **4 Anticipating the future**

<br>

## **1 Recognizing what works** 

*A successful mission for AI* <br>
<img src="/assets/ziptiedrone2.png" alt="drones" width="23%">


**Palantir's first real practical application was in the military. That's no accident.**
- Benefits >> negatives.
- Errors can be tolerated (not used in the nuclear forces).
- Man in loop.

Palantir is making a lot of money because they provide a product that is extremely useful. And they talk straight about things that others only hype about. **Engineers wont go away, their expertise is required in the AI age more than ever**. Only Palantir is saying this, because Palantir's business does **not demand the myth of AI intelligence**. Palantir is the only company that at first said that **AI will empower people, not replace them**.


<br>

## **2 And what doesnt work**

*An unsuccessful mission for AI*<br>
<img src="/assets/waymo.png" alt="drones" width="26%"> 

#### **The endless hype**

"No more programmers" (Jensen Huang), "no more work for people" (Musk), "we must pause AI development because its not safe" (Anthropic CEO), "AI already has emotions" (Jeffrey Hinton) etc etc. But even Palantir has its own hype. Watch the first (English) half of this fascinating **[interview of Palantir CTO](https://www.youtube.com/watch?v=lcUHDsA5lzc)**. Pure unadulterated hype. I could not help but laugh at every other sentence from the CTO.  *Details about video soon.....*

The reasons for the hype:
- Money. That's the motivation for any successful company. 
- They have a product that noone understands. Just like Pfizer a few years ago.
- People dont understand the science. Just like with Covid and mRNA.
- There is no incentive to promote anything but a merely superficial understanding of AI among the general public (and government officials). 

<!-- The AI gurus, titans, employees (with stock options), and their financial backers all know they will get rich with the coming AI IPOs. The success of these IPO's depends greatly on the public not understanding certain aspects/myths about AI. *Recently some very interesting details of these IPOs have come to light that suggest a coordinated effort to mislead the public (I won't talk about because so many others are).* -->

#### **AI has no intelligence (and therefore is never in control)**
Think for a minute what AI integration into a companys digital infrastructure would be like if AI was truly intelligent. You just put AI in control of the existing digital infrastructure and done. **Turnkey integration.** **But AI is not intelligent. AI is based 100% on deterministic binary algorithms that compute statistical probabilities.** Therefore, it can not be the central loop (NNs are not control loops). **AI is an addon.** 
- Non-AI code bases have to provide any deterministic functions such as control, validation, permissions, execution, logging, and safety. 
- AI must be custom built into the system by those who understand **AI's significant risks and limitations** (thats why Palantir employs **forward deployed engineers** (FDEs)).
- The most reliable AI systems use the smallest AI component that can provide the required functionality.

#### **AI is a security risk**
AI is the gatekeeper of the source of truth. But the safety and reliability of that "truth" is only as good as reputation of whoever programmed ("trained") the AI model. The core NN in AI has what are often referred to as "hidden layers" (HLs). These are the layers in the NN that perform number crunching to generate "intelligent" output. **Understanding what those HLs do by looking at the parameter values is impossible**. You can not tell what have been programmed into the AI core. 

<br>

## **3 Providing core insights (demos)**

#### **For details see the [QS demos](/0-qs/)**

I was quite confident in my assessment of the Palantir CTO's speech because I've built many AI demo projects. But the most insight I got from "simple" "tiny" demos. Such **demos are the core of the ZAI website, and are organized into 3 sections:**

- **3.1 NNs**
- **3.2 Models**
- **3.3 Agents (external)**

<br>

### **[3.1 NNs](/2_models/)**

<!-- The NN is the core of AI "intelligence". A NN provides a pattern matching algorithm. The the NN is controlled by Python code ("agent").


 - **3.1.1 Tiny NN demo (D2ccc) INFERENCE**
- **3.1.1b Tiny NN demo (D2ccc) TRAINING**
- **3.1.2a ALEXNET CNN** (this is a good example to study before doing the Tiny CNN demo)
- **3.1.2b Tiny CNN demo (D4)**
- **3.1.3 Tiny TF demo (D5)** -->

<br>

#### **3.1.1 Tiny NN demo (D2ccc)** 

<!-- *"Inference" means normal run-time operation. Generating output from input. Training is described next.*  -->

A simple NN demo of the core of AI. 

*Demo D2ccc (left) and test results (right)*<br>
<img src="/assets/M-05.png" alt="drones" width="46%">     <img src="/assets/M-02.png" alt="drones" width="26%">

<br>

<!-- #### **3.1.1b Tiny NN demo (D2ccc) TRAINING**

(WIP) 

<br> -->

#### **3.1.2 Tiny CNN (D4)**

See [2.2.1 D4 CNN image classifier](https://ziptieai.com/2.2.1-d4-cnn-image-classifier/) and (for details) [2.2.1b D4 CNN algorithm details](https://ziptieai.com/2.2.1b-d4-cnn-algorithm-details/).


<img src="/assets/M-07.png" alt="drones" width="46%">
<img src="/assets/M-08.png" alt="drones" width="20%">

<!-- A good example to study before doing the Tiny CNN demo.

Diagram from page [2.2.1b D4 CNN algorithm details](https://ziptieai.com/2.2.1b-d4-cnn-algorithm-details/).

<img src="/assets/M-06.png" alt="drones" width="46%"> -->


<br>

#### **3.1.3 Tiny TF (D5)** 


<img src="/assets/M-09.png" alt="drones" width="70%">


<br>


### **[3.2 Models](/2b_models/)** (with API)

The agent and the NN are typically packed into a **model** that has an API that makes it possible for existing software to **use the model as a "helpful" assistant**. 

<br>


### **[3.3 Agents](/3_agents/)**

External (not LLM internal) agents provide 
- reliable workflows built around models, tools, and automation. 
- tolerance of AI faults and unpredictable outputs


<br>

## **4 Anticipating the future**

AI has big a future after the IPOs are finished and the hype is over.
Those that understand how AI really works stand to benefit the most.
The original ZiptieAI was my personal learning project.
But now **ZiptieAI has a mission to help myself (and others) stay ahead of the AI curve**. 
In the no-so-distant future, AI integration skills will be required in the digital infrastructure of all business segments. This work will required a massive number of tech workers who, empowered by AI tools, will help integrate AI **as a helpful assistant** into all areas of life.  

<br>



26.0612 (v1 26.0611)

<!-- *A successful mission for AI (left) and not so successful mission (right).* <br>
<img src="/assets/ziptiedrone2.png" alt="drones" width="23%"> <img src="/assets/waymo.png" alt="drones" width="26%">  -->

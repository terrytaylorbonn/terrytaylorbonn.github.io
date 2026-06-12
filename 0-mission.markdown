---
layout: page
title: Mission
permalink: /0-mission/
---

*v1 26.0611 **WIP**. This page replaced **[TL;DR (v1)](/0-tldr/)**.*

<br>

This page describes the **ZiptieAI mission**. 

<br>

<!-- *A successful mission for AI (left) and not so successful mission (right).* <br>
<img src="/assets/ziptiedrone2.png" alt="drones" width="23%"> <img src="/assets/waymo.png" alt="drones" width="26%">  -->

**TOC**
- 1 Recognizing what works
- 2 And what doesnt work 
- 3 Providing core insights (demos)
- 4 Anticipating the future

-----------------<br>

- 5 NN demo D2cc details

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

"no more programmers" (Jensen Huang), "no more work for people" (Musk), "we must pause AI development because its not safe" (Anthropic CEO), "AI already has emotions" (Jeffrey Hinton) etc etc. 

But even Palantir has its own hype. Watch the first (English) half of this fascinating **[interview of Palantir CTO](https://www.youtube.com/watch?v=lcUHDsA5lzc)**. Pure unadulterated hype. I could not help but laugh at every other sentence from the CTO.

*Details about video soon.....*



The reasons for the hype:
- Money. That's the motivation for any successful company. 
- They have a product that noone understands. Just like Pfizer a few years ago.
- People dont understand the science. Just like with Covid and mRNA.
- There is no incentive to talk about the helpful details of how AI really works. The AI gurus, titans, employees (with stock options), and their financial backers all know they will get rich with the coming AI IPOs. The success of these IPO's depends greatly on the public not understanding certain aspects/myths about AI. *Recently some very interesting details of these IPOs have come to light that suggest a coordinated effort to mislead the public (I won't talk about because so many others are).* This also helps in getting government subsidies.

#### **AI has no intelligence (and is never in control)**
Think for a minute what AI integration into a companys digital infrastructure would be like if AI was truly intelligent. You just put AI in control of the existing digital infrastructure and done. **Turnkey integration.** **But AI is not intelligent. AI is based 100% on deterministic binary algorithms that compute statistical probabilities.** Therefore, it can not be the central loop (NNs are not control loops). **AI is an addon.** 
- Non-AI code bases have to provide deterministic functions such as control, validation, permissions, execution, logging, and safety. 
- AI must be custom built into the system by those who understand **AI's significant risks and limitations** (thats why Palantir employs **forward deployed engineers** (FDEs)).
- The most reliable AI systems use the smallest AI component that can provide the required functionality.

#### **AI is the ultimate security risk**
AI is the gatekeeper of the source of truth. But the safety and reliability of that "truth" is only as good as reputation of whoever programmed ("trained") the AI model. AI can easily become the "evil" in Google's "dont be evil". The core NN in AI has what are often referred to as "hidden layers" (HLs). These are the layers in the NN that number crunch the inputs to generate "intelligent" output. **Understanding what those HLs do by looking at the parameters is impossible**. You can not tell if there is a "backdoor" prompt waiting to be activated. **The solution: Build your own. This will get easier with time**. 


<br>

## **3 Providing core insights (demos)**

I was quite confident in my assessment of the Palantir CTO's speech because I've done a lot of a projects. But the most insight I have gotten came from "simple" "tiny" demos. To really understand AI, **you need to study (line by line) the code of tiny demos** of core AI functionality. Such **demos are the core of the ZAI website, and are organized into 3 sections:**

- 3.1 NNs
- 3.2 Models
- 3.3 Agents (external)

<br>

### **[3.1 NNs](/2_models/)**

The NN is the core of AI "intelligence". A NN provides a pattern matching algorithm. The the NN is controlled by Python code ("agent").

*A TF NN*<br>
<img src="/assets/M-04.png" alt="drones" width="36%"> 

<!-- Thats why FDE's, because they understand how the system must be tweeked to get an acceptable error rate. -->

- 3.1.1 Tiny NN demo (D2ccc) 
- 3.1.2 Tiny CNN demo
- 3.1.3 Tiny TF demo 


<br>

#### **3.1.1 Tiny NN demo (D2ccc)** *(see section 8 at the end of this page for code description)*

<img src="/assets/M-02.png" alt="drones" width="26%">

<br>

#### **3.1.2 Tiny CNN demo** 

(TODO) 

<br>

#### **3.1.3 Tiny TF demo** 

(TODO) 

<br>


### **[3.2 Models](/2b_models/)** (with API)

The agent and the NN are typically packed into a **model** that has an API that makes it possible for existing software to **use the model as a "helpful" assistant**. 

I refer to the **code in the model that controls the TF NN as the "internal agent" (iAgent)**. This concept is central to understanding how models work. *Note: GPT has steadfastly resisted my use of this term until only recently. That's because GPT was never programmed with text that discussed such a concept.*


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

--------------------
--------------------
--------------------
--------------------

<br>

## **5 NN demo D2cc details**

*Note: I created this version of the D2 demo on 26.0611. I documented the details in **[docx #607](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**. Its similar to D2 demo on page **[2.1 Core NNs](/2.1-predictive-nns/)**.*

1) The short bit of code shown below defines the D2ccc Tiny Demo classifier NN.

```
model = nn.Sequential(
    nn.Linear(2, 16),
    nn.ReLU(),
    nn.Linear(16, 16),
    nn.ReLU(),
    nn.Linear(16, 2),  # 2 class scores/logits
).to(device)
```

2) This is the resulting NN.


```text2
- W = weights, b = biases (these are the model parameters that are UPDATED during training and FIXED during inference)
- h1-01 = hidden layer 1, neuron 01
- h1-02 = hidden layer 1, neuron 02
- ...
- h2-1 = hidden layer 2, neuron 01
- ...
- y-1  = output neuron 1
- y-2  = output neuron 2
```

- 50 data points
- 100 epochs
- num_test = 30

<img src="/assets/M-01.png" alt="drones" width="43%">


3) Computation details. 

```
x, y (inputs)
        ▼
Layer 1: nn.Linear(2,16)
 h1_1 = w1*x + w2*y + b  → ReLU → a1_1
 ...
 h1_16= w1*x + w2*y + b  → ReLU → a1_16
        ▼
Layer 2: nn.Linear(16,16)
 h2_1 = w1*a1_1 + w2*a1_2 + ... + w16*a1_16 + b  → ReLU → a2_1
 ...
 h2_16= w1*a1_1 + w2*a1_2 + ... + w16*a1_16 + b  → ReLU → a2_16
       ▼
Output layer: nn.Linear(16,2)
 logit_outside = w1*a2_1 + w2*a2_2 + ... + w16*a2_16 + b
 logit_inside  = w1*a2_1 + w2*a2_2 + ... + w16*a2_16 + b
        ▼
argmax(logits)
        ▼
class 0 = outside circle
class 1 = inside circle
```

4) These are the total number of computations within the NN.

```text2
TOTALS
- 354 wx+b operations + 32 ReLU operations = 386 simple operations per point
- weights: 32 + 256 + 32 = 320
- biases: 16 + 16 + 2 = 34
- total parameters = 354
- ReLU after h1: 16 comparisons
- ReLU after h2: 16 comparisons
```

5) Resulting output (**I will explain these results better later**). 

- I intentionally lowered the training length to make the result less than optimal (easier to see).
- I added the green circle. It shows where the boundary should be (*in this demo you could compute the test points to see if they were in the center; an equation would work; but the point of this demo is to show how to can do that without equations and what results would be; this would be valuable for data sets that cannot be classified by a simple equation*).
- Yellow / purple area boundary was the NN-computed from a limited data set.
- White dots = outside area.
- Red dots = NN corrected classified as in the green circle.
- X marks = NN incorrectly classified as outside the green circle.

test 1
- 50 data points
- 100 epochs
- num_test = 30

<img src="/assets/M-02.png" alt="drones" width="43%">

test 2
- 500 data points
- 1000 epochs
- num_test = 30

<img src="/assets/M-03.png" alt="drones" width="43%">


6) Lessons learned from this demo:
- The simple NN can classify x,y locations with good accuracy.
- **But classification accuracy is not equation-level perfect**. In our simple demo the results were good for a small NN. But for more complex datasets the size of the NN would increase dramatically. AI must be used where the input / output relationship can not be defined with simple computation or equations. **But AI is always an approximation (UFA, universal function approximator), so the challenge is integrating AI so that the approximation errors are acceptable** (for war time planning systems OK, for self driving cars or home humanoids NOT OK).

<br>



26.0612 (v1 26.0611)

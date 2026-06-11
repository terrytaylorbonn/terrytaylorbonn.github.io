---
layout: page
title: Mission
permalink: /0-mission/
---

*v1 26.0611 **WIP**. I have a lot of notes to still add to this page. But the core organization and concepts are fairly stable. This page replaced **[TL;DR (v1)](/0-tldr/)** on 26.0611 (the old page is still an interesting read).*

<br>

This page describes the **ZiptieAI mission**. 



*A successful mission for AI (left) and not so successful mission (right).* <br>
<img src="/assets/ziptiedrone2.png" alt="drones" width="23%"> <img src="/assets/waymo.png" alt="drones" width="26%"> 


<br>

**TOC**
- 1 AI's big future
- 2 Knowledge is power (dont get scammed)
- 3 Why are they doing this?
- 4 AI is never the central control loop
- 5 Low level demos are the key
- 6 AI is the ultimate security risk
- 7 The future

<br>

## **1 AI's big future**

Palantir is making a lot of money because they provide a product that is extremely useful.

**Engineers wont go away, their expertise is required in the AI age more than ever**. Only Palantir is saying this, because Palantir's business does **not demand the myth of AI intelligence** *("no more programmers" (Jensen Huang), "no more work for people" (Musk), "we must pause AI development because its not safe" (Anthropic CEO), "AI already has emotions" (Jeffrey Hinton) etc etc)*. Palantir is the only company that at first said that **AI will empower people, not replace them**.

<br>

## **2 Knowledge is power (dont get scammed)**

Having just praised Palantir, its now time to expose Palantir's hype.  Watch the first (English) half of this fascinating **[interview of Palantir CTO](https://www.youtube.com/watch?v=lcUHDsA5lzc)**. Pure unadulterated hype. I could not help but laugh at every other sentence from the CTO.

*I will write much more about this video soon.*

<br>

## **3 Why are they doing this?**

- Money. That's the motivation for any successful company. 
- They have a product that noone understands. Just like Pfizer a few years ago.
- People dont understand the science. Just like with Covid and mRNA.
- There is no incentive to talk about certain all the helpful details.

The AI gurus, titans, employees (with stock options), and their financial backers all know they will get rich with the coming AI IPOs. The success of these IPO's depends greatly on the public not understanding certain aspects/myths about AI. *Recently some very interesting details of these IPOs have come to light.* This is also crucicial for getting government subsidies.

<br>

## **4 AI is never the central control loop**

A central myth that is being pushed is that AI is in control.

Think for a minute what AI integration into a companys digital infrastructure would be like if AI was truly intelligent. You just put AI in control, in the center, and the old infrastructure is AI's slave. **Turnkey integration.**

**But AI is not intelligent. AI is based 100% on deterministic binary algorithms that compute statistical probabilities.** Therefore, it can not be the central loop (NNs are not control loops). **AI is an addon.** 
- AI must be custom built into the system. 
- AI is used only where judgment, classification, summarization, prediction, or pattern detection is required. 
- The most reliable AI systems use the smallest AI component that can solve the uncertain part of the workflow.

Deterministic code for control, validation, permissions, execution, logging, and safety. Thats the existing company code base. AI must be added on. And added on by those who understand **AI's significant risks and limitations**. Thats why Palantir employs **forward deployed engineers** (FDEs).

<br>

## **5 Low level demos are the key**

To really understand AI, **you need to study (line by line) the code of tiny demos** of core AI functionality. Such **demos are the core of the ZAI website, and are organized into 3 sections**.


#### **[2 NNs](/2_models/)**

The NN is the core of AI "intelligence". A NN provides a pattern matching algorithm. Thats why FDE's, because they understand how the system must be tweeked to get an acceptable error rate.

In the tiny demos the NN is controlled by Python code (a tiny "agent").

*I will add here several diagrams of NN internals soon.*


#### **[2b Models](/2b_models/)** (with API)

The agent and the NN are typically packed into a **model** with an API that makes it possible for existing software to **use the model as a "helpful" assitant**. 

I refer to the **code in the model that controls the TF NN as the "internal agent" (iAgent)**. This concept is central to understanding how models work.

*Note: GPT has steadfastly resisted the use of this term until only recently. That's because GPT was never programmed with text that discussed such a concept.*


#### **[3 Agents](/3_agents/)**

External (not LLM internal) agents provide 
- reliable workflows built around models, tools, and automation. 
- tolerance of AI faults and unpredictable outputs

**Palantir systems first real practical application was in the military. That's no accident.**
- Benefits >> negatives.
- Errors can be tolerated (not used in the nuclear forces).
- Man in loop.

<br>

## **6 AI is the ultimate security risk**

AI is the gatekeeper, the secret agent. The "evil" in Google's "dont be evil".

The core NN in AI is typically referred to as the "hidden layer". You can actually view the programmed ("trained") parameters for these layers, but **you have no idea what the results of these parameters are**. 

<br>

## **7 The future**

AI has big future after the IPOs are finished and the hype is over.
But before then many will get scammed by the hype.
Dont be one of them.
The original ZiptieAI mission was my personal learning project.
But now **ZiptieAI has become a site to help myself (and others) stay ahead of the curve**.

<br>

26.0611 (v1 26.0604)

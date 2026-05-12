---
layout: page
title: "(2b) UFAs"
permalink: /UFAs/
---

<br>


*This page is WIP (v1 26.0510). I've not seen a presentation on the UFA topic like this anywhere, so I created my own.*

<br>

#### **The TF UFA is critical to Agentic AI. So why do you never hear anything about UFAs?**

Its probably because of the word "approximator". 

**If an LLM was truly intelligent, then an AI agent (Python app) could simply send free form text and be done with it.** But an LLM is not intelligent. **LLM outputs are statistical approximations** (the "A" in "UFA", "Univeral Function Approximator") based on the (1) algorithms and (2) input data used to program ("train") the LLM TF.  Therefore to use AI agents effectively, it really helps to understand Universal Function Approximators (UFAs) and how they are implemented in LLM TFs. It's your best defense againt the omnipresent AI hype. 

This section talks about the **GPT-3 transformer (TF)**. Newer models may be much more powerful, but the core techniques they use to implement a UFA will be similar. Most of this page is my original material (I'm sure this kind of info is out there in the internet somewhere, but I have not seen a single cohesive presentation like this). So (as the LLMs always say) a disclaimer: **I sometimes make mistakes. :)**

<br>

### **TOC**

<!-- ***TL;DR?** Read section 2.*

**1 The LLM TF UFA is the only practical interface between human language and (unintelligent) computers**  -->



**[1 We need a practical human-language <> computer interface](/2b-1-TF-only-interface/)**

- Human communication systems (language) are designed for intelligent beings.
- Digital systems are simply computation. No intelligence. 
- Digital systems are vital for us. We need a bridge. 
- TF UFA is only viable option. But it has definite limits.


**[2 Belgium UFA](/2b-2-belgium-UFA/)** is the simplest UFA conceptual demo.
- The simplest demo of a UFA that 
  - inputs x/y (lat/long) coordinates and 
  - outputs if you are in Belgium or Netherlands. 
- This is a good demo from Welch labs. I explain in much more detail. 
- This UFA can be programmed manually. 

**[3 Digits UFA](/2b-3-digits-UFA/)** tries to use the Belgium demo to detect digits.
- You often see CNNs used to detect digits. 
- In this demo, I want to show how you could try to do this with 
  -  a manually programmed UFA 
  - built ono the Belgium demo. 
- It wont work well, but is still instuctive. *This is my own original idea, not sure if it makes sense.* 

**[4 CNN UFA](/2b-4-CNN-UFA/)** (convoluted neural networks). AlexNet 2012 is an excellent demo.
- 2012 AlexNet Object recognition demo
- Data for training was the key (you cant train this manually)
- This is an excellent demo to understand the basics before tackling TF UFA

**[5 TF UFA](/2b-5-TF-UFA/)** (transformer) is the best UFA for human language.

Its not intelligent. Its computational pattern matching.
- TF converts each (1) Human Language (HLang) input (prompt) into (2) Vector Language (VLang).
- The VLang for each prompt is refined into a "storyline".
- The **(3) storyline of the last token is used to determine the vocab token that most closely matches what has been programmed into the NN for the current input**.
- **(4) TF adds the new token to the input and repeats the process** (until finished or told to stop).
- HLang/JSON can be added to the initial HLang input to describe how the **(5) LLM should customize the response content and structure**. This greatly enhances the ability of the "deterministic" agent (usually Python) to reliably process the reponse. 
- For examples of TF Agentic with AI see "4 Agent+AI concepts" on page [(4) Agentic AI](/agentic-ai/)

<br>

<!--
<br><br><br>
=======================================================
<img src="/assets/.png" alt="drones" width="40%"> 
-->



26.0512 (v1 26.0510)

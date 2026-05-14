---
layout: page
title: "(2b) UFAs"
permalink: /UFAs/
---

<br>


**An LLM transformer (TF) is a** Universal Function **Approximator (UFA)**. You've probably never heard anything about UFAs. Thats because of the word "approximator". **This word shatters the idea that AI is intelligent.** 

**AI will never be in charge; it will always be nothing more than a "helpful assitant". But it is an incredible assistant. Revolutionary.**

Understanding what a UFA does is extremely helpful when designing agentic AI apps. what the limitations are. To keep you from spending money on projects based on false assumptions (the AI titans just want you to spend your money). **Because an LLM is not intelligent, AI agents are not the answer for many problems. And even if Agentic AI is the solution, it has to be designed carefully.** 


<br>

This page is my own take on UFAs for AI. THe following is a sampling of my thoughts on UFAs and AI in general:

- **A TF UFA is 100% deterministic**. There is a very mistaken idea that GPUs are not deterministic like CPUs. They are. For basic info, watch this: 
  - ByteMonk released (26.0510 ) a fantastic video that clearly describes **how GPUs operate ([Google's New TPU Quietly Ends the GPU Era?](https://www.youtube.com/watch?v=iseM_Sb-ruo))**. 
  - In the future, I will start using "GPU-based" and "CPU-based" to distinguish betweed the AI and the agentic parts of apps ("deterministic" is a misleading misnomer). 
- **A TF UFA performs token sequence recognition**. 
- You have to use an approximator to recognize token sequences because **human languages are just primitive hints designed for intelligent human to communicate complex concepts**. 
- **Word combinations can be almost infinite**, with all kind of spelling mistakes, abbreviations, bad grammar, etc etc. You can never create a DB of all possible combinations.
- **UFA can make a good guess of the meaning of inputs that are not an exact match to to any inputs it was programmed ("trained") on.**
- **Machines have no intelligence. The only they can process human language (HL) is to implement a UFA is with massive brute force computation** (thus GPUs instead of CPUs; theoretically you could use a CPU for any GPU task, but it would be vastly slower).
- The UFA works by converting input tokens (word parts, "Human Language (HL)") into numbers (what I call "vector language" (VL)). **The UFA has no concept of anything but numbers**. 
- The UFA then performs massive GPU computations to create from the original VL a very detailed numberical representation of the meaning of the entire token input set (lets just call this the "storyline"). In most LLM TFs, that storyline is stored in the last token VL.
- The storyline is a conceptual/feature summation/detection of the input. **The concepts/features are derived not from human interpretations of language, but from the training data set. They are strictly numerical.**
- THe storyline is converted into a probability for each token in the entire vocabulary. The best token is chosen (unless you use temperature, which selects less than optimal token to give the illusion that the UFA is not deterministic).

<br>

Much of the above is my own interpretation after intensive study of LLM TFs and many conversations with GPT.  Most of this page is my original material. So (as the LLMs always say) a disclaimer: **I sometimes make mistakes. :)**



<!-- But an LLM is not intelligent. **LLM outputs are statistical approximations** (the "A" in "UFA", "Univeral Function Approximator") based on the (1) algorithms and (2) input data used to program ("train") the LLM TF.  Therefore to use AI agents effectively, it really helps to understand Universal Function Approximators (UFAs) and how they are implemented in LLM TFs.  -->



<br>

### **TOC**

<!-- ***TL;DR?** Read section 2.*

**1 The LLM TF UFA is the only practical interface between human language and (unintelligent) computers**  -->



**[1 We need a practical human-language <> computer interface](/2b-1-TF-only-interface/)**

- Human communication systems (language) are designed for intelligent beings.
- Digital systems are simply computation. No intelligence. 
- Digital systems are vital for us. We need a bridge. 
- TF UFA is only viable option. But it has definite limits.

**[(2b)-1a Latent semantic computation](/2b-1a-latent-semantic-computation/)** (currently just chat).



**[1b ZAI 2D demo UFA](/2b-1b-ZAI-2D-demo-UFA/) (DRAFT)** is the simplest UFA conceptual demo.


**[2 Belgium UFA](/2b-2-belgium-UFA/) (DRAFT)** is another very simple conceptual demo that has received almost 400K views and great reviews. **There are several core misconceptions in this video. They are very instructive.**
- It shows 
  - inputs x/y (lat/long) coordinates and 
  - outputs if you are in Belgium or Netherlands. 
- This UFA can be programmed manually. 



<!-- - Its spending too much effort with 3d depictions. These depictions are nice to look at, and impressive, but they dont convey an understanding of what is going on.
 - Video tries to expand this to multi-layer NNs. But this is where the main idea of this demo breaks down. I will explain why in [4b Belgium UFA multilayer UFA](/2b-4b-belgium-multilayer-UFA/) (see below). -->

<!-- **[3 Digits UFA](/2b-3-digits-UFA/) (TODO)** tries to use the Belgium demo to detect digits.
- You often see CNNs used to detect digits. 
- In this demo, I want to show how you could try to do this with 
  -  a manually programmed UFA 
  - built ono the Belgium demo. 
- It wont work well, but is still instructive. -->


**[(2b)-3 Training](/2b-3-training/)**


**[4 CNN UFA](/2b-4-CNN-UFA/) (TODO)** (convoluted neural networks). AlexNet 2012 is an excellent demo.
- 2012 AlexNet Object recognition demo
- Data for training was the key (you cant train this manually)
- This is an excellent demo to understand the basics before tackling TF UFA

<!--
**[4b Belgium UFA multilayer UFA](/2b-4b-belgium-multilayer-UFA/)**. I revisit the Belgium demo again, using the lessons learned from the CNN convultion to explain what is really going on in the Belgium multi-layer NN.-->


**[5 TF UFA](/2b-5-TF-UFA/) (WIP)** (transformer) is the best UFA for human language.

This section talks about the **GPT-3 transformer (TF)**. Newer models may be much more powerful, but the core techniques they use to implement a UFA will be similar.  
Its not intelligent. Its computational pattern matching.
- TF takes the **convolution/max-pooling** concept in CNNs and duplicates the same idea for language in TF as **Attention-heads/softmax**. This is my own idea, and its key to understanding how the TF functions. 
- TF converts each (1) Human Language (HLang) input (prompt) into (2) Vector Language (VLang).
- The VLang for each prompt is refined into a "storyline".
- The **(3) storyline of the last token is used to determine the vocab token that most closely matches what has been programmed into the NN for the current input**.
- **(4) TF adds the new token to the input and repeats the process** (until finished or told to stop).
- HLang/JSON can be added to the initial HLang input to describe how the **(5) LLM should customize the response content and structure**. This greatly enhances the ability of the "deterministic" agent (usually Python) to reliably process the reponse. 
- For examples of TF Agentic with AI see "4 Agent+AI concepts" on page [(4) Agentic AI](/agentic-ai/)




**[(2b)-6 Predictive](/2b-6-predictive/)**

<br>



<!--
<br><br><br>
=======================================================
<img src="/assets/.png" alt="drones" width="40%"> 
-->



26.0514 (v1 26.0510)

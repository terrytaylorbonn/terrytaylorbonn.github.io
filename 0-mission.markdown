---
layout: page
title: Mission
permalink: /0-mission/
---

<br>

<!-- *Page reorganized 26.0701 -->

The **ZiptieAI mission** is to give you 

- 1 Core AI concepts
- 2 Core AI demos and technical concepts
- 3 AI deep dive (code)
- 4 Anticipation of the AI future

<br>

### **1 Core AI concepts** 

**I never cease to be amazed by the engineering genius behind AI**. That being said, **building successful AI applications requires a basic understanding of what AI really is**. *Section "Concepts" is more technical.... this section is more big picture, the market, getting the gist of AI.*
- 1.1 AI = deterministic algorithms running on digital HW
- 1.2 LLM agent + transformer = simulated intelligence
- 1.3 The core of AI: NN classification (matrix math based pattern matching)
- 1.4 Extensions of the simple NN (CNNs, TFs)
- 1.5 The TF algorithm (QKV context computation from 2020) is still the basis of LLM AI
- 1.6 AI is an incredible revolutionary engineering marvel.. for the right applications
- 1.7 Falling for AI hype can cost you... dearly
- 1.8 AI's place in our world (not our place in AI's world)

<!-- - 1.1 AI = deterministic algorithms running on digital HW
- 1.2 There is no "I" (intelligence) in AI
- 1.3 (1.2b) So what is AI? AI = classification, pattern matching (simple NN)
- 1.4 (1.2c) Variations of the simple NN theme (CNNs, TFs)
- 1.5 (1.2d) KV saved (HACKS) (cant get better algo to work)
- 1.6 (1.4) AI is an incredible revolutionary engineering marvel.. for the right applications
- 1.7 (1.3) Falling for AI hype can cost you... dearly
- 1.8 (1.5) AI's place in our world (not our place in AI's world)
-->


<br>

#### **1.1 AI = deterministic algorithms running on digital HW**

The following shows the code that defines the NN structure and the training algorithm.  Clocked circuit state machine. It will always output the EXACT same result for the same input.

<img src="/assets/M-14.png" alt="desc" width="60%"> 

The AI simulation of intelligence started to seem intelligent only recently after the computational hardware reached the performance level required to (1) generate responses at least as fast as a human would respond and (2) with a level of accuracy that at least initially convinced the human user that AI had some level of genuine intelligence. 

But AI has 0 intelligence. **AI circuits have absolutely no similarity whatsoever to human brain neurons.** Human thought exists not as a snapshot, but as a symphony playing out in time. But AI circuits host clocked state machines.  

You could even run the most sophisticated LLMs on electro-mechanical relays. It might require the entire power output of nuclear plant and take a year or more to generate a token response, but it is theoretically possible.  

*Electro-mechanical relay (a theoretical alternative to the GPU)*<br>
<img src="/assets/relay.png" alt="drones" width="12%">



<br>

#### **1.2 LLM agent + transformer = simulated intelligence**

LLM AI is based on 2 very distinct computational components.

- **Transformer (TF)** generates response tokens based on the input tokens. The actual TF algorithm only computes FP numbers. **The TF computational process is a straight shot (not procedural)**. The TF computes a classification of the entire input. This classification is used to select the next token. That new token is added to the input. The TF is reset, and the process for the next token starts. This process continues until the TF stops or the iAgent comands a stop.
- **Internal agent (iAgent)** sends and receives tokens to/from the TF. The iAgent is the core control loop, the typical **procedural program** (usually confusing referred to as **the** deterministic program; the problem is the GPU is also 100% deterministic). The iAgent has an API that allows the external world (a human or an "external Agent") to use the model. 

Note: TF algorithms are referred to as "neural" networks because the diagrams for NN matrix math look like diagrams that could be considered similar to those for biological neural networks.   

<img src="/assets/M-15-2bbb.png" alt="drones" width="63%"><br>


*The LLM agent and transformer are the inseparable duo that simulates intelligence*<br>
<img src="/assets/M-11b.png" alt="drones" width="33%"><br>


<!-- **This site takes a very down-to-earth mechanistic approach to understanding AI. Thats because AI is based on mechanistic binary matrix math algorithms that run on binary circuits.** 
**A "model" in AI is anything that has a neural network (NN) at its core**. It may have a lot of other stuff wrapped around the NN (CNN convolution, LLM attention heads, etc) but **the core statistical pattern matching functionality runs on a NN**. The differences are mainly architecture, training, orchestration, and use case. **All models are first (1) "trained"** (internal NN params are programmed using SW tools) and **then (2) used to infer output from input.** 
*AI model components and code (code does not lie)*<br>
<img src="/assets/M-15-2b.png" alt="drones" width="53%"><br><br> 
<img src="/assets/M-14.png" alt="desc" width="60%">  -->

<br>

#### **1.3 The core of AI: NN classification (matrix math based pattern matching)**

**"Training" = programming a NN (not teaching; a NN does not learn)**. The process involves
- Feed FP numbers (converted input text prompt and answer) to the NN.
- Compare the input against the shifted (one token) output.
- Adjust the internal parameters of the NN every so slightly so that the error from the expected output is reduced (without messing up significantly other already trained inputs).
- Repeat this a massive number of times. This "training" can take weeks. 
- Hope for a stable result. The training process is not predictable.

**Inference** is when the TF is used to recognize the pattern of the some never before encountered input (not matching **exactly** anything the TF was trained on). This is the "magic" of AI. The TF computes the probabilities of all possible outputs (usually 50K vocab tokens) and the best token is selected (unless "tempearture" is used; this is a gimmick where the TF selects randomly one of the more probable tokens to give the illusion that the TF is non-deterministic). 

<img src="/assets/M-50.png" alt="drones" width="23%">

<br>

#### **1.4 Extensions of the simple NN (CNNs, TFs)**

Detecting simple patterns (classification) worked fine with a simple NN. But for images and text, some extra "pre-processing" is required for classification. 

For text **convolution** is added (thus convoluted NN). Convolution is matrix math performed before the core classification NN (the "dense layers"). This is required because of the nature of recognizing pixelated input (pixels are convoluted with neighboring related pixels).

For text a **transformers** is added. This basically computes the real meaning of the original tokens based on the "neighboring" **by meaning** tokens. There is also the core NN in the form of an "FFN" (no need to translate, the name is meaningless) for each token. The tokens adjust each other and go through the FFN for many layers, and the classification "percolates" into the FP numbers (12288 for each token in GPT-3) of the last token. **The new token is actually based on a CLASSIFICATION of the entire input**.

<img src="/assets/M-51.png" alt="drones" width="13%">

<br>


#### **1.5 The TF algorithm (QKV context computation from 2020) is still the basis of LLM AI**

The TF QKV context computation algorithm modifies the token "hidden layers" (12288 FP numbers that are called "hidden" because you can not determine what the computations do by analyzing the programmed parameters) based on other tokens (thus computing context adjustments). *[2.3.6.1b D5 tiny TF algorithm details](/2.3.6.1b-d5-tiny-tf-algorithm-details/)* (draft, WIP) explains in detail the simplest demo (its not simple) of the LLM TF QKV (context) mechanism.

<img src="/assets/M-52.png" alt="drones" width="19%">


The core of AI is not rapidly evolving. Thats one reason why AI continues to focus on ramping up brute-force computation ("scaling"). The pic below is from a video I was watching on 26.0629. That one line "key-value (KV) caches need to be maintained" explains (part of) the reason why AI needs so much memory. Google "what is a kv cache" for details. 

*QKV is still the core of LLM AI (**[video](https://youtu.be/lSDC6-BdVus?t=357)**)* <br>
<img src="/assets/kv.png" alt="drones" width="40%">


<br>

#### **1.6 AI is an incredible revolutionary engineering marvel.. for the right applications** 

Palantir in the past few years has become synonomous with cutting edge **real world** AI applications. But Palantir only recently adopted AI. 25 years ago Palantir's initial projects were for military applications **without AI**. These non-AI apps were designed as helpful assistants for decision makers, not as as a replacement for mankind. **AI later became the ultimate helpful assistant for Palantir's missions**. AI had limitations, but the benefits of AI far outweighed the negatives **when AI was applied properly**.  

<!-- 
*"...AI software will be as important as hardware, with platforms such as Palantir's Maven Smart System poised to turn massive drone sensor feeds into highly usable battlefield intelligence". [Zerohedge 26.0620](https://www.zerohedge.com/military/only-beginning-how-profit-asymmetric-warfare-boom)*. -->

*A very successful real-word application of AI* <br>
<img src="/assets/ziptiedrone2.png" alt="drones" width="23%">

<br>

#### **1.7 Falling for AI hype can cost you... dearly**

**"No more programmers"**, **"no more workers", "self-driving cars will be ready next year"**, **"we must pause AI development because its not safe"**, and **"AI already has emotions"** (that last statement was from a winner of both the Nobel and Turing prizes). If you yourself fall for such hype, it can cost you dearly.

<!-- **AI is a security risk**. The core NN in AI has what are often referred to as "hidden layers" that perform the massive brute-force number crunching to generate "intelligent" output. **It's impossible (even for AI) to determine how a NN has been programmed by analyzing the parameter settings in these layers**. -->

*An unsuccessful mission for AI*<br>
<img src="/assets/waymo.png" alt="drones" width="26%"> 

<br>

#### **1.8 AI's place in our world (not our place in AI's world)** 

Its no accident that Palantir talks straight about many aspects of AI. Palantir's business does **not demand the myth of AI intelligence**. Palantir says that **AI will not replace people, it will empower them** and that **"engineers wont go away, because their AI-enhanced expertise will be required even more in the age of AI"**. If AI was truly intelligent then AI integration would just involve connecting AI and letting it rip. But successful AI integration into any system requires extensive technical expertise. In the diagram below, the small green box (far left) represents the core legacy enterprise SW. **The core algorithms and workflows developed over decades for such systems are not going to be replaced by AI. AI is going to assist**, and in such a way that AI's unavoidable errors will not cause significant problems. 

<!-- 
 **But AI is not intelligent. AI is based 100% on deterministic binary algorithms that compute statistical probabilities. AI is an addon, a helpful assistant.** The most reliable AI systems use the smallest AI component that can provide the required functionality. -->

<!-- A recent video from one of my favorite bloggers illustrates how a lack of understanding of AI leads to a very mistaken "AI first" world view. The video [AI 落地生死战：为什么 90% 的企业软件会被重写？](https://www.youtube.com/watch?v=DlDvYe96cNY) **"The life-or-death battle for AI implementation: Why 90% of enterprise software is being rewritten"**. He is right about "90%" but not about "rewriting" (replacing) existing SW. AI is never the core logic loop in any app. **AI is always an assistant**.  -->

<!-- (there are no English audio or subtitles, but rest assured that such a service will become standard in the near future). The video talks about how major business SaaS CRM SW (such as Salesforce) is being threatened by AI.  --> 

*AI is an add-on, a helpful assistant, never in the driver's seat*<br>
<img src="/assets/M-15ccc.png" alt="drones" width="78%">

<!--
-------------------------
-------------------------
-------------------------

That video was the source of inspiration for a new **DIY [AI project](/3.3-ai-projects/)** for an **[AI project ledger](/3b.3.4-ai-proj-4-ledger/)** (basically a mini DIY Salesforce app). I asked GPT if we could make an app that would record any text messages on an encrypted ledger instead of being stored (constrained) in a DB. This would be somewhat similar to a Bitcoin ledger. All human language customer data is stored on a ledger (maybe even photos, screenshots, voice, etc). AI takes care of indexing and runtime analysis. 

<!-- The ledger records everything you ever did, all emails, all meeting notes etc. The ledger would be massive, but nowadays terabyte storage for home use is normal (the current size for the bitcoin ledger is < 1 TB!). 

*Visualization of a candidate Bitcoin block that is currently sitting in the mempool waiting to be mined (Bitcoin Ledger / Blocks / Transactions; Each rectangle is one transaction)* <br>
<img src="/assets/M-27.png" alt="drones" width="43%">

 (who paid what to whom). A Bitcoin ledger simply adds very structured encryption information that makes it impossible to alter the contents of the ledger without anyone noticing. Bitcoin does not need AI to do this, because the data structure in the ledger is fixed. 

Structured data forms the basis of many SaaS systems (similar to ontology in Palantir systems). Valuable content that does not realy fit into the ontology has be laboriously modified (by humans or with human supervision) or added as attachments. -->

<!-- #### **Now "imagine if you will..."**

(an opening line attributed to Rod Serling's **[Twilight Zone](https://en.wikipedia.org/wiki/The_Twilight_Zone)** series) such a system, but with an AI helpful assistant. All of sudden, untold millions (billions?) of customers can take the messy cryptic (human language) input from real life business processes and have AI "force feed" it into the system. -->

<br>

### **2 Core AI demos and technical concepts**

Note: The latest architectures are not introducing anything radically different from the core AI functionality of these simple demos. I recently saw a video where one of the author's of the original paper "Attention is all you need" stated that no other ground-breaking architecture has appeared since the paper was pubished.

<!--
  - **2.1 Core AI demos ([QS](/0-qs/))**. You need hands-on demo experience before you can really understand the core AI concepts.
  - **2.2 Core AI [concepts](/0b-demos/)**. The most important concept is that there is no "I"  (no intelligence) in "AI".  -->

<br>

#### **2.1 Core AI demos ([QS](/0-qs/))**

**You can only learn how AI works by doing code demos** (or at least studying the code). **Code does not lie**. 

<!-- Chatbots are programmed to inundate you with hype and AI lingo. GPT often remarks about my habit of wanting to describe AI from a **mechanistic** viewpoint. My response has always been **"of course, AI is mechanistic**. I went down so many rabbit holes when studying AI. **The ONLY way to understand AI is by doing examples. -->

*A simple NN **[demo](/2.1.2-classifier-nn/)** of the core of AI*<br>
<img src="/assets/M-02.png" alt="drones" width="22%">


**NOTE: About my use of "tiny" demos and analysis based on Alex-Net CNNs (2012) and GPT-3 (2020) throughout this site**. The core of AI is not rapidly evolving. The simple demos on this site are the best demos if you want to understand the core mechanics of how AI really works. For example, page **[2.3.6.1b D5 tiny TF algorithm details](/2.3.6.1b-d5-tiny-tf-algorithm-details/)** (draft, WIP) explains in detail the simplest demo (its not simple) of the LLM TF QKV (context) mechanism  

*QKV is still the core of LLM AI (**[video](https://youtu.be/lSDC6-BdVus?t=357)**)* <br>
<img src="/assets/kv.png" alt="drones" width="40%">



<!--
*Code for **[NN](/2.1.1-predictive-nn-01-sine/)** definition (left) and training (right)*<br>
<img src="/assets/M-14.png" alt="desc" width="60%"> -->

<br>

#### **2.2 Core AI technical [concepts](/0b-demos/)**

This section focuses on a conceptual understanding of the technical aspects (especially the algorithm details) of the demos. 

<!-- **An AI LLM is first and foremost a man <> machine interface with hard coded language skills and memory**. A human chats with an LLM via tokens (words). Human eyesight and intelligence convert these tokens into thoughts (an amazing little-understood process). **The LLM internal agent (a traditional CPU-based algorithm) controls the transformer (TF) and interfaces with the outside world. The TF generates a token sequence based on the input tokens (nothing more).** The closely synchronized teamwork of the internal agent and the TF result in a convincing simulation of intelligent thought. -->

<!-- On the LLM side, tokens are converted by the internal agent to FP numbers before being input to the LLM transformer (TF). An LLM sees nothing and has no thoughts. It only crunches numbers. **AI chatbots only say what they are programmed to say**. -->

*The similarities of the CNN and TF algorithms*<br>
<img src="/assets/00-MAIN.png" alt="drones" width="58%"> 

<!--
<img src="/assets/M-09.png" alt="drones" width="58%"> -->



<!-- *Human (left), LLM agent (center), and LLM transformer (right)*<br>  
<img src="/assets/M-11.png" alt="drones" width="31%"> -->

<br>

### **3 AI deep dive (code)**

<!-- iptieAI methodically attacks the complexity of the AI ecosystem in a very mechanistic fashion (because AI is first and foremost a mechanical algorithms). --> 

The code demos are organized into the 4 groups shown in the diagram below.
- **(2) Core [NNs](/2_models/)**.
- **(2b) [Models](/2b_models/)** that package core NNs for reuse.
- **(3) External [agents](/3_agents/)** that provide an interface between models (helpful assistants) and legacy systems.
- **(3b) Real-world [projects](/3.3-ai-projects/)**.

*The ZiptieAI deep dive takes you methodically through the entire AI stack*<br>
<img src="/assets/M-15.png" alt="drones" width="78%">


<!-- <img src="/assets/tf_S1-S6.png" alt="desc" width="40%"> 
<img src="/assets/0_projects2.png" alt="drones" width="35%"> -->

<br>

### **4 Anticipation of the AI future**

AI has a big future even after the pre-IPO hype is over. **Those who understand how to integrate AI into their own workflows will benefit the most. ZiptieAI has a mission to help myself (and others) stay ahead of the AI curve**. In the near future, AI integration skills will be required in all business segments (just like with the PC 40 years ago). This work will require a massive number of tech workers who, empowered by AI tools, will integrate AI **as a helpful assistant** into all areas of life.  

*The helpful assistant of the future*<br>
<img src="/assets/M-10.png" alt="desc" width="35%"> 


<br>

26.0701 (v1 26.0611)

<!-- *A successful mission for AI (left) and not so successful mission (right).* <br>
<img src="/assets/ziptiedrone2.png" alt="drones" width="23%"> <img src="/assets/waymo.png" alt="drones" width="26%">  -->


<!-- #### **3.1.1b Tiny NN demo (D2ccc) TRAINING**

(WIP) 

<br> 

#### **3.1.2 Tiny CNN (D4)**

See [2.2.1 D4 CNN image classifier](https://ziptieai.com/2.2.1-d4-cnn-image-classifier/) and (for details) [2.2.1b D4 CNN algorithm details](https://ziptieai.com/2.2.1b-d4-cnn-algorithm-details/). -->

<!--
*An image classifier.*<br>
<img src="/assets/M-07.png" alt="drones" width="46%">
<img src="/assets/M-08.png" alt="drones" width="20%">
-->

<!-- A good example to study before doing the Tiny CNN demo.

Diagram from page [2.2.1b D4 CNN algorithm details](https://ziptieai.com/2.2.1b-d4-cnn-algorithm-details/).

<img src="/assets/M-06.png" alt="drones" width="46%"> 


<br>

#### **3.1.3 Tiny TF (D5)** -->

<!-- 
*A transformer that prints out "hello world hello world hello world ...."*<br>
<img src="/assets/M-09.png" alt="drones" width="70%">
-->

<!-- 
<br>

The QS also includes
- **[3.2 Models](/2b_models/)** (with API). The agent and the NN are typically packed into a **model** that has an API that makes it possible for existing software to **use the model as a "helpful" assistant**. 
- **[3.3 Agents](/3_agents/)**. External (not LLM internal) agents provide 
  - reliable workflows built around models, tools, and automation. 
  - tolerance of AI faults and unpredictable outputs
-->
<!-- 
(whatever the official term is; the human brain is definitely not the same).
 **Trust but verify** anything you get from AI. Verify means investigating, doing demos.
-->



<!-- I was quite confident in my assessment of the Palantir CTO's speech because I've built many AI demo projects. But the most insight I got from "simple" "tiny" demos. 

Such **demos are the core of the ZAI website, and are organized into 3 sections:**

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

<!-- <br>

#### **3.1.1 Tiny NN demo (D2ccc)** 

*"Inference" means normal run-time operation. Generating output from input. Training is described next.*  -->

<!-- The AI gurus, titans, employees (with stock options), and their financial backers all know they will get rich with the coming AI IPOs. The success of these IPO's depends greatly on the public not understanding certain aspects/myths about AI. *Recently some very interesting details of these IPOs have come to light that suggest a coordinated effort to mislead the public (I won't talk about because so many others are).* -->

<!-- But even Palantir has its own hype. Watch the first (English) half of this fascinating **[interview of Palantir CTO](https://www.youtube.com/watch?v=lcUHDsA5lzc)**.  Pure unadulterated hype. I could not help but laugh at every other sentence from the CTO.  *Details about video soon.....* 
The reasons for the hype:
- Money. That's the motivation for any successful company. 
- They have a product that noone understands. Just like Pfizer a few years ago.
- People dont understand the science. Just like with Covid and mRNA.
- There is no incentive to promote anything but a merely superficial understanding of AI among the general public (and government officials). 
#### **AI has no intelligence (and therefore is never in control)**
Think for a minute what AI integration into a companys digital infrastructure would be like if AI was truly intelligent. You just put AI in control of the existing digital infrastructure and done. **Turnkey integration.** **But AI is not intelligent. AI is based 100% on deterministic binary algorithms that compute statistical probabilities.** Therefore, it can not be the central loop (NNs are not control loops). **AI is an addon.** 
- Non-AI code bases have to provide any deterministic functions such as control, validation, permissions, execution, logging, and safety. 
- AI must be custom built into the system by those who understand **AI's significant risks and limitations** (thats why Palantir employs **forward deployed engineers** (FDEs)).
- The most reliable AI systems use the smallest AI component that can provide the required functionality.

#### **AI is a security risk**
AI is the gatekeeper of the source of truth. But the safety and reliability of that "truth" is only as good as reputation of whoever programmed ("trained") the AI model. The core NN in AI has what are often referred to as "hidden layers" (HLs). These are the layers in the NN that perform number crunching to generate "intelligent" output. **Understanding what those HLs do by looking at the parameter values is impossible**. You can not tell what have been programmed into the AI core. -->

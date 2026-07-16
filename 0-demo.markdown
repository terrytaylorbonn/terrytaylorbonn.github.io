---
layout: page
title: Hack
permalink: /0-demo/
---

<br>

*This page rewritten 26.0714 (WIP)*

<br>


To work effectively with AI, the most important thing is to understand that **"Artificial intelligence" is a hack**. But an **extremely valuable hack when engineered into target systems properly**. That's what ZiptieAI is all about.

**TOC**
- 1 “what does jely made of?”
- 2 The “artificial intelligence” hack (the TF half of an LLM)
- 3 Google: “what does it mean to hack something together?”
- 4 The hack in detail: Astounding engineering (GPT-3 transformer (TF))
- 5 TF GPU-based algorithms are 100% deterministic
- 6 LLM agent + transformer = the hack becomes intelligent
- 7 The glorious future of the simulated intelligence hack

<br>

## **1 "what does jely made of?"**

**Google answers "The ingredients in jelly depend on the type...."**. The technical wizardry behind that simple answer is amazing. That's AI. That has changed our world (many of us have forgotten what it was like when all input to computers had to be be perfect).

Without AI a computer could not answer such a question.  A procedural program would have to 
- check all possible combinations of letters against all possible meanings and contexts.
- encode all possible topics. 
- account for all possible grammar formulations and errors.
- misspelled words.
- bad punctuation.  

A procedural program can do simple things like checking capital/lower-case letter combos, etc, but that's about it.  Imagine what would be required for what AI does now (complete discussions, etc). Impossible without AI.

for the "jely" demo, The following diagram (left to right) shows how AI does it (MODIFY DIAGRAM). 
- The main system is YOU and your browser.
- External agent is all the logic on the Google side, that interface between you and the LLM.
- 2b Model is Gemma, etc. Has internal agent (interface between outside model and TF) and TF.
- **2 TF transformer is where the AI magic happens. Its all matrix math on GPUs.** 

<img src="/assets/hack-05.png" alt="drones" width="75%">


PS: 
- **The true TF magic (there's so much magic in a TF) is that if the input does not match any of the example ("training") data used to program ("train") the TF, then it will still find the closest SEMANTIC (MEANING) MATCH. So you dont have to worry about covering all possible examples**
- **but the more examples you train on the better the results; thats why the race is on for scaling and massive GPU computing; thats why nuclear power is "safe and effective"** all of a sudden, now that the tech titans need massive amounts of electricity).
- And if its not programmed into the TF, the model can tell the external agent to find the required text (search) and then process the text into response. Amazing.  
- the model can also simulate thinking, planning, creating subtasks.. all from the example text it was programmed on (and with the complex logic of the internal agent that controls the model).


<br>

## **2 The "artificial intelligence" hack (the TF half of an LLM)**

(the other half is the internal agent; together they make up an LLM)

The following diagram shows what an LLM TF (and CNN, NN in general) really does. You often read that it computes the new token from the last token. Nonsense (the computed data for the new token ends up in the last token, but this data was computed from all tokens). The TF runs a complex pattern matching algorithm that generates an output that classifies the input. Matrix math is used to compute the most likely token for that classification output (12288 FP-16 #s) (1 token out of ~50K tokens).

**What is inside the TF is an engineering marvel**. But intelligence? Nonsense (and the AI gurus all very well aware of this fact). **As a source of intelligence, its a crude brute-force hack**. Thats works well enough to make it extremely valuable.

<img src="/assets/hack-08.png" alt="drones" width="40%">

<br>

## **3 Google: "what does it mean to hack something together?"**

**Answer:** "To hack something together means to quickly assemble a prototype, program, or physical object using whatever materials and methods are immediately available. .... 

Key Characteristics
- **Speed Over Polish**: The primary goal is functionality. .....
- **Unconventional Methods**: It involves using parts or code in ways they were not originally intended to be used (colloquially known as a "kluge" or "jerry-rigging"). 
- **Tech Origins**: Heavily used in software development to describe a quick, temporary script or "dirty code" written to test a feature or bypass a bug. 

While sometimes viewed as a negative sign of poor planning, it is often a celebrated, creative process in "hackathons" where building a working concept rapidly is the entire point. 
- **This is what AI has been for over half a century... technical experiment, a hack that only recently (thanks to powerful GPUs that could perform the brute-force computations) worked well enough to market as "intelligent"**.
- **But the hack performs some vital functions extremely well, which makes it valuable.**
- **The challenge: Project Engineering so that it works well enough for specific applications.**

Note: **PC Multi-tasking is not a hack**. Computers may not actually run all tasks concurrently, but the net effect for a human is multi-tasking. **The net effect of TF's for humans IS NOT INTELLIGENCE**. The AI titans do all they can to make them appear to be intelligent, and they claim they are possibly intelligent (a false statement they are well aware of). 

<br>

## **4 The hack in detail: Astounding engineering (GPT-3 transformer (TF))**

*Note: Even the latest LLM TFs use the same basic algorithm*.

TF is the core of AI. The latest models are basically the same.
- Loop X inputs 2048 token embeddings (12288 FP16 #s for each token)
- The TF runs > 1 million billion computations to compute the next token (these computations are 100% deterministic; they will always give the same results for the same inputs).
- At the end of 96 computational layers the 12288 FP16 #s  for the last token are the classification of the pattern formed by (up to) 2048 input embeddings. 
- The TF has 175 billion parameters used to compute the pattern. These parameters were programmed by special SW that took massive input examples, and for each example (1) compared the output to the desired and (2) adjusted slightly the params to improve the accuracy for the one input example. Even at computer speeds, such training can take weeks. 
- The number of pattern combinations represented by the training data is beyond imagination.
- Yet the possible number of combinations are far greater. 
- The TF works because the input tokens are a combination that the TF was never trained on, but the TF algorithm will match the input to the closest matching input combo the TF was programmed ("trained") on.

***The hack: The transformer (LLM core) computes a numerical probability of possible classifications of the (numerical) input combination (an LLM sees nothing, has no thoughts, no emotions, etc etc etc)***<br>
<img src="/assets/hack-01.png" alt="drones" width="45%">

<br>

NOTE the following:  
- The output 12288 FP #s are a classifier. They are used to select a new token that is (out of ~50K tokens, the vocabulary) the best classifier of the input sequence. Note: TF's are sometimes programmed to not select the best match, because this will give the impression of non-deterministic intelligence, not binary computation. 
- After that, the new token is appended to the input. To compute the next token (loop X+1) the calculations start from 0 (KV calculations can be reused). This hack (one of many) must be done because of algorithm limitations (nobody has figured out a better algorithm). 
- The TF can run on a CPU, but that is extremely slow. The TF computations are 100% deterministic, but they are not procedural like for most CPU programs (no branching, etc). TF algorithms are shotgun algorithms (I call them that, inspired by "shotgun" homes that were thin and long and just ran from front to back).  Data just races through the GPU from start to finish.


<br>

## **5 TF GPU-based algorithms are 100% deterministic**

The following is an example of the python code that defines the structure and training algorithm of a very simple NN.  Such a NN runs on clocked binary circuits and will always output the EXACT same result for the same input. **The inputs and outputs are ONLY FP (floating point) numbers. NNs are pure number crunchers.**

<img src="/assets/M-14.png" alt="desc" width="60%"> 

The AI simulation of intelligence started to seem intelligent only recently after the computational hardware reached the performance level required to (1) generate responses at least as fast as a human could read them and (2) with a level of accuracy that (at least initially) convinced users that AI had some level of genuine intelligence. But AI has no intelligence. **AI algorithms and the circuitry they run on have little similarity to human brain neurons.** You could run the most sophisticated LLMs on GPUs based on electro-mechanical relays. It might require its power plant and take years to answer a prompt, but it is theoretically possible.  

*Electro-mechanical relay*<br>
<img src="/assets/relay.png" alt="drones" width="12%">

<br>

## **6 LLM agent + transformer = the hack becomes intelligent**

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


<!-- ### **1 Basic AI concepts** 

**The engineering genius behind AI is amazing**. But **building successful AI applications requires a basic understanding of what AI really is**.
- 1.1 AI = deterministic algorithms running on digital HW
- 1.2 LLM agent + transformer = simulated intelligence
- 1.6 AI is an incredible revolutionary engineering marvel.. for the right applications
- 1.7 Falling for AI hype can cost you... dearly
- 1.8 AI's place in our world (not our place in AI's world)

 - 1.1 AI = deterministic algorithms running on digital HW
- 1.2 There is no "I" (intelligence) in AI
- 1.3 (1.2b) So what is AI? AI = classification, pattern matching (simple NN)
- 1.4 (1.2c) Variations of the simple NN theme (CNNs, TFs)
- 1.5 (1.2d) KV saved (HACKS) (cant get better algo to work)
- 1.6 (1.4) AI is an incredible revolutionary engineering marvel.. for the right applications
- 1.7 (1.3) Falling for AI hype can cost you... dearly
- 1.8 (1.5) AI's place in our world (not our place in AI's world)
-->


<br>

## **7 The glorious future of the simulated intelligence hack** 

<br>

#### **7.1 The hype and the costly (to end customer) failures**

**"No more programmers"**, **"no more workers", "self-driving cars will be ready next year"**, **"we must pause AI development because its not safe"**, and **"AI already has emotions"** (that last statement was from a winner of both the Nobel and Turing prizes). If you yourself fall for such hype, it can cost you dearly.

- *[Palantir CEO火力全开，场面控制不住了！](https://www.youtube.com/watch?v=feUFT1Q-oBA)*
- *[zerohedge.com/ai/something-has-gone-completely-wrong-palantirs-alex-karp-goes-ballistic-openai-anthropic](https://www.zerohedge.com/ai/something-has-gone-completely-wrong-palantirs-alex-karp-goes-ballistic-openai-anthropic)*

<!-- **AI is a security risk**. The core NN in AI has what are often referred to as "hidden layers" that perform the massive brute-force number crunching to generate "intelligent" output. **It's impossible (even for AI) to determine how a NN has been programmed by analyzing the parameter settings in these layers**. -->

*An unsuccessful mission for AI*<br>
<img src="/assets/waymo.png" alt="drones" width="26%"> 

<br>




#### **7.2 But AI is an incredible revolutionary engineering marvel.. for the right applications** 

Palantir in the past few years has become synonomous with cutting edge **real world** AI applications. But Palantir only recently adopted AI. 25 years ago Palantir's initial projects were for military applications **without AI**. These non-AI apps were designed as helpful assistants for decision makers, not as as a replacement for mankind. **AI later became the ultimate helpful assistant for Palantir's missions**. AI had limitations, but the benefits of AI far outweighed the negatives **when AI was applied properly**.  

<!-- 
*"...AI software will be as important as hardware, with platforms such as Palantir's Maven Smart System poised to turn massive drone sensor feeds into highly usable battlefield intelligence". [Zerohedge 26.0620](https://www.zerohedge.com/military/only-beginning-how-profit-asymmetric-warfare-boom)*. -->

*A very successful real-word application of AI* <br>
<img src="/assets/ziptiedrone2.png" alt="drones" width="23%">

<br>

#### **7.3 AI's place in our world (not our place in AI's world)** 

Its no accident that Palantir talks straight about many aspects of AI. Palantir's business does **not demand the myth of AI intelligence**. Palantir says that **AI will not replace people, it will empower them** and that **"engineers wont go away, because their AI-enhanced expertise will be required even more in the age of AI"**. If AI was truly intelligent then AI integration would just involve connecting AI and letting it rip. But successful AI integration into any system requires extensive technical expertise. In the diagram below, the small green box (far left) represents the core legacy enterprise SW. **The core algorithms and workflows developed over decades for such systems are not going to be replaced by AI. AI is going to assist**, and in such a way that AI's unavoidable errors will not cause significant problems. 

<!-- 
 **But AI is not intelligent. AI is based 100% on deterministic binary algorithms that compute statistical probabilities. AI is an addon, a helpful assistant.** The most reliable AI systems use the smallest AI component that can provide the required functionality. -->

<!-- A recent video from one of my favorite bloggers illustrates how a lack of understanding of AI leads to a very mistaken "AI first" world view. The video [AI 落地生死战：为什么 90% 的企业软件会被重写？](https://www.youtube.com/watch?v=DlDvYe96cNY) **"The life-or-death battle for AI implementation: Why 90% of enterprise software is being rewritten"**. He is right about "90%" but not about "rewriting" (replacing) existing SW. AI is never the core logic loop in any app. **AI is always an assistant**.  -->

<!-- (there are no English audio or subtitles, but rest assured that such a service will become standard in the near future). The video talks about how major business SaaS CRM SW (such as Salesforce) is being threatened by AI.  --> 

*AI is an add-on, a helpful assistant, never in the driver's seat*<br>
<img src="/assets/M-15ccc.png" alt="drones" width="78%">

<br>

#### **7.4 A window to the AI future**

AI has a big future even after the pre-IPO hype is over. **Those who understand how to integrate AI into their own workflows will benefit the most. ZiptieAI has a mission to help myself (and others) stay ahead of the AI curve**. In the near future, AI integration skills will be required in all business segments (just like with the PC 40 years ago). This work will require a massive number of tech workers who, empowered by AI tools, will integrate AI **as a helpful assistant** into all areas of life.  


*The helpful assistant of the future*<br>
<img src="/assets/M-10.png" alt="desc" width="35%"> 

<!--
*The future man-machine interface ([NL](/nl/))*<br>
<img src="/assets/nl-01.png" alt="desc" width="15%"> -->

<br>



26.0716 (v1 26.0714 (0628))


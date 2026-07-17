---
layout: page
title: Hack
permalink: /0-demo/
---

<br>

<!-- *Rewritten 26.0714 (WIP)* -->

The most important thing to understand about AI is that **AI is a hack. An extremely valuable hack** (when used properly). 

**TOC**
- 1 “what does jely made of?”
- 1b The main components of an AI computational system
- 2 The “artificial intelligence” hack (the TF half of an LLM)
- 3 Google: “what does it mean to hack something together?”
- 4 The hack in detail (the amazing engineering of the GPT-3 transformer)
- 5 TF GPU-based algorithms are 100% deterministic
- 6 The LLM internal agent is just as important as the TF
- 7 The very bright future of simulated intelligence

<br>

### **1 "what does jely made of?"**

**Google answers "The ingredients in jelly depend on the type of...."**.

To build a computer that can answer such a simple question (especially with spelling and grammar errors) is a massive engineering challenge, because **computers have absolutely no intelligence**. They can only compute numbers. **Geoffery Hinton, who received the Turing and Nobel prizes for his ground breaking work on AI, stated many times that he believed AI already had emotions. He knew what he was saying was not true** (my non-AI engineering background was more than enough to understand this, and such ridiculous claims about AI from Hinton and other experts during recent years was one of reasons I shifted the focus of ZiptieAI to LLMs). He has always understood in detail how AI really works, and he understood that the vast majority of people did not. But people are slowly learning the facts about AI, which is perhaps why Hinton recently admitted that his statement about emotional computing machines was a mistake.

**But the massive engineering effort to build AI computers is well worth the investment**. The technical wizardry behind such a simple answer is rapidly changing our world. Many of us (8 billion all over the world) have forgotten (or never knew) what it was like when all input to computers had to be be perfect. When a search engine simply returned articles with the most keyword matches. Without AI a computer could not answer messy human language questions.  A procedural program (traditional CPU based languages like Python, Java, etc) would have to 
- Detect all possible topics. 
- Check all possible combinations of letters against all possible meanings and contexts.
- Account for all possible grammar formulations and errors (misspelled words, bad punctuation, etc).  

A procedural program can do simple things like checking capital/lower-case letter combos, etc, but that's about it.  Imagine what would be required for what AI does now (complete discussions, etc). Impossible without AI.

<br>

### **1b The main components of an AI computational system**

The following diagram shows the main components of the typical AI system.
- The main system (left) could be you/browser or a company's vitally important non-AI computer systems.
- The external agent is all the logic that interfaces between the main system and the AI helpful assistant.
- The LLM has an internal agent and TF. The internal agent is the interface between the outside world and the TF.
- **The TF (transformer) is where the AI magic happens (matrix math computation on GPUs).** 

<img src="/assets/hack-05.png" alt="drones" width="75%">



<br>

### **2 The "artificial intelligence" hack (the TF half of an LLM)**

*(the other half is the internal agent; together they make up an LLM)*<br>
<img src="/assets/M-11b.png" alt="drones" width="27%"><br>

The following diagram summarizes the core function performed by an LLM TF. You often read that it computes the new token from the last token. Nonsense. The computed data for the new token ends up in the last token, but this data was computed from all tokens. The TF runs a complex pattern matching algorithm on the last token embeddings (12288 FP16 #s in GPT-3) that generates an output that is a classification of the input (used to select 1 token out of ~50K tokens as the next token).

**The TF is an engineering marvel** that has applications everywhere in the digital world. But intelligence? Nonsense. Its a brute-force hack using matrix math, not neurons (the term "neural network" is a marketing term, convincing because the matrix math diagrams look like a crude simplification of a neural net). 

<img src="/assets/hack-08.png" alt="drones" width="40%">

<br>

### **3 Google: "what does it mean to hack something together?"**

**Answer:** "To hack something together means to quickly assemble a prototype, program, or physical object using whatever materials and methods are immediately available. ... Key Characteristics are
- **Speed Over Polish**: The primary goal is functionality. .....
- **Unconventional Methods**: It involves using parts or code in ways they were not originally intended to be used (colloquially known as a "kluge" or "jerry-rigging"). 
- **Tech Origins**: Heavily used in software development to describe a quick, temporary script or "dirty code" written to test a feature or bypass a bug. 

While sometimes viewed as a negative sign of poor planning, it is often a celebrated, creative process in "hackathons" where building a working concept rapidly is the entire point. 

<br> 

-----

<br>

**This is what AI has been for over half a century. A hack that only recently (thanks to powerful GPUs that could perform the brute-force computations) worked well enough to be marketed as "intelligent"**. The hack works well enough in certain situations that are extrememly useful to mankind. The challenge is building systems that exploit AI capabilities while minimizing its limitations. A good analogy with AI is the multi-tasking feature of everyday computers. Computers may not actually run all tasks concurrently, but computers run fast enough that the net effect is real multi-tasking. **The net effect of AI is not is not intelligence**. Its more like (1) a knowledge store with (2) language abilities.  

<br>

### **4 The hack in detail (the amazing engineering of the GPT-3 transformer)**

The diagram below summarizes how the TF in GPT-3 works (even the latest and greatest "frontier" LLM TFs use the same basic algorithms as in GPT-3):
- Loop X inputs 2048 token embeddings (12288 FP16 #s for each token)
- The TF runs over 1 million billion computations to compute the next token (these computations are 100% deterministic; they will always give the same result for the same inputs).
- At the end of 96 computational layers the 12288 FP16 #s for the last token are the classification of the entire input pattern (formed by up to 2048 input embeddings). 
- The TF has 175 billion parameters used to compute the pattern. These parameters were programmed by special SW that took a massive set of input "training" examples, and for each example (1) compared the output to the desired output and (2) adjusted slightly the parameters to improve the accuracy for the current input example. Even at computer speeds, such training can take weeks. 
- The number of pattern combinations represented by the training data is beyond imagination.
- Yet the possible number of combinations are still far greater than the input examples. 
- The TF still works because if the input tokens are a combination that the TF was never trained on, the TF algorithm will match the input to the closest matching input combination the TF was programmed ("trained") on.

*The hack: The TF computes a numerical classification of the numerical input (an LLM sees nothing, has no thoughts, no emotions, etc etc etc)*<br>
<img src="/assets/hack-01.png" alt="drones" width="45%">

<br>

Even more hack details for the really curious:  
- The classifier is used to select the new token out of a ~50K token vocabulary. 
- TFs are sometimes programmed to not select the best match, because this will give the impression of non-deterministic intelligence. 
- The new token is appended to the input. To compute the next token (loop X+1) the calculations starts from 0 (all previous calculations are reset with possible exception of some KV calculations). This hack (one of many) must be done because of algorithm limitations (nobody has come up with a better algorithm). 
- The TF can run on a CPU, but that is extremely slow. TF computations are 100% deterministic, but they are not procedural as in CPU programs (no branching, etc). Data races through the GPU from start to finish with no procedural branching.
- The true magic of the TF is that if the input does not exactly match any of the example ("training") data used to program ("train") the TF, **the TF will still find the closest semantic (meaning) match.** 
- **The more examples you train the TF on, the better the inference (response) results will be**. Thats why the focus is on scaling and massive GPU computing (and the required power sources).
- And if the required info has not been programmed into the TF, the model can tell the external agent to find the required text (the TF's only interface to the outside world is to the internal agent via tokens; the iAgent feeds this text to the TF as part of a prompt).  
- The model can also simulate thinking, planning, creating subtasks, etc (if the model TF was programmed on such example text pattens). 


<br>

### **5 TF GPU-based algorithms are 100% deterministic**

The following is an example of the python code that defines the structure and training algorithm of a very simple NN.  Such a NN runs on clocked binary circuits and will always output the EXACT same result for the same input. **The inputs and outputs are ONLY FP (floating point) numbers. NNs are pure number crunchers.**

<img src="/assets/M-14.png" alt="desc" width="60%"> 

The AI simulation of intelligence started to seem intelligent only recently after the computational hardware reached the performance level required to (1) generate responses at least as fast as a human could read them and (2) with a level of accuracy that (at least initially) convinced users that AI had some level of genuine intelligence. But AI has no intelligence. **AI algorithms and the circuitry they run on have little similarity to human brain neurons.** You could run the most sophisticated LLMs on GPUs based on electro-mechanical relays. It might require its own power plant and take years to answer a prompt, but it is theoretically possible.  

*Electro-mechanical relay*<br>
<img src="/assets/relay.png" alt="drones" width="12%">

<br>

### **6 The LLM internal agent is just as important as the TF**

LLM AI is based not only on the TF, but also on the **Internal agent (iAgent)** that sends and receives tokens to/from the TF. The iAgent is the core control loop, a **procedural program** (usually confusingly referred to as **the** deterministic program; the problem is the GPU is also 100% deterministic). The iAgent has an API for external access. The iAgent is specifically programmed to work with a particular TF. 


<!-- - **Transformer (TF)** generates response tokens based on the input tokens. The actual TF algorithm only computes FP numbers. **The TF computational process is a straight shot (not procedural)**. The TF computes a classification of the entire input. This classification is used to select the next token. That new token is added to the input. The TF is reset, and the process for the next token starts. This process continues until the TF stops or the iAgent comands a stop.  Note: TF algorithms are referred to as "neural" networks because the diagrams for NN matrix math look like diagrams that could be considered similar to those for biological neural networks.   
 -->

*The LLM internal agent (left) and TF (right)*<br>
<img src="/assets/M-15-2bbb.png" alt="drones" width="63%">

<!-- 
*The LLM agent and transformer are the inseparable duo that simulates intelligence*<br>
<img src="/assets/M-11b.png" alt="drones" width="33%"><br>
xxxx **This site takes a very down-to-earth mechanistic approach to understanding AI. Thats because AI is based on mechanistic binary matrix math algorithms that run on binary circuits.** 
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

### **7 The very bright future of simulated intelligence** 

**AI is unfortunately a lot of hype**. "No more programmers", "no more workers", "self-driving cars will be ready next year", "we must pause AI development because its not safe", and "AI already has emotions" (that last statement was from a winner of both the Nobel and Turing prizes). If you yourself fall for such hype, it can cost you dearly.

<!-- - *[Palantir CEO火力全开，场面控制不住了！](https://www.youtube.com/watch?v=feUFT1Q-oBA)*
- *[zerohedge.com/ai/something-has-gone-completely-wrong-palantirs-alex-karp-goes-ballistic-openai-anthropic](https://www.zerohedge.com/ai/something-has-gone-completely-wrong-palantirs-alex-karp-goes-ballistic-openai-anthropic)*
**AI is a security risk**. The core NN in AI has what are often referred to as "hidden layers" that perform the massive brute-force number crunching to generate "intelligent" output. **It's impossible (even for AI) to determine how a NN has been programmed by analyzing the parameter settings in these layers**. -->

*An unsuccessful application of AI*<br>
<img src="/assets/waymo.png" alt="drones" width="26%"> 


**But AI is an revolutionary engineering marvel... for the right applications**. Palantir in the past few years has become synonomous with cutting edge **real world** AI applications. But Palantir only recently adopted AI. 25 years ago Palantir's initial projects were for military applications **without AI**. These non-AI apps were designed as helpful assistants for decision makers, not as as a replacement for mankind. **AI later became the ultimate helpful assistant for Palantir's mission software**. AI had limitations, but **the benefits of AI far outweighed the drawbacks when AI was applied properly**.  

<!-- *"...AI software will be as important as hardware, with platforms such as Palantir's Maven Smart System poised to turn massive drone sensor feeds into highly usable battlefield intelligence". [Zerohedge 26.0620](https://www.zerohedge.com/military/only-beginning-how-profit-asymmetric-warfare-boom)*. -->

*A very successful real-world application of AI* <br>
<img src="/assets/ziptiedrone2.png" alt="drones" width="23%">

Palantir says that **AI will not replace people, it will empower them** and that **"engineers wont go away, because their AI-enhanced expertise will be required even more in the age of AI"**. If AI was truly intelligent then AI integration would just involve connecting AI and letting it rip. But successful AI integration into any system requires extensive technical expertise. In the diagram below, the small green box (far left) represents the core legacy enterprise SW. **The core algorithms and workflows developed over decades for such systems are not going to be replaced by AI. AI is going to assist**, and in such a way that AI's unavoidable errors will not cause significant problems. That requires some pretty sophisticated engineering in the external agent (the red square below). 

<!--  **But AI is not intelligent. AI is based 100% on deterministic binary algorithms that compute statistical probabilities. AI is an addon, a helpful assistant.** The most reliable AI systems use the smallest AI component that can provide the required functionality. -->
<!-- A recent video from one of my favorite bloggers illustrates how a lack of understanding of AI leads to a very mistaken "AI first" world view. The video [AI 落地生死战：为什么 90% 的企业软件会被重写？](https://www.youtube.com/watch?v=DlDvYe96cNY) **"The life-or-death battle for AI implementation: Why 90% of enterprise software is being rewritten"**. He is right about "90%" but not about "rewriting" (replacing) existing SW. AI is never the core logic loop in any app. **AI is always an assistant**.  -->
<!-- (there are no English audio or subtitles, but rest assured that such a service will become standard in the near future). The video talks about how major business SaaS CRM SW (such as Salesforce) is being threatened by AI.  --> 

*AI is an add-on, a helpful assistant, never in the driver's seat*<br>
<img src="/assets/M-15ccc.png" alt="drones" width="78%">

**AI has a big future. Those who understand how to integrate AI into their own workflows will benefit the most**. In the near future, AI integration skills will be required in all business segments (just like with the PC 40 years ago). This work will require a massive number of tech workers who, empowered by AI tools, will integrate AI **as a helpful assistant** into all areas of life.  

*The helpful assistant of the future*<br>
<img src="/assets/M-10.png" alt="desc" width="35%"> 

<!-- *The future man-machine interface ([NL](/nl/))*<br>
<img src="/assets/nl-01.png" alt="desc" width="15%"> -->

<br>

26.0717 (v1 26.0714 (0628))

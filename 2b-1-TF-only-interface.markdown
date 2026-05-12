---
layout: page
title: "1 The requirement for a human-language <> computer interface"
permalink: /2b-1-TF-only-interface/
---

<br>


- 1.1 Requirement: Interface human language and computer worlds
- 1.2 Equations (deterministic) work for many things
- 1.3 Equations (deterministic) dont work for human interaction
- 1.4 "Deterministic" computer algorithms
- 1.5 Transformer UFA solution
- 1.6 Viable / nonviable applications of UFA


<br> 

#### **1.1 Requirement: Interface human language and computer worlds** 

We need a computational unit that can interact using human language. The very idea that binary machines are intelligent is ridiculous (and leads to bad engineering designs). *I try to add diagrams for every section because humans quickly get the gist of a diagram; for AI diagrams are a massive challenge to interpret.*

**(1) Human language is far more complex than computer interactions**. 
We are intelligent. Our writing system is designed with that in mind. We don't write in a predictable manner, and our thoughts are incredibly complex. We also make spelling mistakes and abbreviations. No problem for us. 

*Human languages vs computer languages ([video](https://www.youtube.com/watch?v=zulOvXlg2kk))* <br>
<img src="/assets/1.1-1_hlang_mlang.png" alt="drones" width="55%"> 

**(2) But the LLM is very fast and can be scaled and is native to the digital worlds.**
And the digital world is vitally important. It can do many things vastly more efficiently than humans. **But interfacing these 2 worlds is complex**. We need a computational engine residing in a computer that can 
- Replicate human interaction mechanisms (language) 
- Store "common" word responses for a vast number of submitted prompts.

*Human language prompt + agent instructions -> LLM response (compatible with Agent)*<br>
<img src="/assets/1.1-3_interface_2_worlds.png" alt="drones" width="60%"> 

**(3) This interface will be an approximation (not safe for many applications)**.
Humanoids in the home, FSD on the streets. You are mixing 2 worlds that dont belong together:
- Humans who see, hear, touch, smell, see, have consciousness, feelings, etc. This defines everything thing they do, their complex interactions.
- Machines based 100% on 100% binary computation. They see nothing, have no thoughts, etc. They do ONLY what they are programmed to do.
- **Machines do not "hallucinate". Their algorithms fail** (harmless in a chatbot).

*Humanoid in the kitchen.. what could go wrong?*<br>
<img src="/assets/1.1-4_humanoid_home.png" alt="drones" width="20%"> 

<br> 

#### **1.2 Equations (deterministic) work for many things** 

Examples from the drone world. 

**(1) Kalman (filter) equations for predicting movement with limited info.** 
They store the basic reality of movement. But is that how the human mind really tracks objects, predicts movement? The human version is more complex (not equations).

<img src="/assets/1.2_kalman.png" alt="drones" width="30%"> 

**(2) PID controller.**  
Computes how moving objects can be controlled with inputs (in a perfect environment). Humans can also steer objects quite well, and human thinking is probably more complex (not equations). 

<img src="/assets/1.2_PID.png" alt="drones" width="30%">  <img src="/assets/1.2_PID2.png" alt="drones" width="40%"> 


**(3) FFT's are digital approximations**, but they work well for many apps.
 
<img src="/assets/1.2_FFT.png" alt="drones" width="50%"> 

<br>

#### **1.3 Equations (deterministic) dont work for human interaction**


**(1) For a human, words and language elicit thought.** 
I cant find a good pic for thought. There is none. 

<img src="/assets/1.3_neurons.png" alt="drones" width="20%"> 

**(2) For computer, words are just visual representations of numbers (ASCII characters).** 
An LLM's thinking is all computation in binary. 
Finding a pic for binary is simple.
 
<img src="/assets/1.3_ascii.png" alt="drones" width="35%"> 

<br>

#### **1.4 "Deterministic" computer algorithms**

So if you cant do it with an equation, then just do it with a binary algorithm?

**(1) Interactions that are far too complex (molecular interaction)**.
There are equations that determine atomic interaction in molecules, but atoms are not points in spaces, and they all interact with each other. The computations are not possible. Simplifying the computational model of interaction to fit the level of computational power leads to a gibberish answer.
 
<img src="/assets/1.4_protein.png" alt="drones" width="30%">  

**(2) Large sets of data sometimes dont follow any logical patterns**. 
This example is used throught this page (Belgium/Holland demo). The map defines city sections in the Netherlands that are considered legally part of Belgium. A lot of processes in nature are like this.  There are rules defined by the data (the map), but there is no discernable logic.

<img src="/assets/1.4_belgium.png" alt="drones" width="40%"> 

**(3) Human language is not possible to recognize with traditional computer algorithms based on logic and equations**.  
Our words are minimalist code that we use to transfer info (just like facial expressions). 
- The possible combinations are as numeroous as with the protein molecular, 
- the rules as illogical as the Belgian town districs in Holland (Netherlands, the Netherlands, Dutch) map.
- And then the spellllling mistakes, the synonyms, etc etc. 

Defining all the possible combinations of words is impossible.

<img src="/assets/1.4_word_combos.png" alt="drones" width="65%"> 

<br>

#### **1.5 Transformer UFA solution**

**(1) The TF implements a UFA (probabliistic approximator, not intelligence).**

When I first read about UFAs, I thought it was some useless theoretical talk. Its actually the key to understanding AI. AI is based on Transformers (TFs) that implement UFAs. If you understand UFAs then you truly understand AI. **But most importantly, you understand AI's limitations.**

In the diagram below, the inputs are X and Y (diagram does not say what these are; for a GPT-3 TF these would be 2 of the 12288 FP (floating point) numbers for a single token inside the TF; these numbers represent complex aspects of the data that is defined in training, not by a human (that is the key; for the Belgium demo we define ourselves what the data represents)). Using a UFA, its possible to define complex regions of the output value (I go into the algorithm and math later on this page). 

*Universal Function Approximators (UFAs). That word "approximation" is the key.  https://medium.com/hackernoon/illustrative-proof-of-universal-approximation-theorem-5845c02822f6* <br>
<img src="/assets/1.5_ufa.png" alt="drones" width="80%"> 
 
**(2) TF UFA encodes patterns via programming ("training")**. 

In the Belgium problem, your inputs are X and Y (latitude, longitude). Your output is Belgium or Netherlands. With a map you could create a detailed data map that is very exact. But that Belgium demo is a extremely simplified version of what you need for language. 

For the TF you use massive amounts of input / desire-output combinations to program the NN (set ~ trillion parameters, the weights and biases). 


**(3) Inference**. Inference just replicates the training, except that you input text and computer the most probable next token (thats all a TF does; not intelligent).

*Diagram from the excellent [video](https://youtu.be/7xTGNNLPyMI?t=2890) "Deep Dive into LLMs like ChatGPT" by Andrej Karpathy.* <br> 
<img src="/assets/1.5_inference.png" alt="drones" width="35%">  

<br>

#### **1.6 Viable / nonviable applications of UFA**

**(1) Viable: Belgian town demo (mistakes are not critical)**. I go throught the math on this demo later in this document. The original [video](https://youtu.be/qx7hirqgfuU?t=6) content (from Welch labs) is excellent. But I try to approach the topic a bit differently, avoiding the complex 3d videos and focusing on the math algorithm (to me thats easier to understand, and it scales easily into more than 2 "dimensions"). 

*Netherlands/belgium example [video](https://youtu.be/qx7hirqgfuU?t=6)* <br>
<img src="/assets/1.6_belgium.png" alt="drones" width="30%"> <img src="/assets/1.6_belgium_tf_map.png" alt="drones" width="40%"> 

**(2) Not viable: Computer-driven cars on public roads**.Its just my opinion. You can fly a drone or an airliner with auto-pilots because airspace is a forgiving medium (you have a lot of room for error in the air). But a car in a city teeming with pedestrians? On a dark rainy night? A decade of unfulfilled self-driving car promises has convinced me that self-driving cars and humanoids in the home will not be safe enough for at least another 10 years (I hope I am wrong). 

*FSD*<br>
 <img src="/assets/1.6_no_fsd.png" alt="drones" width="30%"> 



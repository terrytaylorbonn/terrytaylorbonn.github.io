---
layout: page
title: TL;DR
permalink: /0-tldrxxxx/
---

<br>


This is the TL;DR = "too long; didn't read" page. The page that tells you what its all about (the gist) without you having to read much.

**TOC** (sorry, its not a one-line expanation; this is, after all, not a simple topic)
- 1 ZiptieAI can give you a solid foundation in AI ... ASAP
- 2 Or you can buy a black box (that promises to help you understand whats inside the black box)
- 3 The golden middle
- 4 How ZiptieAI.com delivers

<br>

### **1 ZiptieAI can give you a solid foundation in AI ... ASAP**

On the ZAI webpage **[build your own Tiny Transformer](https://ziptieai.com/2.3.6.1b-d5-tiny-tf-algorithm-details/)** I show you how to build your own LLM TF on your local PC. Then train it and run inference. With concept and line-by-line code description. If you are new to AI, it might take your a few weeks or even months to really grasp it all. But its time well spent. 

<br>

### **2 Or you can buy a black box (that promises to help you understand whats inside the black box)**


On 26.0604 the Youtube AI algorithm that magically finds videos that fit my viewing **patterns** (an absolutely magical AI tool that has changed my life) listed a video on my phone that makes a lot of good points about what AI is. **Most viewers would love this video, but for me its an example of typical AI misconceptions and hype.** I recognized the good and the bad immediately, because **I have done a lot of AI programming**. Especially low-level AI model programming. 

<br>

#### **2.1 The video starts out with an excellent summary of AI hype and failures**

The video author states about AI investments: "You know what that tells you? The people writing the checks (the venture capitalists) dont believe the hype either. LLMs have a point of diminishing returns... are they going to be one of the biggest hype machines we've ever seen?". Then he makes a truly **brilliant statement: "The truth lies somewhere in the middle"** (between AI as a total scam and AI as a replacement for humanity). I write more about this "middle" later in section 3 of this page. 

<br>

#### **2.2 The video then talks about the real engineering AROUND AI**

He then says "we're going to talk about **the real engineering AROUND AI**, what to expect for it, and what an AI realist is telling you about it." Note that word **"around"**. This video is about selling you a black box. The core AI runs inside that black box :) . The code on this Github is for agents that work **around** the model. But **you will never really understand AI by playing around with an AI LLM black box.. you need to build your own LLM (transformer part)**. 

PS: What I like most about the marketing on this video is that "you can run your own AI with unlimited tokens" by buying the black box. :) You can do the same thing by just running a model on your local PC. 


*The black box*<br>
<img src="/assets/tldr-2.png" alt="drones" width="55%"> 


<br>

#### **2.3 A [key moment](https://youtu.be/SIPmUwwRKRo?t=575) in the video**

<img src="/assets/tldr-1.png" alt="drones" width="45%"> 

I have many issues with the statements in the pic above:
- ***"even those not training models"***. I recently added a detailed description of **how to [build your own Tiny Transformer](https://ziptieai.com/2.3.6.1b-d5-tiny-tf-algorithm-details/)**. This also includes training. Only after you've built the simplest TF and done the simplest training do you really have an intrinsic understanding of what TF training is.
- ***"they (programmers) think in code"***. Its doesnt matter if you think in code... **what matters is you understand that AI does NOT think**. LLMs (TFs) are just deterministic binary code. **If you enter the same input, you get EXACTLY the same output** (if not, that means the LLM used the trick of intentionally adding random input).
- ***"all abstractions are leaky"***. (???). AI is not an abstraction. It is pattern recognition. AI only knows numbers. It has no senses, no thoughts, no feelings, etc etc etc. Its just binary computation. "Artificial intelligence" is not an abstraction -- its a marketing gimmick.
- ***"when AI produces suboptimal code"***. (???). Producing code is AI's primary strength. Deterministic AI SW is naturally good at working with code. Code is vastly simpler for AI to work with than anything that requires an iota of real intelligence to do realiably. The problem is when you want an non-intelligent LLM to "understand" exactly your high level conceptual descriptions (usually incomplete) of what the code should do.
- ***"the person who understands the substrate catches the failures everyone else misses"***. (???). The failures of AI are obvious. You dont' catch them, they catch you. When your "FSD" tries to drive you into a lake, you notice. When your AI tool "hallucinates" (a clever marketing term) its annoyingly obvious. In the future, if you are foolish enough to allow a humanoid robot into your home, its "hallucinations" will be painfully obvious. The real lesson is **"the person who understand AI fundamentals wont go down the rabbit hole everyone else does"**. They wont design systems in the first place that never should have been based on AI.

<br> 

#### **2.4 He sums up [the core of LLM AI](https://youtu.be/SIPmUwwRKRo?t=276) with one sentence (but not with demos)**

"(some Turning award winner) has argued for decades that **statistical models trained on text learn how we describe the world, not how the world actually works"**. Exactly. 

But just a minute later he talks about **you can buy the black box and run agents immediately**. The problem with that is: **Agents are not AI. They use AI.** How are you supposed to **learn how statistical models fake real intelligence** if you dont actually build a model (and study the code line by line)? 


<br>


#### **2.5 A [total misconception](https://youtu.be/SIPmUwwRKRo?t=411) in the video**

He then make a comparison between compilers and AI (see pic below). 

He says compilers will always give you the exact same thing (he means the bytecode, the compiled code that will actually run). But he does not mention that compilers (even without AI) can guarantee that the code is correct, because code is vastly simpler than human language and thought. **But a compiler can not guarantee that the code will do what it was intended to do.** 

Then he says that on the other hand "you can give AI LLMs the exact same input multiple times and get a different output every time." **That is not correct. An LLM (and the TF inside) is 100% deterministic.** The same input will **always** generate the same output (if all internal state variables are all the same **and if randomness is not intentionally injected into the system** (a trick often used to fool the user into thinking the LLM is not deterministic)). 

*This diagram shows the LLM as clouds because its determinism is difficult to grasp and conceptualize*<br>
<img src="/assets/tldr-3.png" alt="drones" width="45%"> 

<br> 

### **3 The golden middle**

My goal here is not to criticize the video. Its a great video because it fulfills its core purpose: To sell a black box to those wanting to understand whats in the black box. Thats really good marketing. 

My goal is the golden middle. Without GPT I could not have built ZAI in record time. I relied almost exclusively on GPT (and other AI tools), because the quality of instruction by an (unintelligent) LLM was vastly superior to that of traditional tech writing output. 

**So AI is without a doubt incredibly valuable. But for what? You can only answer that if you have done low level demos. Hands on.**

But how? Andrey Karpathy once said it will take you 10,0000 hours (5 years at regular 8 hrs day, 5 days a week) to really learn AI (and I agree if you try to learn from his documentation and video demos). 

You have to choose a "golden middle". You need to know 
- How deeply to analyze/write AI code (TF code) and study libraries
- What AI projects make sense (exploit the advantages and avoid the shortcomings of AI)

<br>

### **4 How ZiptieAI.com delivers**

ZAI helps direct you on the right path of self learning. That's all you need from human sources. AI (having been programmed ("trained") with vast amounts of previous text written by intelligent humans) can assist you with the details.

The path consists primarily of writing code. Code is the source of truth. Code does not lie. 

*ZAI [demos](/0b-demos/)*<br>
<img src="/assets/tldr-4.png" alt="drones" width="55%"> 

<br>

26.0604 (v1 26.0604)

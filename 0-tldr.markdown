---
layout: page
title: TL;DR
permalink: /0-tldr/
---

<br>

TL;DR = "too long; didn't read". **This page describes the gist of this site** without having to read the entire site.

**TOC**
- 1 Magical A/C units
- 2 Magical AI units 
  - 2.1 Amazing capabilities
  - 2.2 Very low cost
- 3 How I know AI has no real intelligence (its a no brainer)
- 4 Learning how to separate the AI wheat from the chaff (using ZiptieAI)
- 5 "Agentic" AI and AI agents (using ZiptieAI)

[TL;DR (v2) (WIP)](/0-tldr-v2/)

<br>

### **1 Magical A/C units**

A Youtube ad has been popping up on my screen lately that shows a new tiny A/C unit that some genius developed because all existing A/C units are ripping us all off. This magical unit has no air ducts (to disperse heat outside). You just plug it in and it cools your room within a minute with vastly less energy usage than traditional A/C. The magical A/C unit looks just like the heater in the pic below. Anyone with basic common sense understands that the heat has to be transported out of the room somehow. Yet apparently many people are buying these things. 

**I dont even have to test one of those A/C units to know it wont cool a room**. I know that the people selling it are lying. But it may heat a room, because all that energy it uses is dispersed into the room. So **I know it has potential good uses (just not what's advertised)**.  

<img src="/assets/tldr-5.png" alt="drones" width="14%"> 

The ad popped up again and I was able to snap a screenshot! Buy yours today from buyglacierbreeze.com!

<img src="/assets/tldr-5gb.png" alt="drones" width="38%"> 

<br>

### **2 Magical AI units**

If you thought glacierbreeze was awesome (with its abilities to cool big rooms in no time using almost no energy and without requiring a hose to push hot air outside), then you ain't seen nothing yet. AI supposedly has 
- **2.1 Amazing capabilities**. First and foremost **a clocked binary state machine that has real intelligence that will soon reach super-human AGI levels**.
- **2.2 Very low costs**. Computing **a single token on GPT-3 required up to a million billion (10^15) FP calculations**. I pay $20/month for GPT-5 to generate massive numbers of tokens. 
    
<br>

#### **2.1 Amazing capabilities**

One of my favorite AI Youtube channels is Best partners TV. They recently had a video about one of my favorite A/I researchers, Richard Sutton. The video is called "[Enactive Cognition](https://www.youtube.com/watch?v=6bfCuxI_84U)".  

The following is the summary of the video: *Recently, Richard S. Sutton, the **father of reinforcement learning**, ... co-authored a groundbreaking paper titled "Toward **Enactive Artificial Intelligence**." This paper can be seen as a ... **critique of the current mainstream AI paradigm**. As a founder of reinforcement learning, Sutton starts from the most basic questions of cognitive science, **revealing a harsh truth: current AI lacks true understanding because it has been on the wrong path from the outset** ... The **next step for AI must be a complete shift towards enactive cognition**, allowing agents to generate their own experiences and understanding of the world through active interaction with the environment, embodied action, and **self-evaluation**.*

The same old AI **hype**. I don't even have to watch the video to know the basic premise is nonsense. I dont have to be an AI expert to understand that SW running on clocked binary circuits can not even begin to match the cognitive abilities of the human mind. **AI crunches numbers. It sees nothing, hears nothing, has no thoughts, absolutely no cognitive abilities**.

*The best minds in the world can't create a number cruncher with driving capabilities even remotely on the level of the human mind*<br>
<img src="/assets/tldr-6.png" alt="drones" width="22%"> 

<br>

#### **2.2 Very low cost**

The Youtube A/C commercials often talk about how **some little gadget can cool an entire room in a few minutes while using vastly less electricity** than what you are using now. 

Once you get familiar with AI algorithms, you start to realize **the massive amount of brute-force computation required to generate AI output**. I personally get the feeling that I am not paying near what my actual usage costs. I've read such opinions quite often recently. I think if you really understand just how much computing you can get with a $20 a month GPT description, then you realize that **someone is for some reason giving you a huge discount... but why, and for how long?**. 

I typed out some of the **[conversation with Ed Zitron](https://youtu.be/W2vgx5mHaYA?t=42)** of EZ Primary Research. 

*"people are confusing a semiconductor rally with an underlying business which really doesn't exist... **their (Anthropic) growth is coming because people cannot measure how much an AI task actually costs**. And a couple of months ago Anthropic started charge their enterprise customers the actual token rates. .... **they are having trouble justifying the AI spend based on the actual return that one can actually measure**. So you have a thing that you can measure the costs and you cant measure the return on investment. What do you call that? you call that a thing without an ROI." He later goes on to talk about OpenAI and Anthropic as dangerous companies that face no real scrutiny. ... **People are creating workflows around it based on services they likely can not afford long term**.*

On 26.0608 I saw a video about **Trump proposing that the US government invests in AI companies and allows all Americans to share all those massive profits that will come in the near future**. A while back the AI titans were wanting government guarantees for loans for AI infrastructure investment. It sounds like the strategy for getting government subsidies has taken a new twist.

In any case, **nuclear power recently became safe and effective**. I wonder why... maybe future cheaper sources of power and ever more efficient GPUs will make the cost of AI something that people are really willing to pay full price for. 

<img src="/assets/00-ai-nukes.png" alt="drones" width="28%"> 

<br>

### **3 How I know AI has no real intelligence (its a no brainer)**

**Docx #607** (on the **[Gdrive](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**) chapter **"D6 — Tiny Pattern Detector Neural Network"** shows how to build a simple NN (and run on local PC with no GPU). The NN detects the sequence "1,1,1" in a list of 10 numbers. 

```
[0, 0, 0, 1, 1, 1, 0, 0, 0, 0] pattern_score= 0.87180638 detected= 1
[0, 1, 0, 0, 1, 0, 0, 1, 0, 0] pattern_score= 0.00000197 detected= 0
[1, 1, 1, 0, 0, 0, 0, 0, 0, 0] pattern_score= 0.00000000 detected= 0
[0, 0, 0, 0, 0, 0, 1, 1, 1, 0] pattern_score= 0.98744279 detected= 1
```

Note the words "pattern" and "score". Its **pattern matching**, and the score is the **probability that a pattern match was detected**. This is the core of how NN's work. All of them. Even Tesla FSD (that has been making the hollow promise of safe FSD (full self driving) for over a decade). 

The following shows the internal parameters that compute the NN output. These parameters were programmed into the NN during "training" by running many input/desired-output pairs through the NN and modifying the parameters until the results were as good as they can get.

```
Hidden Neurons
Neuron 0
tensor([0.0947, 0.1645, 0.0096, 0.6908, 0.3498, 1.1162, 0.5762, 1.0838, 0.4246, 0.8733])
Neuron 1
tensor([-0.1893, -0.4918, -0.9708, -0.5948, -1.1588, -0.4314, -1.1738, -1.5425, 0.5428, -0.6313])
Neuron 2 ........................
```

For this simple demo you could simply write a Py script that searches for 1,1,1. But you need NN's for complex patterns that are impossible to match using traditional methods.

All of AI (FSD, LLMs, etc) is based on the same kind of probability computations. This really helps you to appreciate what an engineering marvel AI tools are and **how limited their mimicry of "intelligent" capabilities is**. Likewise, CPU-based binary computing (for non-AI computers like PCs) is also an engineering marvel, being based on primitive binary clocked switching transistors.


<br>

### **4 Learning how to separate the AI wheat from the chaff (using ZiptieAI)**

*"Separate the wheat from the chaff" is an idiom that means to distinguish valuable or useful things (or people) from worthless ones.*

There is a lot of wheat in AI. And **what Sutton proposes may make real significant improvements** in statistical pattern matching tools ("AI"). And **there is a massive demand for AI's capabilities**. You just need to be **able to separate the AI wheat from the chaff**. 

#### **How?**

**1 Coding basic AI demos (NNs, CNNs, LLMs, etc) is the only way to really grasp what AI (and AI hype) is**. You can make a lot of quick progress in understanding the core of AI by doing some surprisingly simple demos. Its not that difficult nowadays, because AI tools (Cursor, GPT, Codex, etc) do the coding and debugging for you.  

**2 You'll quickly realize where AI excels and fails**. AI NNs are just statistical models trained on whatever input you give them. They only crunch numbers (they don't have any comprehension of the real world).

**3 You also have an idea what kind of software engineering jobs will experience big growth in the future**. You can sift through predictions about the future like the following. 

<img src="/assets/tldr-1.png" alt="drones" width="45%"> 

My comments:
- ***"even those not training models"***. True. But "training" is the key to creating models. Its still a good idea to have basic hands-on training.
- ***"they (programmers) think in code"***. What matters is they understand (on an intrinsic level) that AI **only** "thinks" in code (AI is simply a number cruncher). 
- ***"all abstractions are leaky"*** (???). The many AI abstractions (such as "attention", "reasoning", "planning") are all hype and marketing terms. 
- ***"when AI produces suboptimal code"*** (???). Producing code is AI's primary strength. The problem is trying to get AI to deal with anything that human's excel at (conceptual, original material). 
- ***"the person who understands the substrate catches the failures everyone else misses"***. The failures of AI catch you. When your AI "FSD" tries to drive you into a lake, you can't help but notice. Understanding the fundamentals allows you to focus on AI projects that wont die deep in a rabbit hole. 

**4 ZiptieAI can give you a solid foundation in AI**. ZAI describes a complete set of **[demos](/0b-demos/)** (WIP) you can do on your local PC (many without a GPU). Code is the source of truth. Code is not hype. I career-transitioned to AI just a few years ago. The fast transition was only possible thanks to the incredible capabilities of AI tools (GPT, Cursor, etc). 

<!-- This site (and the **[wiki](https://github.com/terrytaylorbonn/auxdrone/wiki)**) is primarily my way of documenting my AI projects (and as an online **[resume](/about/)**). -->


*ZAI model [demos](/0b-demos/) (WIP)*<br>
<img src="/assets/tldr-4.png" alt="drones" width="55%"> 


<br>

### **5 "Agentic" AI and AI agents (using ZiptieAI)**

For the **[simple NN demos](/2.1-predictive-nns/)**, the NN and the code that controls the NN are defined in the same Python script. The **[Tiny CNN demo](/2.2-cnns/)** adds convolution code (convolution basically scans for patterns in neighboring pixels). The **[Tiny Transformer](/2.3.6-llm-demos/)** adds "attention heads" (AHs, context sharing between tokens) to the NN Python script. **Major "frontier" (lastest and greatest) LLMs** also have not only a very large and complex  (1) TF (with AHs) but also a very sophisicated (2) **internal agent (iAgent, non-GPU code)**. The iAgent **totally controls the TF with text prompts** (and the TF answers only with text responses). 

<img src="/assets/tldr-8.png" alt="drones" width="65%"> 

Most of this page has been about NNs because **an AI agent totally depends on an advanced agentic LLM's ability to provide higher level functionality that mimics higher level human brain functionality** (such as thinking, planning, reasoning, etc). Example: You send a prompt with a complex plan, and the TF breaks it down into **"atomic" planning steps**. The TF can do this because it has been trained on such planning text. This capability is revolutionary. **However**, the **probability that the external agent (Py script) can process the atomic plan without error is never 100%**. But it is much higher than the chance the script can process the original plan (often messy unsanitized human language). 

**These limitations of AI are apparent in tiny demos, but major AI systems also struggle with the same limitations.** Agentic AI will always be challenging because the LLM is a probablistic computational device with no intelligence.   

*ZAI agentic [demos](/0b-demos/) (WIP)*<br>
<img src="/assets/tldr-7.png" alt="drones" width="55%"> 

<!-- **[build your own Tiny Transformer](https://ziptieai.com/2.3.6.1b-d5-tiny-tf-algorithm-details/)** shows you how to build your own LLM TF on your local PC. Then train it and run inference. it might take your a few weeks or even months to really grasp it all. But its time well spent. -->

<br>

26.0608 (v1 26.0604)

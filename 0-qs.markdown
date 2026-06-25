---
layout: page
title: QS
permalink: /0-qs/
---

<br> 

#### ***This page is a work in progress (WIP)***. *The goal is a start-to-finish set of representative demos that teaches the core concepts of each section.*

```
GPT:
Overall, I think this is one of the strongest organizational ideas you've come up with. It answers the question that every newcomer has:
"What should I actually build first?"
Your site has become large enough that people need a guided path. A QS page solves that.
(1) The basic idea
I would score it 9.5/10.
The only thing I'd change is the philosophy.
Instead of
•	"one demo from each section"
I'd make it
•	"one representative demo that teaches the core idea of that section."
That is a subtle but important distinction.
For example, D4 isn't chosen because it's "the CNN demo."
It's chosen because it teaches almost everything someone needs to know about CNNs.
```

<br> 

This QS (quick start) follows the organization of this site as shown in the site "master diagram" (below).
- **2 NN demos**. Tiny demos that can also run on a CPU. These NNs only know FP numbers as input and output. So if you have any type of other data, you must encode and then decode. 
  - **2.1 Core NN** (can be used alone or as CNN dense layers / TF FFN).  
  - **2.2 CNNs (convolution)** has an extra "NN" that performs convolution. 
  - **2.3.6 Transformers**. A bare bones but fully functional TF.
  - **2.5 Robotic AI** (Robotic AI is not a core focus right now).
- **2b Model demos**. A model contains the **NN/CNN/TF** and an **"internal" agent (iAgent)** that controls and provides access to the NN/CNN/TF. The iAgent implements an **API** that provides external access to the model.
  - **2b.2 Tiny demos**. 
  - **2b.2b Building models**.
  - **2b.3 Modifying models**.
  - **2b.4 Running models locally**. 
- **3 External agent (py script) demos**. Using a model as a helpful assistant.
  - **3.1 Code-first agents**.
  - **3.2 Agent framework**. 
- **3b Projects**. Projects are where all the previous pieces come together. They aren't just "more demos" — they're the integration point. The real goal of AI projects is to integrate AI into an existing SW app. However, there are no such "integration" apps yet... but the following are good initial demos:
  - **3b.3 NMAP Security Assistant**. Uses the local PC as the target system. This is not only a practical tool, but also can help you learn very important security topics for your home PC/network setup.
  - **3b.2 JobRadar**. This intros hope to connect to email, etc to get a daily summary.  


<br> 

*Master diagram (ZAI original)*<br>
<img src="/assets/M-15.png" alt="drones" width="78%">

*Note: Old demos are available on [Wiki](https://github.com/terrytaylorbonn/auxdrone/wiki), [Github](https://github.com/terrytaylorbonn?tab=repositories), [Gdrive](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO) (docx lab notes).*

<!-- Note that **there are many variations of this setup**, and I will try to provide the version of this diagram for each demo (v1 of this diagram created 26.0615). -->
<!-- 
**The ONLY way to understand AI is by doing examples.** This page currently is an overview of all the demos on this site. But it will slowly morph into a Quick Start with specific demos to focus on. 
**TOC**
- **1 Master diagram**
- **2 NN demos**
- **2b Model demos**
- **3 Agent demos**
- **3b Projects**  -->
<!-- 26.0625 BACKUP
- **2 NN, CNN, TF**
  - **Core NN (CNN dense, TF FFN)** is the core NN in all demos (except agent only demos with no AI).
  - **CNN convolute, TF QKV (context)** is an extra NN in CNNs and LLM transformers (TFs).
  - Note that these run (normally) on a GPU. But they run on a CPU.
  - These NNs only know FP numbers as input and output. So if you have any type of other data, you must encode and then decode.
- **2b Model**
  - Contains the **NNs** and an **"internal" agent (iAgent)** that has sole access to the NN. iAgent and NNs **only** communicate with tokens.
  - iAgent often implements an **API** that allows external access.
- **3 External agent (py script)** uses the model as a helful assistant.
- **3b Project** usually provides integrates AI into existing digital infrastructure.
-->

<br>

### **[2 NN demos](/2_models/)**

<br>


#### **[2.1 Core NNs (CNN dense layers / TF FFN)](/2.1-predictive-nns/)**. Basic neural network demos.<br>


<!-- <img src="/assets/classification.png" alt="drones" width="15%"><br> <br>  -->


Tiny NN demo ([demo D2ccc](/2.1.2-classifier-nn/)) (inference)

**This one simple NN demo will give you an understanding of the core of all AI inference** (including CNNs, LLMs TFs, etc). The following diagram shows the core components of the demo:
- **Encoder**. All NNs only "know" numbers (including ChatGPT, Claude, etc). So if you have a dataset that is not (FP) numbers, it must be encoded (and later decoded).
- **NN**. The source of "intelligence". A UFA (universal function approximator). 
  - This NN inputs 2 numbers. And based on that number outputs 2 probabilities. That's it.
- **Decoder**. Convert from a probability for inside/outside the circle to a binary state (1 or 0; inside/outside circle).  

*GPT: It teaches tensors, forward(), Linear, ReLU, logits, CrossEntropy, training, inference without overwhelming people.*


<img src="/assets/M-05.png" alt="drones" width="50%"> <img src="/assets/M-02.png" alt="drones" width="16%">

<br>

#### **[2.2 CNNs (convolution)](/2.2-cnns/).**  <br> 

See Tiny CNN (**[demo D4 MNIST](/2.2.1-d4-cnn-image-classifier/)**).

A hands on demo. Input a 28x28 pixel screenshot of a digit, and the NN outputs "0", "1", ... "9". For details see 
- **[2.2.1 D4 CNN image classifier](https://ziptieai.com/2.2.1-d4-cnn-image-classifier/)**
- **[2.2.1b D4 CNN algorithm details](https://ziptieai.com/2.2.1b-d4-cnn-algorithm-details/)**

There are 3 main parts.
- **1 Data input**. In this case the data input is .............
- **2 Feature extraction (nn.Conv2d + nn.MaxPool2d)**. This is where convolution and pooling are used to turn the original pixel values into "hidden state" values that progressive define higher level features (I typical call these values "pix's"). ...
- **3 Final NN (nn.Linear) computing CNN "logits"**. This involves
  - 3.1 Linear NN (like for D2ccc) computes the probabilities of each of 10 possible outputs (digits 0 to 9).
  - 3.2 The most probable output is converted into a label (such as "7"). -->

*CNN demo D4 overview (ZAI/GPT original diagram)* <br>
<img src="/assets/M-33.png" alt="drones" width="40%">

<br>


#### **[2.3.6 Transformers](/2.3.6-llm-demos/).**<br>

See (**[demo D5 Tiny TF](/2.2.1-d4-cnn-image-classifier/)**).

*TF demo D5 overview (ZAI original diagram)*<br>
<img src="/assets/M-09.png" alt="drones" width="55%"><br> 

<!-- <img src="/assets/d5_0.png" alt="drones" width="32%"><br> <br> -->

<br>

#### **2.5 Robotic AI ([wiki](https://github.com/terrytaylorbonn/auxdrone/wiki/Robotic-AI-demos))**<br>

```
GPT: 
Tiny obstacle detector (or whichever demo first connects perception to action). 
The important concept isn't robotics hardware. It's sensor → NN → decision → actuator.
```

```
ME: i think D30 (28bbb) is the robotic AI demo you mentioned. 
#502_3_robotics_AI_no_jepa_v31_26.0131.docx
28bbb D30 add GIF (BINGO) #174 is there any way to create a gif with just the resulting path and obstacle? 
Yep — very easy, and this is a good next step because visualizing the trajectory is what makes D30 click for robotics readers. 
There are three simple ways, depending on how fancy you want it:

GPT: 
Yes — D30 / 28bbb “avoid the rock” is probably the right 2.5 Robotic AI QS demo.
It has the key robotics loop:
start position
→ perceive obstacle
→ plan path
→ avoid obstacle
→ reach goal
→ visualize trajectory
That is much better than a drone-specific demo for QS, because it is simple, visual, and general.
For QS I’d write:
- **2.5 Robotic AI**. Connects AI to action: perceive the world, choose a path, avoid an obstacle, and move toward a goal. **Demo is D30 “avoid the rock” / 28bbb GIF**.
Why it works:
  “rock” makes the problem intuitive.
  the GIF makes the result instantly understandable.
  it shows robotics without requiring robot hardware.
  it connects perception + planning + action, which is the core idea.
So yes: D30 28bbb is the pick.
```

<img src="/assets/robotic_ai.png" alt="smol" width="55%" style="border: 1px solid black;"><br> 

<br>

### **[2b Model demos](/2b_models/)**

<!-- - ([2b.1b 2025 demos](/2b.1b-2025-llm-demos/))<br><img src="/assets/smol.png" alt="smol" width="35%"><br> <br> -->

<br>

#### **[2b.2 Tiny demos](/2b.3.6-llm-demos/)**<br> 

```
GPT: M01 (save model) because it introduces NN + .pt.
```

<br>

#### **[2b.2b Building models](/2b.2b-build-models/)**<br> 

```
GPT: M06 HuggingFace publish because suddenly the model becomes portable.
```

<br>

#### **[2b.3 Modifying models](/2b.3-modify-models/)**<br> 

```
GPT: M06 HuggingFace publish because suddenly the model becomes portable.
```

<br>

#### **[2b.4 Running models locally](/2b.4-run-models-locally/)**<br>

```
GPT: M07 FastAPI. This is where the model becomes a service. I think that's exactly what people need to understand
```

<br>

### **[3 Agent demos](/3_agents/)**

The center of the Agentic AI universe is the AI agent.  The agent and LLM together can doing amazing things. But they also have severe limitations. "Tuning" then to work together is the core focus. 

 

```
GPT:

3.1 Code-first agents >> PAL_CORE planning demo
I'd probably use
PAL_CORE planning demo
because it shows
•	LLM ↓ JSON ↓ Python ↓ Tools ↓ Result
That is the essence of agent programming.

3.2 Framework > n8n / PydanticAI
Probably your smallest
n8n
or
PydanticAI
demo.
The framework itself isn't important.
The concept is.
```

```
Delete this:
- **[3.1 Agentic (no AI)](/3.1-agentic/)** <br> 
<img src="/assets/4_5_3x.png" alt="drones" width="20%"> <br><br>
- **[3.2.4 Agentic + AI / Basic demos](/3.2.4-ai-agent-basic-demos/)**. <br>
<img src="/assets/calc1b.png" alt="drones" width="35%"> <br><br>
- **[3.2.5 Agentic + AI / PAL demos](/3.2.5-ai-agent-pal-demos/)**.   <br>
<img src="/assets/4_6_2x.png" alt="drones" width="20%">  <br>
<img src="/assets/4_5_3x_bbb.png" alt="drones" width="20%"><br><br> 
```

<br>

### **[3b Projects](/3.3-ai-projects/)** (GPT: this note is extremely important)

This section focuses on "spinning up" real-world projects quickly with minimal code analysis or manual coding. 

- The real goal of AI projects is to integrate AI into an existing SW app. 
- But the demos listed are all basically Palantir style demos, where you create an external agent that is the main app (I don't have (yet) my own app that I'd like to integrate AI into). 
- The focus is mostly on programming an agent to use external tools and APIs, not on an existing SW calling the agent for assistance. 
- In any case, you use these demo techniques to give your AI app access to a systems DB (like I do with the JobRadar, which has access to a test Gmail account emails).  *GPT: Existing system > Gmail > External Agent > LLM > Summary / Alert.*
- In any case a good first demo might be 
  - **3b.3 NMAP Security Assistant**. Uses the local PC as the target system. This is not only a practical tool, but also can help you learn very important security topics for your home PC/network setup.
  - **3b.2 JobRadar**. This intros hope to connect to email, etc to get a daily summary.  

```
GPT:
The only thing I'd emphasize a little more is that 3b Projects are where all the previous pieces come together. 
They aren't just "more demos"—they're the integration point:
•	2.x teaches how models work. 
•	2b teaches how models are packaged and served. 
•	3 teaches how agents use models. 
•	3b shows how agents solve real problems by integrating with existing software and external systems. 
That makes 3b feel like the natural culmination of everything that came before, rather than another independent section.

```


```
GPT: 
Nmap has several advantages:
•	real system 
•	real data 
•	security 
•	MongoDB 
•	OpenAI explanation 
•	Mattermost alerts 
It demonstrates nearly every important concept in one project.
```


```
GPT: 

I actually think this note is extremely important.
Because it explains something almost nobody explains.
Namely:
AI projects are almost never "build ChatGPT."
Instead they're
Existing software

AI assistant
Exactly.
I especially liked this sentence:
The real goal of AI projects is to integrate AI into an existing SW app.
I would make that the very first sentence.

The second bullet, however, I would simplify.
Instead of
Palantir style demos, where you create an external agent...
I'd simply say
My demos use the external agent as the main application because I don't yet have a large production application to integrate AI into.
That's easier to understand.
```

<img src="/assets/6_main_diagram.png" alt="drones" width="40%"> 


<br>

26.0625 (v1 26.0527)


<!-- **I wasted so much time going down so many rabbit holes when studying AI**. AI is an awesome technology. Without AI tools (GPT) I never could have accomplished 5% of what I have done on the ZiptieAI project. But **AI chatbots only produce the output they are programmed to produce, and much of that about AI itself is misleading hype (or outright lies)**. The very term "artificial intelligence" is a perfect example. AI is not intelligent, and the very concept of "man-made" intelligence shows a basic lack of understanding of what intelligence is. 

**Code does not lie**. Do this QS and see for yourself what AI really is. Then go to the **[concepts section](/0b-demos/)** to get a firm conceptual grasp of the big picture. You need to do the QS first because otherwise you will struggle greatly to understand much of the **AI lingo (which can be quite misleading)**.
-->

<!-- **Studying code for basic AI demos** (NNs, CNNs, LLMs, etc) is the **only way to really understand AI** (and AI hype). And its **not that difficult** nowadays, because AI tools (GPT, Sonnet, etc) do all the difficult coding and debugging for you. But **you have to supply the right prompts**. 

- **1 Drone demos**
 -->

 
<!-- 
### **1 [Drone demos](/1-drones/)**

This site does not really focus on drones anymore. But I include it because it was the first project I did where I used AI (object recogntion). Note that drones dont need AI to fly (like cars need AI to drive on roads). 

*My AI drone build*<br>
<img src="/assets/airborne2.png" alt="drones" width="40%"> <img src="/assets/6cjnano.png" alt="6c" width="23%"> 

<br>
-->

<!-- *AlexNet CNN (left) and LLM transformer (right)*<br>
<img src="/assets/cnn2.png" alt="desc" width="35%">  <img src="/assets/tf_S1-S6.png" alt="desc" width="40%"> -->


<!-- <img src="/assets/0_projects2.png" alt="drones" width="35%"> -->

<!-- <img src="/assets/readfile3.png" alt="drones" width="60%" style="border: 1px solid black;"> -->

<!-- - **[3.3 Agentic AI projects](/3.3-ai-projects/)**. Complete business segment projects (main long-term focus).<br> 
<img src="/assets/6_main_diagram.png" alt="drones" width="25%"> <br><br>
-->


<!-- <img src="/assets/lucius.png" alt="drones" width="55%"> -->

<!-- This page will be a list of demos. Basically a start to finish AI/agents course.

<img src="/assets/classification.png" alt="drones" width="20%"> 

I often see Facebook ads about learning AI. They promise you will **understand AI in 30 days spending only 15 minutes a day studying** (some courses are even better; they only require 10 minutes a day). I ain't smart enough to create such a course. Or a course that demos the "intelligence" of AI. Unfortunately I also **ain't smart enough to make such demos that require no programming skill**. The great AI gurus and AI titans promised us that programming skills would go away (they are even smarter than those folks making the Facebook ads). 

My demos are **mechanistic**, because that's what AI tools are: **Binary, deterministic, mechanistic.** 

-->

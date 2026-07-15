---
layout: page
title: QS
permalink: /0-qs/
---

<br> 

This page (WIP) describes a set of start-to-finish demos that teach the core concepts of AI.

**TOC**
- **2 NN demos**. Tiny demos that can also run on a CPU. These NNs only know FP numbers as input and output. So if you have any type of other data, you must encode and then decode. 
- **2b Model demos**. A model contains the **NN/CNN/TF** and an **"internal" agent (iAgent)** that controls and provides access to the NN/CNN/TF. The iAgent implements an **API** that provides external access to the model.
- **3 External agent (py script) demos**. Using a model as a helpful assistant.
- **3b Project demos**. Projects are where all the previous pieces come together. They aren't just "more demos" — they're the integration point. The real goal of AI projects is to integrate AI into an existing SW app. However, there are no such "integration" apps yet... but the following are good initial demos:

*Master diagram (ZAI original)*<br>
<img src="/assets/M-15.png" alt="drones" width="78%">

*Note: Old demos are available on [Wiki](https://github.com/terrytaylorbonn/auxdrone/wiki), [Github](https://github.com/terrytaylorbonn?tab=repositories), [Gdrive](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO) (docx lab notes).*

<br> 

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

### **[2 NN demos](/2_models/)**

Tiny demos that can also run on a CPU.  
  - **2.1.2 Tiny NN** (very basic NN).  
  - **2.2.1 Tiny CNN** (very basic CNN for recognizing digits 0-9).
  - **2.3.6.1 Tiny transformer** (very basic TF that outputs "hello world..." for input "h").
  - **2.5 Tiny Robotic NN** (very basic demo of using NN to avoid obstacles).

<br>

#### **2.1.2 Tiny NN / [demo D2ccc](/2.1.2-classifier-nn/)**

<!-- <img src="/assets/classification.png" alt="drones" width="15%"><br> <br>  
Tiny NN demo ([demo D2ccc](/2.1.2-classifier-nn/)) (inference) -->

**This one simple NN demo will give you an understanding of the core of all AI inference** (including CNNs, LLMs TFs, etc). The following diagram shows the core components of the demo:
- **Encoder**. All NNs only "know" numbers (including ChatGPT, Claude, etc). So if you have a dataset that is not (FP) numbers, it must be encoded (and later decoded).
- **NN**. The source of "intelligence". A UFA (universal function approximator). 
  - This NN inputs 2 numbers. And based on that number outputs 2 probabilities. That's it.
- **Decoder**. Convert from a probability for inside/outside the circle to a binary state (1 or 0; inside/outside circle).  

```
GPT: It teaches tensors, forward(), Linear, ReLU, logits, CrossEntropy, training, inference without overwhelming people.*
```

<img src="/assets/M-05.png" alt="drones" width="50%"> <img src="/assets/M-02.png" alt="drones" width="16%">

<br>

#### **2.2 Tiny CNN [demo D4 MNIST](/2.2.1-d4-cnn-image-classifier/)** 

A hands on demo. Input a 28x28 pixel screenshot of a digit, and the NN outputs "0", "1", ... "9". See also **[2.2.1b D4 CNN algorithm details](https://ziptieai.com/2.2.1b-d4-cnn-algorithm-details/)**.

There are 3 main parts.
- **1 Data input**. In this case the data input is .............
- **2 Feature extraction (nn.Conv2d + nn.MaxPool2d)**. This is where convolution and pooling are used to turn the original pixel values into "hidden state" values that progressive define higher level features (I typical call these values "pix's"). ...
- **3 Final NN (nn.Linear) computing CNN "logits"**. This involves
  - 3.1 Linear NN (like for D2ccc) computes the probabilities of each of 10 possible outputs (digits 0 to 9).
  - 3.2 The most probable output is converted into a label (such as "7"). -->

*CNN demo D4 overview (ZAI/GPT original diagram)* <br>
<img src="/assets/M-33.png" alt="drones" width="40%">

<br>

#### **2.3.6.1 Tiny TF [demo D5](/2.3.6.1-d5-tiny-tf/)**

*TF demo D5 overview (ZAI original diagram)*<br>
<img src="/assets/M-09.png" alt="drones" width="55%"><br> 

<!-- <img src="/assets/d5_0.png" alt="drones" width="32%"><br> <br> -->

<br>

#### **2.5 Tiny Robotic NN ([wiki](https://github.com/terrytaylorbonn/auxdrone/wiki/Robotic-AI-demos))**

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

A model contains the **NN/CNN/TF** and an **"internal" agent (iAgent)** that controls and provides access to the NN/CNN/TF. The iAgent implements an **API** that provides external access to the model.
  - **2b.2 Tiny demos**. 
  - **2b.2b Building models**.
  - **2b.3 Modifying models**.
  - **2b.4 Running models locally**. 


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
GPT: A tiny fine-tuning demo would be excellent
For example: M08 Tiny Fine Tune
  1. Load M01 model.pt, 2. Run inference, 
  3. Continue training for 100 epochs on slightly different data
  4. Save model_v2.pt, 5. Compare outputs before/after
This would teach the core idea:
  Fine-tuning = continue training an existing model on additional data.
  No transformers required. The exact same concept applies to LLMs, just at a much larger scale.
I actually think this would become one of the best demos in your 2b Models section because it bridges the gap between:
  training from scratch (Section 2), and
  using pre-trained models (Section 2b).
So yes—I would make Tiny Fine Tune the representative demo for 2b.3 Modifying models. It fits the section much better than the backdoor example.
```

<br>

#### **[2b.4 Running models locally](/2b.4-run-models-locally/)**<br>

```
GPT1: M07 FastAPI. This is where the model becomes a service. 
I think that's exactly what people need to understand
```

```
GPT2: Yes. I actually think Ollama is a better representative demo for 2b.4 Running models locally than M07 FastAPI.
The purpose of 2b.4 is not to teach FastAPI. It's to teach:
"How do I run a model on my own computer?"
Most people today will use something like:   Ollama, LM Studio, vLLM,   llama.cpp
rather than writing their own FastAPI server.
```

<br>

### **[3 External Agent demos](/3_agents/)**

The focus of this sections is the actual agents.

<!-- This is on the QS /0-qs.markdown/ page. -->

**3.1 Code-first (no AI)**. Most of the demos start out without AI to verify.

**3.2 Frameworks (no AI / automation)**. These are designed for any application, whether it uses AI or not. Examples: n8n, FastAPI, Flask, Django, Express.js, Spring Boot. One the best demos would be the n8n demo. The test things about n8n is you can run it easily locally (for free). n8n is not AI-only. Originally it was built as a workflow automation platform. For example: Gmail ↓ Save attachment ↓ Dropbox ↓ Send Slack message. No AI involved.

**3.3 Code-first (AI-assisted)**. The PAL/PAL_CORE demos. 

**3.4 AI Frameworks**. These are specifically designed to make building AI applications easier.
Examples: n8n (general automation, but now widely used for AI workflows). Gmail ↓ LLM summarizes email ↓ Store in MongoDB ↓ Mattermost alert. Other examples: LangChain,  LangGraph,  CrewAI,  OpenAI Agents SDK, PydanticAI. These assume that one or more models/LLMs are part of the application. *Note that LangChain, CrewAI, etc don't provide much value without AI. Their purpose is to orchestrate AI models, tools, memory, and workflows.*

*3 External agent ecosystem*<br>
<img src="/assets/6_main_diagram.png" alt="drones" width="40%"> 

<!-- The center of the Agentic AI universe is the AI agent.  The agent and LLM together can doing amazing things. But they also have severe limitations. "Tuning" then to work together is the core focus. Agents can also run without AI.  
- **[3.1 Agentic (no AI)](/3.1-agentic/)** <br> 
- **[3.2.5 Agentic + AI / PAL demos](/3.2.5-ai-agent-pal-demos/)**.   <br>
- **[3.2.4 Agentic + AI / Basic demos](/3.2.4-ai-agent-basic-demos/)**. <br>
-->
<!-- <img src="/assets/4_5_3x.png" alt="drones" width="20%"> <br><br>
<img src="/assets/calc1b.png" alt="drones" width="35%"> <br><br>
<img src="/assets/4_6_2x.png" alt="drones" width="20%">  <br>
<img src="/assets/4_5_3x_bbb.png" alt="drones" width="20%"><br><br>  -->
<!-- 
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
n8n or PydanticAI demo.
The framework itself isn't important.
The concept is.
```  -->

<br>

### **[3b Project demos](/3.3-ai-projects/)** (the end goal of ZiptieAI)

<!--This section focuses on "spinning up" real-world projects quickly with minimal code analysis or manual coding. --> 
<!-- ALSO: simply say "My demos use the external agent as the main application 
because I don't yet have a large production application to integrate AI into.""
That's easier to understand. -->

See "Concepts" for an explanation of S1-S4.

#### **PART 1: Enterprise SW demos** 

The real goal of AI projects is to integrate AI into an existing SW (ESW) app.

- **3b.11 SLACK** 
  - S1 Simply use the browser to access Slack.
  - S2a Claude + MCP → Slack ✅ (current demo). 
  - S2b Claude **Tag** in Slack ✅ (future demo after Claude gives acccess to the tag function my subscription class). This would be an **S2 Native/Managed AI**. 
  - S3 Slack app + OpenAI. Agent works as a Slack App / Bot (uses Slack APIs / users interact via Slack UI).

*3b Slack Project demo ecosystem for stages S1-S4 (S4 add DB?)*<br><img src="/assets/M-38.png" alt="drones" width="55%"> 

#### **Part 2: Standalone AI Application demos**.

- **3b.3 NMAP Security Assistant**. Uses the local PC as the target system. **S4 External AI agent / works OUTSIDE the target**.
- **3b.2 GMAIL (JobRadar)**. Standalone that happens to access Gmail API.  *Existing system > Gmail > External Agent > LLM > Summary / Alert.* 

*3b standalone AI app (S4 only)*<br>
<img src="/assets/M-41.png" alt="drones" width="30%"> 

<br><br><br><br><br><br>


--------------------------------------------
--------------------------------------------
--------------------------------------------
--------------------------------------------
--------------------------------------------
--------------------------------------------
--------------------------------------------

<br><br><br><br><br><br>

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



<!--
<img src="/assets/M-09.png" alt="drones" width="58%"> -->



<!-- *Human (left), LLM agent (center), and LLM transformer (right)*<br>  
<img src="/assets/M-11.png" alt="drones" width="31%"> -->

<br>



26.0628 (v1 26.0527)

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
<!--
  - **2.1 Core NN** (can be used alone or as CNN dense layers / TF FFN).  
  - **2.2 CNNs (convolution)** has an extra "NN" that performs convolution. 
  - **2.3.6 Transformers**. A bare bones but fully functional TF.
  - **2.5 Robotic AI** (Robotic AI is not a core focus right now).
  - **2b.2 Tiny demos**. 
  - **2b.2b Building models**.
  - **2b.3 Modifying models**.
  - **2b.4 Running models locally**. 
  - **3.1 Code-first agents**.
  - **3.2 Agent framework**. 
  - **3b.3 NMAP Security Assistant**. Uses the local PC as the target system. This is not only a practical tool, but also can help you learn very important security topics for your home PC/network setup.
  - **3b.2 JobRadar**. This intros hope to connect to email, etc to get a daily summary.  
-->
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

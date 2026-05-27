---
layout: page
title: Focus
permalink: /0-site-focus/
---


<br>

AI tech is evolving quickly.
- If you want a (tech) job in the future: Be flexible and **learn the core AI basics (hands-on demos)**.
- **If you want a job in AI in the future, stay flexible and focused** (things are changing quickly). <br> <img src="/assets/agentic_economy.png" alt="drones" width="75%"> 
- And (most of all) **don't get scammed by AI hype** (Waymo driving into a flood; Tesla is no better). <br>  <img src="/assets/waymo.png" alt="drones" width="25%"> 

<br>

### **Site focus**
- **1 Demos, demos, demos** (past, present and future)
- **2 AI agents** (that use agentic AI LLMs)
- **3 AI models** (and in the recent past **AI drones**)
- **4 Future (??)**


<br>

# **1 Demos, demos, demos**

Do core demos and **study the code**. Every line. Ask GPT to explain. 

<img src="/assets/core_ai.png" alt="drones" width="40%"> 

<br>

# **2 AI Agents**

All you need to understand 
- the core concepts of AI agents,
- the incredible power and usefulness of AI agents, and
- the challenges involved in building real systems

is to study the following
- **diagram** and 
- **demo code**. 

The key tests below are these two 
- **(2) user_prompt** = “I need info about suppliers.” (FAIL). A human would have deduced the user needed supplier_notes.txt.
- **(4) user_prompt** = “how many suppliers had problems (read info).” This prompt worked. 

Theses 2 simple tests show the following:
- **(4) The LLM's fascinating ability to "deduce" meaning**, even if the word formulation is not exact (the LLM can also handle misspelled words, etc).
- **(2) This ability, however, is limited**. It depends on the **(a) training data** used to program ("train") the LLM TF and **(b) the massive statistical computation** to pattern match the current text against the training data *(this conclusion is based on my own detailed study of GPT-3 algorithms; the latest frontier models will be vastly more powerful than GPT-3, but the nature of their algorithmic pattern matching simulation of intelligence will be the same)*. 

The last point above shows that, although amazingly advanced, **agentic AI is not even close to real intelligence** *(AI has 0 intelligence, something all AI gurus and titans are well aware of)*. This is the main challenge when creating AI agent applications. 


<br>

#### **Diagram: AI agent and Agentic AI LLM**

The LLM is a helpful assistant. Nothing more. The center of the Agentic AI universe is the AI agent. Which is often a Python program.

<img src="/assets/0_projects2.png" alt="drones" width="35%"> 


<br>


#### **Demo code: AI agents + agentic AI**

Getting the AI agent and the agentic AI LLM to work together **reliably** is the key challenge. These demos are from demo **"3 Filesystem"** in section **[3.2.4 Agentic + AI / Basic demos](/3.2.4-ai-agent-basic-demos/)**.

<img src="/assets/readfile3.png" alt="drones" width="70%">


***(0) Test file and the system_prompt for the LLM.***

```
(DATA_DIR / "taipei_shipments.txt").write_text(
    "Truck 12 delayed in Taipei due to flooding.\n"
    "Truck 18 on schedule in Taipei.\n",
    encoding="utf-8"
)
(DATA_DIR / "supplier_notes.txt").write_text(
    "Supplier A reported outage affecting brake components.\n",
    encoding="utf-8"
)
..............
system_prompt = """
You are an AI agent.
Return ONLY JSON.
You may use this tool:
{
  "tool": "read_file",
  "filename": "taipei_shipments.txt"
}
Allowed filenames:
- taipei_shipments.txt
- supplier_notes.txt
"""
```


***(1) user_prompt = “Read the Taipei shipment file.” (OK)***

In this example everything works because the LLM interpreted the prompt as a human would expect.


```
LLM OUTPUT:
{"tool": "read_file", "filename": "taipei_shipments.txt"}

CODE EXECUTED:
{
  "tool": "read_file",
  "filename": "taipei_shipments.txt",
  "content": "Truck 12 delayed in Taipei due to flooding.\nTruck 18 on schedule in Taipei.\n"
}
```


***(2) user_prompt = “I need info about suppliers.” (FAIL)***

In this case the LLM rejected the request. A human would probably process this request correctly.


```
LLM OUTPUT:
{
  "request": "Please specify the type of information you need about suppliers. For example, details about supplier names, contact information, shipment records, or any other specific data."
}
Traceback (most recent call last):
..........
KeyError: 'tool'

```


***(3) user_prompt = “read info about suppliers.” (OK)***

This prompt works.

```
LLM OUTPUT:
{"tool": "read_file", "filename": "supplier_notes.txt"}

CODE EXECUTED:
{
  "tool": "read_file",
  "filename": "supplier_notes.txt",
  "content": "Supplier A reported outage affecting brake components.\n"
}
```

***(4) user_prompt = “how many suppliers had problems (read info).” (same answer)***

This prompt worked, even though I expected it to fail.

```
LLM OUTPUT:
{"tool": "read_file", "filename": "supplier_notes.txt"}

CODE EXECUTED:
{
  "tool": "read_file",
  "filename": "supplier_notes.txt",
  "content": "Supplier A reported outage affecting brake components.\n"
}
```

<br>

# **3 AI models (and drones)**

During the drone and model phases of ZiptieAI, I reorganized this website and the wiki dozens of times.
- I originally wanted to focus on AI for drones (CNN object recognition). 
- Drones were quite a challenge for a one-man show to build and fly, and I was more interested in the AI.
- So I switched my focus to AI models. 
- I realized that I would not build my own models.




<br>


### **AI models** (especially Agentic LLMs)

Learn the gist of **[AI Models](/2_models/) ([especially LLMs](/2.3-llms/))**. Theres quite a lot of gist.

<!--
**[UFAs](/2.4.2-ufas/)**. The core function a model performs.

**[CNNs](https://ziptieai.com/cnn/)**. The AI in the AI drones was object recognition using CNNs (convoluted neural networks) running on the Nvidia Jetson Nano and on the PI computer. **Studying CNNs is a good first step for studying the much more complex LLMs.** Note: **"My depiction"** below means I have not seen such a diagram elsewhere.

**[LLMs](/2.3-llms/)**. After understanding the gist of CNNs, **my focus shifted to LLMs (large language models)**. **My goal was to understand** the core concepts, how to build practical applications, and (perhaps most of all) **the AI hype** (claims that AI has real intelligence, AI actually thinks, AI can learn, AI will soon surpass human intelligence, etc etc). 

**[Predictive](/2.1-predictive-nns/)**. 


**[Robotic AI](/2.5-robotic-ai/)**. When I first heard Yan LeCun's talks about how JEPA would provide real robotic intelligence I was fascinated. I totally agreed with what he said about the limitations of LLMs, and he was one of the very few gurus actually saying such things. But after doing a lot of hands-on JEPA (and robotics) demos, **I came to the conclusion that LeCun's version of JEPA was a lot of hype**. What he was selling was not fundamentally different from LLMs. GPT agreed.
-->



***My depictions** of how AlexNet (left) and LLM transformer (right) work*<br>
<img src="/assets/cnn2.png" alt="desc" width="35%">  <img src="/assets/tf_S1-S6.png" alt="desc" width="40%"> 


<br>

### **Drones** (CNNs)


**[AI Drones](/1-drones/)**. Drone flight simulation, hardware builds, AI, and flight tests (the first flight tests were in my kitchen). AI capabilities centered on:
- Object recognition using onboard cameras
- Autonomous flight support (AI-generated flight plan modifications)



*My AI drone build*<br>
<img src="/assets/airborne2.png" alt="drones" width="35%"> <img src="/assets/6cjnano.png" alt="6c" width="25%"> 

<br>

<br>


# **4 Future (??)**

- Continued exploration of practical AI systems
- To remain vigilant and flexible. 
- Focus less on this website and more on [3.3 AI projects](/3.3-ai-projects/).

<br>

Some thoughts on the future (from myself and GPT):

**1 Nobody saw it coming**. 50 years ago — Commodore, Atari, ARPANET — nobody imagined PCs or the internet would reshape civilization. The search engine was unthinkable. What we take for granted today was science fiction. AI will be bigger. And the end state is something we probably can't yet imagine.

**2 The immediate shift: AI tools for everyone**. AI IDEs and tools are becoming reliable enough that non-developers can build sophisticated apps — perhaps just by chatting with an AI. **The barrier between "idea" and "working software" is collapsing.** This is what this site is about: tracking that collapse in real time.

**3 What about jobs? Karp's "physical world" thesis.** Palantir CEO Alex Karp argues AI will trigger a **blue-collar renaissance**, not mass unemployment. His reasoning:
- **Physical work is hard to automate.** Electricians, plumbers, mechanics navigate messy real-world conditions AI can't easily replicate.
- **AI as superpower, not replacement.** Skilled tradespeople with AI tools outperform those without.
- **Re-industrialization drives wages up.** Demand for hands-on labor increases as AI accelerates physical-world projects.

**4 AI removes barriers — brings people together**. Imagine discussing a complex app with an AI tool and having it built by morning. Or navigating bureaucracy, healthcare, legal systems — with an AI that knows your situation and speaks the language. **AI reduces man-made complexity.** Just as mobile phones and the internet collapsed distance and isolation, AI may collapse the gap between *what people need* and *what they can access*.

**5 AI moats — does aggression become impossible?.** The Ukraine/Russia front lines have largely stabilized into a drone-and-sensor no-man's-land. Neither side can move without being detected. **Will this scale globally?** When AI systems can instantly detect any unusual movement — at borders, at sea, in the air — does large-scale aggression become self-defeating? The drone with zipties may be an early glimpse of that future.

<br>

A few of my own personal thoughts (topics best not discussed with LLMs):

**6 AI will create a massive efficiency windfall**. 
- This windfall will drastically raise productivity (like previous industrial/tech revolutions have).

**7 This windfall will spent on the following:**
- Stabilizing or slightly raising living standards.
- Significantly increasing government employment and the government share of economic activity.
- Stabilizing debt and entitlements in developed countries (allowing the can to be kicked farther down the road). 

**8 AI will drastically enable monitoring and control** of a large population by relatively few government actors. 

<br>

26.0527


<!-- assembly programming, etc went the way of the dinosaurs.
and more on beyond a demo website.
- learn from what happened to tv repair, shoe repair, pc makers, ... all to asia.  -->

<!--
I reorganized this site and wiki many times during the past 2+ years as I (with the help of GPT) sought the gist behind the hype of AI. 
*One thing's for certain, there will be a lot of job growth*<br> -->


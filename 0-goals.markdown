---
layout: page
title: Goals
permalink: /0-goals/
---


<br>

AI tech is evolving quickly.
- If you want a job in the future, be flexible, learn AI. 
- **If you want a job in AI in the future, be much more flexible and focused**. 


<img src="/assets/agentic_economy.png" alt="drones" width="75%"> 


<!--
I reorganized this site and wiki many times during the past 2+ years as I (with the help of GPT) sought the gist behind the hype of AI. 
*One thing's for certain, there will be a lot of job growth*<br> -->

<br>

### **My personal goals** (and the focus of this site)
- **1 Present: AI agents** (that use agentic AI LLMs)
- **2 Recent past: AI models and drones**
- **3 Future (continued exploration of practical AI systems)**


<br>

# **1 Present goal: AI Agents (that use agentic AI)**

All you need to understand 
- the core concepts of AI agents
- the incredible power and usefulness
- the challenges involved in building real systems

is to study the following
- **diagram** and 
- **demo code**


<br>

#### **Diagram: (4) AI agent and (2) Agentic AI LLM**

<img src="/assets/0_projects2.png" alt="drones" width="45%"> 




<br>


#### **Demo code: AI agents + agentic AI**

These demos are from demo **"3 Filesystem"** in section **[3.2.4 Agentic + AI / Basic demos](/3.2.4-ai-agent-basic-demos/)**.


**user_prompt = “Read the Taipei shipment file.” (OK)**



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


**user_prompt = “I need info about suppliers.” (FAIL)**



```
LLM OUTPUT:
{
  "request": "Please specify the type of information you need about suppliers. For example, details about supplier names, contact information, shipment records, or any other specific data."
}
Traceback (most recent call last):
  File "C:\Users\terry\Downloads\d1_agent\ai_demo_03_filesystem.py", line 98, in <module>
    if action["tool"] == "read_file":
       ~~~~~~^^^^^^^^
KeyError: 'tool'

```


**user_prompt = “read info about suppliers.” (OK)**



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

**user_prompt = “how many suppliers had problems (read info).” (same answer)**

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

# **2 Recent past: AI models and drones**

learn the background, from my mistakes.
study how i got here.
reorg'd this website, wiki dozens of times.

assembly programming, etc went the way of the dinosaurs.


<br>


### **AI models (especially Agentic LLMs)**

dont bother with LLM internals. 
just understand the gist.
Theres quite a lot of gist.

**[UFAs](/2.4.2-ufas/)**. The core function a model performs.

**[CNNs](https://ziptieai.com/cnn/)**. The AI in the AI drones was object recognition using CNNs (convoluted neural networks) running on the Nvidia Jetson Nano and on the PI computer. **Studying CNNs is a good first step for studying the much more complex LLMs.** Note: **"My depiction"** below means I have not seen such a diagram elsewhere.

**[LLMs](/2.4-llms/)**. After understanding the gist of CNNs, **my focus shifted to LLMs (large language models)**. **My goal was to understand** the core concepts, how to build practical applications, and (perhaps most of all) **the AI hype** (claims that AI has real intelligence, AI actually thinks, AI can learn, AI will soon surpass human intelligence, etc etc). 

**[Predictive](/2.2-predictive-nns/)**. 


**[Robotic AI](/2.3-robotic-ai/)**. When I first heard Yan LeCun's talks about how JEPA would provide real robotic intelligence I was fascinated. I totally agreed with what he said about the limitations of LLMs, and he was one of the very few gurus actually saying such things. But after doing a lot of hands-on JEPA (and robotics) demos, **I came to the conclusion that LeCun's version of JEPA was a lot of hype**. What he was selling was not fundamentally different from LLMs. GPT agreed.


<br>

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


# **3 Future goals** (continued exploration of practical AI systems)

<br>

- to predict future goals, jobs, AI directions.
- beyond a demo website.
- learn from what happened to tv repair, shoe repair, pc makers, ... all to asia. 


<br>


**1 Nobody saw it coming**. 50 years ago — Commodore, Atari, ARPANET — nobody imagined PCs or the internet would reshape civilization. The search engine was unthinkable. What we take for granted today was science fiction. AI will be bigger. And the end state is something we probably can't yet imagine.

**2 The immediate shift: AI tools for everyone**. AI IDEs and tools are becoming reliable enough that non-developers can build sophisticated apps — perhaps just by chatting with an AI. **The barrier between "idea" and "working software" is collapsing.** This is what this site is about: tracking that collapse in real time.

**3 What about jobs? Karp's "physical world" thesis.** Palantir CEO Alex Karp argues AI will trigger a **blue-collar renaissance**, not mass unemployment. His reasoning:
- **Physical work is hard to automate.** Electricians, plumbers, mechanics navigate messy real-world conditions AI can't easily replicate.
- **AI as superpower, not replacement.** Skilled tradespeople with AI tools outperform those without.
- **Re-industrialization drives wages up.** Demand for hands-on labor increases as AI accelerates physical-world projects.

**4 AI removes barriers — brings people together**. Imagine discussing a complex app with an AI tool and having it built by morning. Or navigating bureaucracy, healthcare, legal systems — with an AI that knows your situation and speaks the language. **AI reduces man-made complexity.** Just as mobile phones and the internet collapsed distance and isolation, AI may collapse the gap between *what people need* and *what they can access*.

**5 AI moats — does aggression become impossible?.** The Ukraine/Russia front lines have largely stabilized into a drone-and-sensor no-man's-land. Neither side can move without being detected. **Will this scale globally?** When AI systems can instantly detect any unusual movement — at borders, at sea, in the air — does large-scale aggression become self-defeating? The drone with zipties may be an early glimpse of that future.

<br>

26.0521

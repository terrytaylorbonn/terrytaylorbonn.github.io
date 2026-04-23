---
layout: page
title: ZiptieAI History
permalink: /history/
---

<br>

ZiptieAI has evolved with AI technology. What began as a drone-focused project became an exploration of practical AI systems.


<br>

#### (1) [AI Drones](/aidrones/)

This phase included drone flight simulation, hardware builds, and flight tests (the first flight tests were in my kitchen).

AI capabilities centered on:
- Object recognition using onboard cameras and CNNs
- Autonomous flight support (AI-generated control inputs that could modify flight plans)

My original plan was to spend my time developing the AI part of AI drones. For me the drones were only the carrier platforms. But I ended spending most of my time on the drones because of 
- Open source software (outdated, with some core documents over 10 years old)
- Components sourced from China (quality and documentation issues)

I wanted to volunteer to build drones in Ukraine, but no success (even as a volunteer; complicated country). It seemed that to get a drone job in the West you needed to an expert in building (1) the platform or (2) the AI (preferably in both).  

<br>


#### [(1b) Tech Stacks & Docs](/tech-stacks/)

I maintained very good documentation of my AI drones activities (especially the critical tech details that were missing in the outdated documentation; some of the core docs/tools had not been updated for over a decade). My original plan was to build my own ZiptieAI website, wiki, and blogs (Substack and Youtube). 

The first step was an "inventory" (refresher course) of the latest doc tools (MERN stacks, REST/GraphQL APIs/docs). But for the first time I used AI tools for assistance. Wow. Suddenly using these doc tools (whose own documentation was of usually of limited use) had become vastly simpler. 

A wakeup call. The AI tools became the focus. 

<br>

#### (2) [LLMs](/sandbox/)

My focus shifted to the new revolutionary AI tools:
- CNNs (convoluted neural networks). CNNs were the basic of the drone oject recognition. 
- LLMs (large language models) and in particular the LLM TF (transformer neural network). 
  - API-based model usage (major frontier models)
  - Local and remote model deployment (smaller models)
  - Fine-tuning
  - RAG, MCP, and tools

I also became particulary interested in the hype surrounding these tools. I did not have to be an AI expert to understand that the expert claims about AI having real intelligence, emotions, consciousness, etc were knowingly false. AI runs on clocked binary circuits, nothing at like the neurons in the brain. I had read many times that up to 95% of AI projects failed. That meant that 20x more money than necessary was being spent on AI projects. The hype was quite effective.

The value of a firm grasp of AI fundamentals was obvious. My goal was to understand the core concepts and how to build practical applications.

<br>

#### (3) [Robotic AI](/robotic-ai/)

AI makes mistakes. Your chat AI warns you about this constantly, although chatbot mistakes are not dangerous. But for robots (especially those around humans, such as cars and humanoids) mistakes can be fatal. So I never experienced much interest in AI for robots (and I have never had the desire to ride in a driverless car). AI's mistakes are unavoidable, because AI is based on massive brute-force GPU computations that analyze the input (based on the "training" inputs) and output the most probable answer (note that an LLM rarely says "I don't know"). 

So I was quite interested when I heard about Yan LeCun claims that JEPA was leading to brighter future where robots would have "real" intelligence (not the "fake" LLM intelligence, not the "dead end"). It took a while to sift through the JEPA hype, but I did. After doing a lot of demos, I asked GPT how, if JEPA and LeCun's new products will both continue to use TFs, will they be fundamentally different from LLMs. GPT said they won't be. 

In any case, the time spent doing hands-on demos for representational learning, prediction-based systems, belief tracking, control loops, planning under uncertainty, etc was well spent. Many of the concepts (such as estimation and autonomy) were related to earlier drone work.

<br>

#### (4) [Agentic AI](/agentic-ai/)

AI agents are the deterministic control loops (often written in Python) that are the real core of AI applications. "Autonomous" AI agents perform complex tasks with limited (but critical) human intervention. For me the real opportunities in AI are primarily in this area. 

All of my previous AI experience provides a solid foundation for working with Agentic AI. Not only to understand how it works, but also to recognize quickly the invevitable hype. A great example of such hyper is that agentic AI is going to take over the world (which probably helps sell more agentic AI). 

An example of this is the hype around Palantir systems used in the Iran war. When I first heard of Palantir's systems I immediately became interested because 
- (1) they work, 
- (2) they can most certainly be used for a vast array of non-military purposes (logistics, manufacturing, healthcare, defense, operations, business intelligence), and 
- (3) there were (totally unrealistic) claims that Palantir's systems could become the real world [SkyNet](https://en.wikipedia.org/wiki/Skynet_(Terminator)). 

Point (3) above is an inevitable conclusion when Palantir's systems are mistakenly referred as AI-based. They are not based on AI, they are assisted by AI. The core control loop is traditional non-AI deterministic programming (and totally CPU-based). AI is used for 
- Input and output (of "messy" human language data)
- Task planning (breaking up complex tasks into smaller tasks)
- "Rule" injection (the main loop is programmed to process any added "rules")

Point (3) is also based on the mistaken assumption that such systems will be used for control of external physical actuators (robots, weapons, cars, etc). These system are used for analysis. The entire system is still a "helpful assistant".

Agentic AI (non-AI deterministic control loop helpful assitants that use AI as a helpful assistant) is likely to be one of the fastest-growing areas of AI in the near future. The success of Palantir shows that such systems are already viable AI applications.


<br>

26.0423

---
layout: page
title: ZiptieAI History
permalink: /history/
---

<br>

AI tech is evolving quickly. ZiptieAI is evolving along with it. What began as a drone-focused project has become an exploration of practical AI systems.


<br>

#### (1) [AI Drones](/aidrones/)

This was the first phase of ZiptieAI (the name was inspired by the zipties Ukraine used to quickly configure drones). This phase included drone flight simulation, hardware builds, AI, and flight tests (the first flight tests were in my kitchen).

AI capabilities centered on:
- Object recognition using onboard cameras
- Autonomous flight support (AI-generated flight plan modifications)

My original plan was to spend the majority of my time on the drone AI (the drones were only meant to be carrier platforms). But I ended spending most of my time on building drones because of quality and usability issues the open source software and components. My original goal was to work as a volunteer building drones in Ukraine.  

<br>


#### [(1b) Tech Stacks & Docs](/tech-stacks/)

I documented my AI drones activities in detail. My original plan was to build my own ZiptieAI website, wiki, and blogs (Substack and Youtube) that focused exclusively on drones. The first step was an "inventory" (refresher course) of the latest doc tools (MERN stacks and REST/GraphQL APIs/docs). 

For the first time I started using AI tools for coding. I was amazed by how much these AI tools simplified development.   

<br>

#### (2) [LLMs](/sandbox/)

My focus shifted to AI:
- CNNs (convoluted neural networks). CNNs were the basic of the drone oject recognition. Studying CNNs was good preparation for the much more complex LLMs.
- LLMs (large language models)
  - Transformers (the LLM neural network). 
  - API-based model usage (major frontier models)
  - Local and remote model deployment (smaller models)
  - Fine-tuning
  - RAG, MCP, and tools

I became particulary interested in the claims about AI having intelligence (and emotions, consciousness, etc). AI runs on clocked binary circuits (nothing like the neurons in the brain). Theoretically you could build a "mechanical" GPU and run AI on it (it would require perhaps years to generate a token). The only difference between the electronic and mechanical GPU would be the execution speed.

I had read that up to 95% of AI projects failed. That meant that 20x more money than necessary was being spent on AI projects. The value of a firm grasp of AI fundamentals was obvious. My goal was to understand the core concepts and how to build practical applications.

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
- (3) there were (totally unrealistic) claims that Palantir's systems could become the real world [SkyNet](https://en.wikipedia.org/wiki/Skynet_(Terminator)) (see my substack post [#73 Understanding Palantir Maven / Why AI will never become Skynet](https://ziptieai.substack.com/p/73-understanding-palantir-maven-through)).

Point (3) above is an inevitable conclusion when Palantir's systems are mistakenly referred as AI-based. They are not based on AI, they are assisted by AI. The core control loop is traditional non-AI deterministic programming (and totally CPU-based). AI is used for 
- Input and output (of "messy" human language data)
- Task planning (breaking up complex tasks into smaller tasks)
- "Rule" injection (the main loop is programmed to process any added "rules")

Point (3) is also based on the mistaken assumption that such systems will be used for control of external physical actuators (robots, weapons, cars, etc). These system are used for analysis. The entire system is still a "helpful assistant".

Agentic AI (non-AI deterministic control loop helpful assitants that use AI as a helpful assistant) is likely to be one of the fastest-growing areas of AI in the near future. The success of Palantir shows that such systems are already viable AI applications.


<br>

26.0423

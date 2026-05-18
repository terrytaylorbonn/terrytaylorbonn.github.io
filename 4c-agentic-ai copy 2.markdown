---
layout: page
title: "3.2 (4c) Agents + AI"
permalink: /4c-agentic-ai/
---


<br> 

**TOC CURRENT** 

- **1 Concepts**. AI is only a (extremely) helpful assistant.
- **2 Diagrams**
- **3 Agent <-> LLM functional overview**.
- **4 Agent+AI demos**. Lab notes on my Gdrive. Code on my Github.

<br> 

**TOC NEW (WIP; I am reorganizing 26.0518-19)**<br>
*See [#606_ai_ides_.docx (on Gdrive)](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO) chapters "Agentic AI DEMOS" and "3.2 Agents + AI" for content to be add to these pages.*
- [3.2.1 Agents + AI / Intro](/3.2-ag-ai-1-intro/)
- [3.2.2 Agents + AI / Diagrams](/3.2-ag-ai-2-diagrams/)
- [3.2.3 Agents + AI / Agentic AI functionality](/3.2-ag-ai-3-ag-ai-func/)
- [3.2.4 Agents + AI / AI'ic agents functionality](/3.2-ag-ai-4-ai-ag-func/)
- [3.2.5 Agentic + AI / AI'ic agents demos](/3.2-ag-ai-5-ai-ag-demos/)
- [3.2.6 Agentic + AI / PAL demos](/3.2-ag-ai-6-pal-demos/)

<br>

Notes:
- [4a chat about iAgent and eAgent](/4a-chat-about-iAgent-and-eAgent/) 26.0514


<br>

# **1 Concepts**

<br>

**Just like iAgent and TF work together, so must extAgent and LLM.**

- 1.1 Agents existed long before AI
- 1.2 Agentic AI (LLMs designed for agents)
- 1.3 AI'ic agents
- 1.4 Model interface layer (MIL)



<br>

### **1.1 Agents existed long before AI**


Your entire architecture is basically:
- **#1 deterministic agent systems existed before LLMs (BUT were expensive and rigid).**
- **2 TF/UFA semantic capabilities made those systems vastly more practical and flexible.**

That is actually a very strong and coherent thesis.


Yes — honestly I think that is now a very strong core thesis for the entire Agentic AI section.
It is:
-	simple 
-	historically grounded 
-	technically meaningful 
-	consistent with your demos 
-	consistent with Palantir-style systems 
-	consistent with your:
LLM = propose
Code = executes
philosophy.
I would only slightly tighten the wording:
VERY IMPORTANT insight for this site

3.1 Deterministic agent systems existed before LLMs,
but were expensive, rigid, and difficult to scale.

3.2 TF/UFA semantic capabilities made such systems
vastly more practical and flexible by enabling:
- semantic interpretation
- structured outputs
- ontology alignment
- planning
- contextual reasoning
- generalization
- explanation generation

This is one of the core reasons modern agentic AI became practical.

I think that now ties together:
-	your PAL demos 
-	your ontology focus 
-	your UFA page 
-	your deterministic-agent viewpoint 
-	your skepticism of “AI magic” 
-	your emphasis on orchestration. 
The whole framework is becoming pretty coherent.

<br>

### **1.2 Agentic AI (LLMs designed for agents)**
 
The following are just a few examples of how AI is a very helpful assistant for agentic apps:
- Interpret/sanitize messy human language text
- Create human language explanations
- Planning (breaking up complex tasks into granular tasks that the agent can process reliably)
- Input and output (of "messy" human language representations)
- Rule injection (by AI into the main loop)

These capabilities an agentic AI app 
- vastly more flexible and capable
- at the cost of unpredictabilty (For many apps this is an excellent tradeoff)

they can be used for a vast array of  purposes (logistics, manufacturing, healthcare, defense, operations, business intelligence)


#### **About planning and other "intelligent" AI functionality**

*For background on VL, storylines, etc discussed below, see [The gist of LLMs](/gist-LLM/).*

In reality AI (in my always humble opinion) is more about pattern matching than language. You input messy human language tokens into the TF, and it generates a vector language (VL) representation of the storyline *(I don't really like the term "vector"; the 12288 vectors for GPT-3 are just scalar indicators of some pattern; usually a vector means a scalar with some other aspect, like direction, etc)*. The VL for the final token is pattern matched against all tokens in the vocabulary. The closest matching token for that pattern is selected as the next token.

It really is that simple. Then again, computers are all based on binary switches. But with a bit of ingeniuty you can milk such systems for all they are worth (and that can be quite a lot, for PC's and LLM's). An example: An LLM can detect (if it saw such a pattern before) that the word "milk" I used in the previous sentence was a verb and it was not about literally milking a cow. That is not intelligence, its pattern matching. 

<br>

### **1.3 AI'ic agents**

It took a decade for AI-assist to be added to Palantir agents (SW). Before AI Palantir agents used ontology (their own mini-dictionary) to limit the human language that could be used in their systems. And it worked. It required "sanitzing" all inputs, but it could process vast amounts of data, looking for that needle in the haystack that might signal another secret 9/11 style terrorist attack.

AI's arrival vastly enhanced Palantir system performance because their machines could now "communicate" freely with messy chaotic human language input. But Palantir's systems, like **all AI-ic agents systems, are assisted by AI (not controlled by AI)**. The LLM is simply a "helpful assistant". **LLMs control nothing, push no buttons**. 

But AI had to be the center of attention for all such projects. It wasn't "AI'ic agents", but rather "agentic AI". Something that might one day take over the world ([Skynet](https://en.wikipedia.org/wiki/Skynet_(Terminator)) style; *see my substack post [#73 Understanding Palantir Maven / Why AI will never become Skynet](https://ziptieai.substack.com/p/73-understanding-palantir-maven-through)*).  That hype generated a lot of publicity. 

I once read that 95% of AI projects fail. One reason is all the hype. The follwing diagram is an important example. *"What Is Agentic AI? Agentic AI is an innovative advancement in artificial intelligence (AI), characterized by its ability to independently make decisions and implement goal-oriented actions on behalf of users or systems." ([link](https://www.cadence.com/en_US/home/explore/agentic-ai.html))*

*An example of the LLM-centric agentic AI universe*<br>
<img src="/assets/4_9_cadence.png" alt="drones" width="10%"> 

Its quite important to understand what AI'ic agents AI is (at least hands-on experience with the basics). 

<br>

### **1.4 Model interface layer (MIL)**

(to switch models... iAgent and TF are customized to work together, agent and LLM maybe now, so need interface)

<br>

# **2 Diagrams**

<br>

- 2.1 Ecosystem
- 2.2 Agent <> LLM interface
- 2.3 Workflow diagram / simple
- 2.4 Workflow diagram / detailed

<br>

### **2.1 Ecosystem**


*The LLM as a helpful assitant for the agent*<br>
<img src="/assets/4_7_help_assist_LLM.png" alt="drones" width="40%"> 

<br>

### **2.2 Agent <> LLM interface**


*Details of the agent <> LLM interface*<br>
<img src="/assets/GPT_agent.png" alt="desc" width="50%"> 

<br>

### **2.3 Workflow diagram / simple**

Reference the diagram below:
- Agent collects human language data (blue square) from the UI, DB, APIs, etc.
- Agent forwards this human language with extra (human language + JSON) commands to LLM for processing (cleaning up, sanitizing).
- LLM (red square) converts the input into "machine" language (text, but text that conforms to the expectations of the agent) as specified by the JSON. 
- Agent then process this "machine" language" (customized specifically for the agent algorithms).<br>

*What AI does for an agent*<br>
<img src="/assets/4_8_what_ai_does.png" alt="drones" width="65%"> 

The following diagram shows an demo of this. 
- (1) 08b uses AI to generate a granular multi-step plan that matches the agent deterministic logic.
- (2) 08 (deterministic) validates the plan 
- (3) 08 (deterministic) excutes the plan 

*Diagram from Substack post [#75 The Real Job of AI in Enterprise Apps](https://ziptieai.substack.com/p/75-the-real-job-of-ai-in-enterprise) shows how AI is only used to generate a plan ("08b AI")*

<img src="/assets/aiplan.png" alt="AI planning" width="25%">

<br>

### **2.4 Workflow diagram / detailed**

Workflow details (see diagram below):
- **#1 UI/DB/API** (human language sources and destinations) **interface with #2 Agent** (the main loop).
- **#2 Agent adds extra info/requirements (JSON) to LLM input**. This instructes the LLM about what type of data and format to return.
- **#3 Model (LLM) interface layer**. Every LLM may require slightly different prompts and output slightly different responses. Palantir uses MIL to support "hot" swapping of LLMs. 
- **#4 Internal agent (iAgent) controls #5 TF**. The iAgent is custom designed to interface with the TF.
- **#5 TF creates output text** based on input text. Thats all the LLM TF does, and yet somehow the LLM seems intelligent.
- **#4 LLM iAgent sends response to #2 (external) agent.** 
- **#2 Agent processes the response.**

*Workflow diagram*<br>
<img src="/assets/4_10_workflow.png" alt="drones" width="65%"> 



<!-- ### 4.4 Core LLM roles in the demos
Page **[(4) Agentic AI](/agentic-ai/)** has links to the following 2 pages. These pages (WIP) list some Agentic demos (without/with) AI that I have setup. I will add more demos and document in the future.
- **[Agentic demos (no AI)](/agentic-demos-no-ai/)** (below left in grey). Palantir was building such system a generation ago, before AI. It can be done, but it takes a lot of work (setting up ontology).  
- **[Agentic demos with AI](/agentic-demos-with-ai/)** (below right in blue). With AI's human language abilites, Agentic can now work with "messy" human language data sources.
Note: The title of this section "UFA MAKES AGENTIC AI PRACTICAL **(FOR LIMITED USE CASES)**" means that **use cases with AI are still limited, but much less so than without AI.**
*Agentic demos (for details see the lab notes doc **#603\_PAL\_.docx** (PAL = Palantir) on my **[Gdrive](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**)*  <br>
<img src="/assets/4_5_3x.png" alt="no ai" width="25%"> <img src="/assets/4_6_2x.png" alt="drones" width="30%">  <img src="/assets/4_5_3x_bbb.png" alt="drones" width="30%"> **(2) ME: what would the list be like for how AI greatly help agents work properly**
https://ziptieai.com/UFAs/ talks about how transformer universal function approximator (UFAs) are critical for agentic ai. i think you once mentioned the 8 main functions of the agent (i think that was without ai). what would the list be like for how AI greatly help agents work properly? below is title and toc of the section on that page in the wiki about TF UFAs .................... 
**GPT: What TF/UFA capabilities make modern agentic AI possible?**
Your current list is already heading in the correct direction.
I would structure it around:
“What TF/UFA capabilities make modern agentic AI possible?”
Something like this:
(3b Advanced inference / trained TF-UFA capabilities (CRITICAL for AGENTIC AI))
-->


<br>


# **3 Agent <-> LLM functional overview**

<br>

#### **[4c.3 Agent <-> LLM functional overview](/4c.3-agent-llm-func-overview/) (temp working file)**

<br>


# **4 Agent+AI demos**

<br>

This page is WIP (v1 26.0509). I need to go back through these demos and document.

Simple demos are the best way to understand the core of agentic+AI apps. For details see the lab notes doc **#603\_PAL\_.docx** (PAL = Palantir) on my **[Gdrive](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**.  

<img src="/assets/4_6_2x.png" alt="drones" width="40%"> 
<img src="/assets/4_5_3x_bbb.png" alt="drones" width="40%"> 

<br>


26.0518
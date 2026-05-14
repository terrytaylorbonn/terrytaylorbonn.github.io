---
layout: page
title: "(4) Agentic AI"
permalink: /agentic-ai/
---

<br>

<!-- **26.0509 REWRITING THIS PAGE ... FINISH BY 26.05010. THIS IS THE CORE PAGE OF THIS WEBSITE. This page will explain how agentic AI really works (my take).** (My rewrite working notes: in docx #606 on gdrive (link in footer) search for ""(4) Agentic AI" rewrite"). -->

**This is perhaps the core page for this website. It describes my take on core Agentic AI concepts (with demos)**. The content (including the diagrams) on this page are mostly my own (hashed out with the help of AI LLMs). *See also the wiki pages **[Agentic AI](https://github.com/terrytaylorbonn/auxdrone/wiki/Agentic-AI)** and **[Agentic AI demos](https://github.com/terrytaylorbonn/auxdrone/wiki/4%E2%80%902-Agentic-AI-demos)**.*

<br> 

**TOC** 
- **1 Why learn agentic AI? (jobs)**. Agentic AI is incredibly useful in all business segments. The job growth will be phenomenal. 
- **2 Agent concepts**. The agent is the central control loop (I would call this perhaps the agentic app). 
- **3 Agent demos (no AI)**. Lab notes on my Gdrive. Code on my Github. 
- **4 Agent+AI concepts**. AI is only a (extremely) helpful assistant.
- **5 Agent+AI demos**. Lab notes on my Gdrive. Code on my Github.

Notes:
- [4a chat about iAgent and eAgent](/4a-chat-about-iAgent-and-eAgent/) 26.0514

<br>

# **1 Why learn agentic AI? (jobs)**

My interest toward agentic AI grew strongly during the Iran war, when I read about how Palantir's AI systems had radically changed the nature of warfare. This was an application of AI that worked. No hype. My interest only grew stronger when I saw how agentic AI was going to be the growth market of the future. What revolutionized the battlefield will also revolutionize business. 

*The future agentic AI job market*<br>
<img src="/assets/4_1_goldman.png" alt="drones" width="75%"> 

I also wanted to see through the AI hype. Even if you dont plan to develop Agentic AI apps, you will undoubtedly still need to deal with them. It took a decade for AI-assist to be added to Palantir systems. And then came the hype. AI had to be the center of attention. It wasn't "AI-istic agents" (a tongue twister), but rather "agentic AI". Something that might one day take over the world ([Skynet](https://en.wikipedia.org/wiki/Skynet_(Terminator)) style).  That hype generated a lot of publicity. I once read that 95% of AI projects fail. Its quite important to understand what agentic AI is (at least hands-on experience with the basics). 

*An example of the LLM-centric agentic-AI universe: "What Is Agentic AI? Agentic AI is an innovative advancement in artificial intelligence (AI), characterized by its ability to independently make decisions and implement goal-oriented actions on behalf of users or systems." ([link](https://www.cadence.com/en_US/home/explore/agentic-ai.html))*  <br>
<img src="/assets/4_9_cadence.png" alt="drones" width="35%"> 


<!-- 
It took a decade for AI-assist to be added to Palantir systems. And then came the hype. AI had to be the center of attention, the center of the universe. It wasn't "AI-istic agents", but rather "agentic AI". Something that might one day take over the world (Skynet style https://en.wikipedia.org/wiki/Skynet_(Terminator) ).  

That hype brought in the big bucks. All kinds of free publicity. Lots of companies spending big bucks on something that doesn't work (for types of applications it was never designed for). Like FSD (full self driving) that could not drive itself (safely, even today).


*An example of the LLM as the core of the Agent (LLM-centric universe): "What Is Agentic AI? Agentic AI is an innovative advancement in artificial intelligence (AI), characterized by its ability to independently make decisions and implement goal-oriented actions on behalf of users or systems." From [Cadence](https://www.cadence.com/en_US/home/explore/agentic-ai.html).*  <br>
<img src="/assets/4_9_cadence.png" alt="drones" width="35%"> 

<br>

#### =1 LLMs have no intelligence

4.3 Knowing what to expect from a PC requires knowing its fundamentals.
it helps to compare this to the PC. all that high level software components are built on binary logic. its really incredible that binary logic can do this. 

TFs are built on matrix math. Thats it. LLMs = TF + iAgent = simulated intelligence. its a UFA .. universal function approximator. best guess based on statistics.  and its quite complex.... depends on training set.. so very difficult to ensure all is correct. 

in the TF human lang tokens are converted by TF to hidden states (12K FP numbers per token for GPT-3). TF performs a massive amount of computation on the hidden states for all tokens (up to millions of billions or more computations) to compute the the best new token. This is the the core of so-called "intelligence" in LLMs (in reality there is no intelligence; thats precisely why you need the agent in the first place).

-->




<br>

# **2 Agent concepts**

- 2.1 The agentic mission 
- 2.2 Ontology

<br>

### 2.1 The agentic mission 

**Palantir agentic systems (no AI) started around 2003 in response to the 9/11 attacks.** The US government wanted to make sure such an event did not happen again. 

<img src="/assets/4_2_wtc.png" alt="drones" width="35%"> 

The mission goals were quite clear: Detect any strange new activity that might indicate a security threat *(such as a bunch of foreign nationals wanting all of a sudden to learn on flight simulators how to fly airliners)*. Palantir was to be the (automated) system for this critical mission. **A system that watches the world (like a sorcerer looking into his crystal ball) 24/7, 365 days a year.**

*A palantír is one of several indestructible crystal balls from the novel"The Lord of the Rings" used to see events in other parts of the world [(Wiki)](https://en.wikipedia.org/wiki/Palant%C3%ADr)*<br>
<img src="/assets/4_3_crystal_ball.png" alt="drones" width="20%"> 

*In an agentic system a deterministic program (like Python) is the sorcerers ball* <br>
<img src="/assets/4_4_agent_ball.png" alt="drones" width="30%"> 

<br> 
 
### 2.2 Ontology
Palantir ontology is something between free-form text and a rigid database. You simply (1) restrict the allowed vocabulary and (2) specify relationships between DB entries. This ensures that the deterministic agent loop can process the DB content without errors (you cant simply automatically ingest "messy" human language without AI).

*[Ontology (wiki)](https://en.wikipedia.org/wiki/Ontology_%28information_science%29)* <br>
<img src="/assets/4_5_onto.png" alt="drones" width="45%"> 

<br>
 
# **3 Agent demos (no AI)**

<!-- (no AI) on my GIT (docx #603 chapters [2.x] pal_vx, [3.x] pal_core_0x)(LINK TO OTHER PAGE.... put details there)  For details see the lab notes doc **#603\_PAL\_.docx** (PAL = Palantir) on my **[Gdrive](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**.  -->

Simple demos are the best way to understand the basics of agentic apps. For details see page **[Agentic demos (no AI)](/agentic-demos-no-ai/)**.

<img src="/assets/4_5_3x.png" alt="drones" width="45%"> 

<br>

# **4 Agent+AI concepts**

- 4.1 Why agentic needs AI
- 4.2 What AI does for an agent
- 4.3 Workflow diagram 
- 4.4 Core LLM roles in the demos
- 4.4b version 2 26.0512
<!-- - 4.4 Agentic AI = human language <-> machine language interface -->

<br>

### 4.1 Why agentic needs AI

 
The following are just a few examples of how AI is a very helpful assistant for agentic apps:
- Interpret/sanitize messy human language text
- Create human language explanations
- Planning (breaking up complex tasks into granular tasks that the agent can process reliably)

These capabilities an agentic AI app 
- vastly more flexible and capable
- at the cost of unpredictabilty.

For many apps this is an excellent tradeoff. 

*The LLM as a helpful assitant for the agent*<br>
<img src="/assets/4_7_help_assist_LLM.png" alt="drones" width="45%"> 

<br>
 
### 4.2 What AI does for an agent

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

<img src="/assets/aiplan.png" alt="AI planning" width="85%">



<br>

### 4.3 Workflow diagram 

Workflow details (see diagram below):
- **#1 UI/DB/API** (human language sources and destinations) **interface with #2 Agent** (the main loop).
- **#2 Agent adds extra info/requirements (JSON) to LLM input**. This instructes the LLM about what type of data and format to return.
- **#3 Model (LLM) interface layer**. Every LLM may require slightly different prompts and output slightly different responses. Palantir uses MIL to support "hot" swapping of LLMs. 
- **#4 Internal agent (iAgent) controls #5 TF**. The iAgent is custom designed to interface with the TF.
- **#5 TF creates output text** based on input text. Thats all the LLM TF does, and yet somehow the LLM seems intelligent.
- **#4 LLM iAgent sends response to #2 (external) agent.** 
- **#2 Agent processes the response.**

*Workflow diagram*<br>
<img src="/assets/4_10_workflow.png" alt="drones" width="70%"> 

<br>


### 4.4 Core LLM roles in the demos

<!-- LLM (iAgent/TF) combo thinking / planning tricks (core functionality that makes agentic AI possible) This can do many things such as
-	standardize messy inputs (messy vocab and meet JSON requirements)
-	planning into small steps
-	rule injection -->

The iAgent/TF duo has functionality that seems to be genuinely intelligent.  

*LLM iAgent/TF*<br>
<img src="/assets/4_12_tf_hidden_states.png" alt="drones" width="30%"> 

<!-- [3.6] (WIP) pal_core_06: simplest demo of all core LLM roles 26.0416
#585 could you create a minimalistic demo that demos the key ways an LLM capabilities can be used in the types of system we have been creating? 
for example, 
(1) input human language commands, 
(2) insert new rules, etc? 
for now, could you just list those key ways?
GPT: Yes. That would be an excellent meta-demo:
one small system showing the main ways an LLM adds value inside structured applications.
For now, here is the concise list of key LLM capabilities relevant to the systems you’ve been building. -->


The following is a list of core LLM Roles in the demos (GPT)<br>

**1. Human Command Interpreter<br>**
Convert vague user language into structured actions.<br>
"Show delayed shipments in Taipei"<br>
-> {"action":"query","filter":...}<br>
**2. Messy Data Ingest / Extraction<br>**
Convert emails, logs, notes, reports into ontology records.<br>
email text -> event JSON<br>
**3. Planner / Task Decomposer<br>**
Break complex requests into atomic executable steps.
compare X vs Y<br>
-> step1 filter<br>
-> step2 aggregate<br>
-> step3 compare<br>
**4. Rule Generator / Rule Injection**<br>
Create new runtime rules without changing source code.<br>
"Alert if outage + delay + supplier overlap"<br>
-> new rule JSON<br>
**5. Semantic Mapping / Ontology Translation**<br>
Map inconsistent human wording into standard machine concepts.<br>
"flat tire", "blowout"<br>
-> tire_failure<br>
**6. Search / Retrieval Helper**. <br>
Turn natural language into queries or rank relevant records/documents.<br>
"What affects Site 1?"<br>
-> graph query / ranked docs<br>
**7. Explanation / Summarization**.<br>
Convert machine results into human-readable conclusions.<br>
3 suppliers affected due to shared parent + route dependency <br>
**8. Interactive Analyst Assistant**.<br>
Support iterative questioning.<br>
Why?<br>
Show evidence.<br>
What changed?<br>
What if road closed?

<br>


### 4.4b version 2 26.0512

From 6 HOW THE LLM TF UFA MAKES AGENTIC AI PRACTICAL (FOR LIMITED USE CASES)

<br> 

**GPT: Honestly, this is becoming a pretty coherent framework.**
You are basically describing:
•	why TF-UFAs are powerful semantic approximators 
•	why they work extremely well for information systems 
•	why they pair naturally with deterministic agents/software 
•	why ontology/schema-constrained outputs are critical 
That is a real architectural viewpoint, not just random AI buzzwords.

<br> 

Page **[(4) Agentic AI](/agentic-ai/)** has links to the following 2 pages. These pages (WIP) list some Agentic demos (without/with) AI that I have setup. I will add more demos and document in the future.
- **[Agentic demos (no AI)](/agentic-demos-no-ai/)** (below left in grey). Palantir was building such system a generation ago, before AI. It can be done, but it takes a lot of work (setting up ontology).  
- **[Agentic demos with AI](/agentic-demos-with-ai/)** (below right in blue). With AI's human language abilites, Agentic can now work with "messy" human language data sources.

Note: The title of this section "UFA MAKES AGENTIC AI PRACTICAL **(FOR LIMITED USE CASES)**" means that **use cases with AI are still limited, but much less so than without AI.**

*Agentic demos (for details see the lab notes doc **#603\_PAL\_.docx** (PAL = Palantir) on my **[Gdrive](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**)*  <br>
<img src="/assets/4_5_3x.png" alt="no ai" width="25%"> <img src="/assets/4_6_2x.png" alt="drones" width="30%">  <img src="/assets/4_5_3x_bbb.png" alt="drones" width="30%"> 

<br>

<!--**(2) ME: what would the list be like for how AI greatly help agents work properly**
https://ziptieai.com/UFAs/ talks about how transformer universal function approximator (UFAs) are critical for agentic ai. i think you once mentioned the 8 main functions of the agent (i think that was without ai). what would the list be like for how AI greatly help agents work properly? below is title and toc of the section on that page in the wiki about TF UFAs .................... 
**GPT: What TF/UFA capabilities make modern agentic AI possible?**
Your current list is already heading in the correct direction.
I would structure it around:
“What TF/UFA capabilities make modern agentic AI possible?”
Something like this:
(3b Advanced inference / trained TF-UFA capabilities (CRITICAL for AGENTIC AI))
-->

#### **(1) Structured machine-language outputs (CRITICAL)**
**GPT:** The TF can generate outputs in highly specific formats:
•	JSON 
•	XML 
•	YAML 
•	API payloads 
•	schemas 
•	ontologies 
This allows Python agents to reliably parse and execute actions. **ME:** Output tokens can have very specific formats ("machine language"). 
The prompt can define the fomrat of the outputs. 
THIS IS CRITICAL for creating responses that the python lang agents use to run analysis.

*Prompt defining format of outputs*<br>
 <img src="/assets/3_build_analysis_messages.png" alt="drones" width="60%"> 


#### **(2) Task decomposition / planning**
**GPT:** The TF is trained to:
•	break large tasks into substeps 
•	generate plans 
•	sequence actions 
•	maintain goal-oriented context 
This is critical for agent workflows and orchestration.

#### **(3) Semantic inference**
**GPT:** The TF can infer:
•	meaning 
•	intent 
•	relationships 
•	context 
•	ontology mappings 
•	hidden connections 
without explicit hardcoded logic.

#### **(4) Natural-language → machine-language translation**
**GPT:** The TF converts vague human requests into:
•	structured actions 
•	API calls 
•	database queries 
•	filters 
•	workflow steps 
This is one of the core capabilities behind agentic AI.

#### **(5) Feature detection / trained abstractions**
**GPT:** The TF FFN/UFA layers contain trained detectors/features for:
•	concepts 
•	entities 
•	relationships 
•	patterns 
•	semantic structures 
Many researchers now believe much of the model’s “knowledge” resides in FFN layers. 

#### **(6) Contextual reasoning**
**GPT:** Attention allows tokens to dynamically reference:
•	earlier instructions 
•	schemas 
•	constraints 
•	conversation history 
•	related entities 
This enables contextual workflows instead of rigid scripting.

#### **(7) Generalization / approximation**
**GPT:** The TF-UFA can approximate:
•	patterns 
•	workflows 
•	mappings 
•	relationships 
•	inference rules 
even when exact cases were never explicitly programmed.

#### **(8) Ontology alignment**
**GPT:** The TF can map:
•	synonyms 
•	alternate phrasings 
•	related concepts 
•	human language variations 
into standardized machine-oriented ontology structures.
Example:
"truck delayed"
"shipment late"
"logistics issue"
may all map into:
{ "event_type": "delivery_delay" }

#### **(9) Error tolerance**
**GPT:** TF-UFA systems tolerate:
•	spelling mistakes 
•	grammar issues 
•	incomplete requests 
•	ambiguous language 
•	noisy input 
This is critical for real-world human interaction.

#### **(10) Explanation generation**
**GPT:** The TF can explain:
•	plans 
•	outputs 
•	anomalies 
•	decisions 
•	recommendations 
in human language.
This is critical for:
•	trust 
•	usability 
•	enterprise workflows 
•	analyst systems 
•	PM-facing systems 



<br>


<br>


# **5 Agent+AI demos**

Simple demos are the best way to understand the basics of agentic AI apps. For details see page **[Agentic demos with AI](/agentic-demos-with-ai/)**.

<!-- on my GIT (docx #603 chapters [2.x] pal_vx, [3.x] pal_core_0x)  (LINK TO OTHER PAGE.... put details there) simple demos are the best way to understand the core of agentic ai. Below lists my demos in my github, described in detailed in docx #603 on the gdrive. i hope to improve my description of these demos on this page soon. -->

<img src="/assets/4_6_2x.png" alt="drones" width="45%"> 

<br>







<!-- ####################################################################
### 4.4 Agentic AI = human language <-> machine language interface
This section describes 3 ways to do this. The first 3.1 is what we want. 
TOC
- 1 (BINGO) (machine conversion MMLI 4<>5) Human lang is the interface medium 
- 2 (FAIL) (machine conversion EM I/F) brain implants did not work (too complex) 
- 3 (BINGO (but not what we want)) (human conversion I/F) Python (MML Converter/compiler)  

 
#### =1 (BINGO) (machine conversion) Human lang as the interface medium 

this is the solution that agentic ai uses. 
•	1 human lang prompt input to the agent. 
•	2 agent sends that prompt along with its own extra prompt material to the LLM.
•	3 LLM sends back response to agent. This response is what I refer to as "machine language". what this means not assembly code, but text that matches a format that the deterministic agent can successfully process.

<img src="/assets/4_11_machine_conversion.png" alt="drones" width="65%"> 

 
in the TF human lang tokens are converted by TF to hidden states. these are analyzed to determine the next token (repeated for each new token).
 
<img src="/assets/4_12_tf_hidden_states.png" alt="drones" width="30%"> 

 
#### =2 (FAIL) (machine conversion EM I/F) brain implants did not work (too complex) 

This was in interesting attempt in the past. brain EM fields are converted by implanted electronic device to digital data. This did not work. The human brain is vastly more complex than all of our electronic tech.  Currently there is success in using nerve signals to help amputees control artifical limbs, but thats about the extent of the tech currently.

<br>
 
#### =3 (BINGO (but not what we want)) (human conversion I/F) Python compiler 

human creates/enters machine-ready commands in the compiler, IDE, UI. this is not what we are looking for, but its instructive to understand how it solves the same probllem in a different way.

Python, the language for humans converted to machine code . When high level languages first appeared, the assembly/machine language programmers hated them (I started in assembler). But machine level code was too big, too complex.  Python gives a high level representation. like AI now, they make coding vastly more productive. Its a trade off though. 
- The Python programmer does not know the details of what the CPU is doing. 
- needs imports, libraries, detailed knowledge of commands, cryptic errors
- runs only on an OS (assembler can be bare metal)

Writing in Python is possible because 
- linters, IDEs, compilers, etc ensure that humans get the grammar right
- runtime error messages, graceful error handling

any "chats" must go thru a complicated UI . that is carefully programmed to filter input. drop lists, buttons, etc. 

agentic usage is thru a carefully scripted API . Python programs can interact with external programs. but those programs on both sides must closely observe the API specs. 

<br> -->





<!-- 




<br><br><br><br><br><br><br><br><br><br><br>

# OLD page ===============================

<br>

See the **[Wiki page](https://github.com/terrytaylorbonn/auxdrone/wiki/Agentic-AI)** for more info.

The focus in this section will be on  
- creating AI agents

I have been doing simple demos and analyzing all the code (up to 800 code lines of Python). The real way to do this is probably with a Cursor style system.

<img src="/assets/ai_project_diagram_4.png" alt="drones" width="40%"> 

<br>

#### 1) Demos are the best way to learn agentic AI

A typical definition of agentic AI would be "systems that plan, reason, and act autonomously to achieve goals." The only way you can decipher such a statement is if you have hands-on experience. The wiki page [Agentic AI demos](https://github.com/terrytaylorbonn/auxdrone/wiki/4%E2%80%902-Agentic-AI-demos) provides a very structured set of detailed demos of core concepts. 

<br>

#### 2) All LLMs have an internal agent

The LLM has 2 main components:

1. A transformer (TF) that performs GPU-based computing to analyze human language input (a prompt) to determine what the output (response) should be. The TF is simply input/output (no loop).
2. An internal agent ("iAgent", a deterministic CPU-based program) that interfaces between the TF and the outside world. This internal agent is the central control loop that manages complex tasks such as conversation history, structure, user interface, etc.

<br>

#### 3) "Agentic AI" refers to an external (to the LLM) agent

This program is the central loop of the entire application in which the LLM plays a supportive ("helpful assistant") role.

![Agentic AI ecosystem](/assets/ecosystem.png)

The (external) agent performs the following functions (sometimes with the assistance of the LLM): 
- Data integration and analytics
- Tools (function calling, APIs, external integrations)
- Workflows (multi-step agent pipelines, orchestration)
- Planning systems (task decomposition, ReAct, chain-of-thought)"

<br>

#### 4) My focus on Palantir agentic AI

Palantir is a well known company with a very successful line of products. Palantir was founded in 2003 with early backing from the CIA — when there was no AI as we understand it today. Palantir was founded (with government backing) to prevent events like 9/11 by connecting data points to detect hidden threats. There were warning signs for 9/11 (foreign nationals wanting to learn to fly airliners on simulators). But collecting and analyzing such signals back then required a lot of manpower. Palantir's tools are nowadays being used in many other business segments (other than defense). 

Only relatively recently has AI played a major (useful assistant) role in Palatir's products. Palantir's AIP (Artificial Intelligence Platform) "enables organizations to securely deploy Large Language Models (LLMs) and artificial intelligence within their private networks, connecting generative AI directly to operational data (the Ontology) and workflows. It allows users to automate tasks, generate insights, and take action securely across various sectors."

AIP probably offers a set of functionality similar to the following:
- **Standardization of "messy" inputs**. AI creates outputs with specific structures and data types. 
- **Planning.** AI breaks up a "messy" plan into a set of standard subtasks that can be verified.
- **Rule injection.** AI can add "rule" keywords to the list of keywords used by the deterministic agentic loop to modify the execution logic.

*Diagram from Substack post [#75 The Real Job of AI in Enterprise Apps](https://ziptieai.substack.com/p/75-the-real-job-of-ai-in-enterprise) shows how AI is only used to generate a plan ("08b AI")*

<img src="/assets/aiplan.png" alt="AI planning" width="85%">

<br>

#### 5) Lessons learned from the demos

Very "basic" demos of such functionality are listed on the wiki page [Agentic AI demos](https://github.com/terrytaylorbonn/auxdrone/wiki/4%E2%80%902-Agentic-AI-demos). Complete documentation with all the steps is on the Gdrive. The  goal of these very simple demos is to show basic core concepts that apply to AI systems of any size. For example:
- Palantir will not become [SkyNet](https://en.wikipedia.org/wiki/Skynet_(Terminator)). The central agent control loop is not AI-controlled and presses no buttons (humans are required).
- SW programming jobs will not disappear. Such systems require very capable product experts preferably with extensive SW experience. Programming is just becoming higher level. 



A few things you will notice if you do thOne of my major goals in studying AI has been to refute the hype (that I recognized early). The AI titans and gurus were feeding the public nonsense about how their inventions could think, have consciousness, have feelings, and even surpass human intelligence.

This is utter nonsense. All of an AI system (CPU and GPU based parts) are on the lowest level clocked binary circuits. This has absolutely nothing to do with the neurons in the human brain. AI tools cannot see, hear, sense touch, smell, have feelings, consciousness, or think. In short, they have no intelligence. -->

<br>

26.0514 (rewrote 26.0509; v1 26.0428)

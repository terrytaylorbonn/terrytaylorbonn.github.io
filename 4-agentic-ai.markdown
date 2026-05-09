---
layout: page
title: "(4) Agentic AI"
permalink: /agentic-ai/
---

<br>

<!-- **26.0509 REWRITING THIS PAGE ... FINISH BY 26.05010. THIS IS THE CORE PAGE OF THIS WEBSITE. This page will explain how agentic AI really works (my take).** (My rewrite working notes: in docx #606 on gdrive (link in footer) search for ""(4) Agentic AI" rewrite"). -->


**This page is WIP (25.0509)**. The thoughts (and the diagrams) on this page are mostly my own (hased out with the help of AI LLMs). 

**TOC** 
- **1 Why learn agentic AI? (jobs)**. The job growth will be phenomenal. Agentic AI is incredibly useful in all business segments.
- **2 Agent concepts**. What is an agent anyway?
- **3 Agent demos (no AI)**. From my github. 
- **4 Agent+AI concepts**. How does AI change things? Dramatically.
- **5 Agent+AI demos**. From my github.

<br>

# **1 Why learn agentic AI? (jobs)**

My interest toward agentic AI grew strongly during the Iran war, when I read about how Palantir's AI systems had radically changed the nature of warfare. This was an application of AI that worked. No hype, no lies. No AI gurus playing us for fools. 

My interest only grew stronger when the hypesters started claiming that Palantir might become Skynet.  But most of all when I saw how agentic AI was going to be the growth market of the future. What revolutionized the battlefield will also revolutionize business. 

*The future agentic AI job market*<br>
<img src="/assets/4_1_goldman.png" alt="drones" width="75%"> 


<br>

# **2 Agent concepts**

What the agent and the AI do.

<br>

### 2.1 The agentic mission 

**Palantir agentic systems (no AI) started around 2003 in response to the 9/11 attacks.** The US government wanted to make sure such an event did not happen again. 

<img src="/assets/4_2_wtc.png" alt="drones" width="35%"> 

 

The mission goals were quite clear: Track all kinds of information,and detect any strange new activity *(such as a bunch of Middle Eastern nationals wanting all of a sudden to learn how to flight airliners on flight simulators; there were warnings about this, but the central government structures were able to ingest those warnings; they did not have enough (motivated) manpower)*. Palantir was to be the (automated) system for this critical mission. **A system that watches the world (like a sorcerer looking into his crystal ball) 24/7, 365 days a year.**

A palantír is one of several indestructible crystal balls from the novel The Lord of the Rings used to see events in other parts of the world. (https://en.wikipedia.org/wiki/Palant%C3%ADr)<br>
<img src="/assets/4_3_crystal_ball.png" alt="drones" width="20%"> 

 

The deterministic program (like Python) agent as a the sorcerers ball <br>
<img src="/assets/4_4_agent_ball.png" alt="drones" width="30%"> 

   <br> 
 
### 2.2 Ontology
Palantir ontology was a big break through. something between free text and a rigid database. you simple restrict the language so that the deterministic loop can process. a lot of effort. but you cant ingest "messy" human language (later with AI you could; and AI puts out basically clean ontology, one of the core magic tricks of AI).

https://en.wikipedia.org/wiki/Ontology_%28information_science%29 <br>
<img src="/assets/4_5_onto.png" alt="drones" width="45%"> 

 <br>
 
# **3 Agent demos (no AI) (SUBPAGE)**
(no AI) on my GIT 
(docx #603 chapters [2.x] pal_vx, [3.x] pal_core_0x)


(LINK TO OTHER PAGE.... put details there) 

simple demos are the best way to understand the core of agentic ai. Below lists my demos in my github, described in detailed in docx #603 on the gdrive. i hope to improve my description of these demos on this page soon. 

<img src="/assets/4_5_3x.png" alt="drones" width="40%"> 

<br>

# **4 Agent+AI concepts**

<br>

### 4.1 Why does agentic need AI?

The agent is the main deterministic control loop of the agentic app. the agent is the center of the universe. 

AI was an add-on to the agents. A helpful assistant. A suped-up search engine with language capabilities. Whose outputs you can never trust. It can use AI ("LLM" in diagram below) as needed as a helpful assistant (usually to interpret/sanitize messy human language text, create human language explanations, planning (breakin up complex tasks into granular task that the agent is programmed to handle, etc etc).

this human language ability, planning ability, etc makes an agentic app vastly more flexible and capable. at the cost of unpredictabilty. but for many apps, that is an excellent tradeoff. 

The LLM as a helpful assitant for the agent<br>
<img src="/assets/4_7_help_assist_LLM.png" alt="drones" width="40%"> 


 <br>
 
### 4.2 What does AI do?


(below) 
- humanLanguage source (blue square; input from UI, db, apis, etc)
- agent sends human language with extra human lang commands to LLM
- LLM (red square) is the AI "magic", turning the into "machine" language (text, but text that conforms to the expectations of the agent). 
- Agent then can process this "machine language"<br>

<img src="/assets/4_8_what_ai_does.png" alt="drones" width="65%"> 


<br>

 
### 4.3 what are the limitations / tradeoffs?

<br>

#### =3 avoid AI hype rabbitholes

It took a decade for AI-assist to be added to Palantir systems. And then came the hype. AI had to be the center of attention, the center of the universe. It wasn't "AI-istic agents", but rather "agentic AI". Something that might one day take over the world (Skynet style https://en.wikipedia.org/wiki/Skynet_(Terminator) ).  

That hype brought in the big bucks. All kinds of free publicity. Lots of companies spending big bucks on something that doesn't work (for types of applications it was never designed for). Like FSD (full self driving) that could not drive itself (safely, even today).


An example of the LLM as the core of the Agent (LLM-centric universe): "What Is Agentic AI? Agentic AI is an innovative advancement in artificial intelligence (AI), characterized by its ability to independently make decisions and implement goal-oriented actions on behalf of users or systems." https://www.cadence.com/en_US/home/explore/agentic-ai.html  <br>
<img src="/assets/4_9_cadence.png" alt="drones" width="35%"> 

<br>

#### =1 LLMs have no intelligence

4.3 Knowing what to expect from a PC requires knowing its fundamentals.
it helps to compare this to the PC. all that high level software components are built on binary logic. its really incredible that binary logic can do this. 

TFs are built on matrix math. Thats it. LLMs = TF + iAgent = simulated intelligence. its a UFA .. universal function approximator. best guess based on statistics.  and its quite complex.... depends on training set.. so very difficult to ensure all is correct. 

in the TF human lang tokens are converted by TF to hidden states (12K FP numbers per token for GPT-3). TF performs a massive amount of computation on the hidden states for all tokens (up to millions of billions or more computations) to compute the the best new token. This is the the core of so-called "intelligence" in LLMs (in reality there is no intelligence; thats precisely why you need the agent in the first place).

<br>

#### =2 balance tradeoffs 

because then you appreciate how fragile the stability and accuracy of external agent and LLM interactiono. "hallucinations" = failed UFA algorithm. the algorithms are have "blind" spots. 

<br>

### 4.4 workflow diagram(WIP)

Workflow details:
- **#1 UI/DB/API** (human language sources and destinations) **interface with #2 Agent** (the main loop).
- **#2 Agent adds extra info/requirements (JSON) to LLM input**. This instructes the LLM about what type of data and format to return.
- **#3 Model (LLM) interface layer**. Every LLM may require slightly different prompts and also output slightly different outputs. Palantir uses  MIL to allow quick easy "hot" switching of models. 
- **#4 Internal agent controls #5 TF**. The agent knows exactly how to talk/listen to TF to create the LLM response.
- **#5 TF creates output text** based on input text. Thats it. This is all the LLM TF does, and yet somehow the LLM seems almost intelligent. Unbelieve (just like how everything your PC does is based 100% on simple binary switching logic).
- **#4 LLM iAgent sends response to #2 (external) agent.** 
- **#2 Agent executes response.**

<img src="/assets/4_10_workflow.png" alt="drones" width="70%"> 

<br>

### 4.5 agentic AI builds a humanLang to machineLang interface
This section describes 3 ways to do this. The first 3.1 is what we want. 
TOC
•	=1 (BINGO) (machine conversion MMLI 4<>5) Human lang is the interface medium 
•	=2 (FAIL) (machine conversion EM I/F) brain implants did not work (too complex) 
•	=3 (BINGO (but not what we want)) (human conversion I/F) Python (MML Converter/compiler)  

 
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

<br>


# **5 Agent+AI demos (SUBPAGE)**



on my GIT 
(docx #603 chapters [2.x] pal_vx, [3.x] pal_core_0x)

(LINK TO OTHER PAGE.... put details there)

simple demos are the best way to understand the core of agentic ai. Below lists my demos in my github, described in detailed in docx #603 on the gdrive. i hope to improve my description of these demos on this page soon. 

<img src="/assets/4_6_2x.png" alt="drones" width="45%"> 

<br>

### 5.3 LIST OF 8
LLM (iAgent/TF) combo thinking / planning tricks (core functionality that makes agentic AI possible)

This can do many things such as
-	standardize messy inputs (messy vocab and meet JSON requirements)
-	planning into small steps
-	rule injection

it does this ... but without intelligence (all made possible by the interaction of the deterministic iAGent that was programmed specifically for the TF; the 2 together can perform these functions.

<img src="/assets/4_12_tf_hidden_states.png" alt="drones" width="30%"> 

[3.6] (WIP) pal_core_06: simplest demo of all core LLM roles 26.0416
#585 could you create a minimalistic demo that demos the key ways an LLM capabilities can be used 
in the types of system we have been creating? 
for example, 
(1) input human language commands, 
(2) insert new rules, etc? 
for now, could you just list those key ways?

Yes. That would be an excellent meta-demo:
one small system showing the main ways an LLM adds value inside structured applications.

For now, here is the concise list of key LLM capabilities relevant to the systems you’ve been building.

Core LLM Roles in Your Demo Systems<br>
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


<!-- 
A few things you will notice if you do thOne of my major goals in studying AI has been to refute the hype (that I recognized early). The AI titans and gurus were feeding the public nonsense about how their inventions could think, have consciousness, have feelings, and even surpass human intelligence.

This is utter nonsense. All of an AI system (CPU and GPU based parts) are on the lowest level clocked binary circuits. This has absolutely nothing to do with the neurons in the human brain. AI tools cannot see, hear, sense touch, smell, have feelings, consciousness, or think. In short, they have no intelligence. -->

<br>

26.0509 (v1 26.0428)

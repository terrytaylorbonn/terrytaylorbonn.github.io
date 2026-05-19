---
layout: page
title: "3.2 (4c) AI'ic agents"
permalink: /4c-agentic-ai/
published: false
---



<br> 

**TOC** 
- **It's "AI'ic agents", not "agentic AI**.  
- **4 AI'ic agent concepts**. AI is only a (extremely) helpful assistant.
- **5 AI'ic agent demos**. Lab notes on my Gdrive. Code on my Github.

Notes:
- [4a chat about iAgent and eAgent](/4a-chat-about-iAgent-and-eAgent/) 26.0514


<br>

# **1 Concepts**

<br>

**Just like iAgent and TF work together, so must extAgent and LLM.**



<br>

### **1.1 VERY IMPORTANT**

<br>

VERY IMPORTANT insight for your site
Your entire architecture is basically:
#### **3.1 deterministic agent systems existed before LLMs**
BUT were expensive and rigid
#### **3.2 TF/UFA semantic capabilities made those systems**
vastly more practical and flexible
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

### **1.2 agentic AI**

 
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

*For background on VL, storylines, etc discussed below, see [The gist of LLMs](/2.4.1-llm-gist/).*

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



<br>

# **2 Diagrams**

<br>

### **2.1 Ecosystem**

*The LLM as a helpful assitant for the agent*<br>
<img src="/assets/4_7_help_assist_LLM.png" alt="drones" width="45%"> 

<br>

### **2.2 agent <> LLM interface**

*Details of the agent <> LLM interface*<br>
<img src="/assets/GPT_agent.png" alt="desc" width="55%"> 

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
https://ziptieai.com/2.4.2-ufas/ talks about how transformer universal function approximator (UFAs) are critical for agentic ai. i think you once mentioned the 8 main functions of the agent (i think that was without ai). what would the list be like for how AI greatly help agents work properly? below is title and toc of the section on that page in the wiki about TF UFAs .................... 
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


This page is WIP (v1 26.0509). I need to go back through these demos and document.

Simple demos are the best way to understand the core of agentic+AI apps. For details see the lab notes doc **#603\_PAL\_.docx** (PAL = Palantir) on my **[Gdrive](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**.  

<img src="/assets/4_6_2x.png" alt="drones" width="70%"> 

Also 

<img src="/assets/4_5_3x_bbb.png" alt="drones" width="70%"> 

<br>


26.0515
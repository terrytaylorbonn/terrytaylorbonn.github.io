---
layout: page
title: 3c Enterprise
permalink: /pal/
---

<br>

The enterprise platform controls almost everything. For now this section focuses solely on the Palantir (PAL) platform.

<br>

**TOC** 
- **3c.1 PAL app concepts** (my own take)
- **3c.2 PAL AI dev assistants** (Understanding how to use PAL's AI tools is critical for learning to use PAL). 
- **3c.3 The gist of Palantir "haystack needle" (HN) apps (demo details)** (demos that show this)
- **3c.4 All demos (chronological order; detailed results from my tests)** (right now this is just a chronological list of what I did, but I might reorganize this in the future)

<br>

### **3c.1 PAL app concepts (WIP)**

<!-- (/3c.ccc_pal_concepts/) -->

<br>

#### **3c.1.1 The PAL framework simplifies tasks**

**Real world apps change quickly**. PAL apps are used to analyze complex environments that are constantly changing. You need a framework to allow focus on the parts that matter. **[3.1 code-first agents](/3_agents/)** was my attempt to do show how to create app agents (AI, non-AI) without a framework (I did not really understand how PAL worked then). Its a lot of work. Complexity. Its difficult to focus on the core task. **PAL is a framework that manages the complexity of creating AI apps**.  

<img src="/assets/pal_9_13.png" alt="drones" width="85%" style="border: 1px solid #999;">

<br>

#### **3c.1.2 PAL (no end user app AI)**

This was the original PAL architecture (25 years ago, shortly after 9/11). This is what demos D1-D7 (below on this page) are all about. Detecting situations without AI. I did some demos to test this kind of functionality without a framework on page **[3.3 Agent PAL core demos](/3.1-agentic/)** (again, my knowledge of PAL back then was limited to what I read).

<img src="/assets/pal_9_14.png" alt="drones" width="85%" style="border: 1px solid #999;">

<br>

#### **3c.1.3 PAL + AI (in end user app)**

on page **[3.3 Agent PAL core demos](/3.1-agentic/)** were also demos with AI.

<img src="/assets/pal_9_15.png" alt="drones" width="85%" style="border: 1px solid #999;">

There are 2 problems when using AI for detection 
- (1) **Data sources are often messy**. You need something like PAL pipelines and ontology to clean things up.
- (2) **Thats important because AI is just pattern recognition**. On the (rather short) page **[Hack](/0-demo/)** I layout the gist of what an AI LLM transformer (TF) does (which shows the core of AI really is). Most importantly on that page I show that **LLM TF's are simply pattern classification algorithms**. The classification of input tokens determines the output tokens (TF's understand nothing about language, they only generate a classification number for the input numbers). Recent GPU performance breakthroughs mean the patterns can scale to massive sizes, increasing the sheer number of patterns that can be reliably classified. **That is not intelligence, but pattern matching. An amazing hack. And it works.. mostly. But it needs guardrails.** 

That's where PAL comes in. **PAL minimizes the limitations of the AI hack while maximizing its effectiveness**. 

*The LLM transformer is a hack, but Palantir provides the guard rails that maximize its effectiveness* <br><img src="/assets/hack-08.png" alt="drones" width="35%" style="border: 1px solid #999;"> 

<br>

<!-- This is a long term goal (just like creating core concepts for AI has been). <br><br>*(placeholder pic; eventually I will create master pic that sums up core concepts)* <br><img src="/assets/pal-demo-01.png" alt="drones" width="65%" style="border: 1px solid #999;">
<br> -->

### **3c.2 PAL AI dev assistants**

<!-- /3c.bbb_pal_strategy_fde/ 
**[3c.2 PAL AI dev assistants (WIP)](/3c.bbb_pal_strategy_fde/) shows how to maximize AI usage when using PAL (by using AIP/FDE)**. 
-->

**Real world apps change quickly**. This ZiptieAI site is constantly evolving. I can manage this task by myself thanks to the AI tools that vastly simplify website management. Its the same when creating apps with PAL tools. AI inside of PAL (and other apps) will vastly improve in the few years, and this will revolutionize end user programming (**PAL's built-in AI has made using PAL vastly easier already**, but there is still much room for improvement). This is just another example of how **AI is not a tech bubble (its only getting started)**.

*No need for traditional docs (that you have to sift through to find what you need); PAL's built in AI answers your questions with details instructions* <br>
<img src="/assets/pal_9_10.png" alt="drones" width="100%" style="border: 1px solid #999;">

<br>

### **[3c.3 The gist of Palantir "haystack needle" (HN) apps (demo details)](/3c.xxx_pal_gist/)**

<!-- (based on demo D8 listed in section "3 Demos" later on this page) -->

What has interested me the most about Palantir for over a year now are the **"haystack needle" (HN) algorithms**. This was the original reason for the founding of PAL. 9/11 occured because the US government failed to detect obvious warning signs in a sea of data. PAL's job was to make sure that that did not happen again by creating a system that could sift through vast amounts of data (about, for example, a sudden surge in foreigners studying to fly large airliners) to flag potential threats. To find the needle in the haystack.

But how exactly did they implement the HN algorithms? That's of practical interest currently because 
- (1) those **HN techniques are being used in all business segments** (not just military and intelligence) and 
- (2) **you can learn the details hands-on yourself for free with no assistance**by getting a PAL trial license (I have only a trial license and I am working alone). 

The goal of this page is to explain (via demos) the gist of a portion of the Palantir (PAL) toolset (there are not many competitors to PAL right now, but there will be in the near future, and they will follow a lot of the PAL methodologies). How to use that toolset to create HN apps.

*The gist of Palantir: A crystal ball (called a "palantir" ("seeing stone") in Lord of the Rings) that can find a haystack needle (HN)* <br><img src="/assets/pal_9_06.png" alt="drones" width="25%" style="border: 1px solid #999;">

<br>

### **3c.4 All demos (chronological order; detailed results from my tests)**

**[PAL demo strategy](/3c.aaa_pal_strategy_demos/)** is 
- Document in docx (MS.Word) files. These are detailed and can be realistically maintained (the official demos seem to not be updated often; videos are nice, but they get outdated quickly and are impossible to update). **My personal opinion (and the future direction of my own demos) is that demo documentation should rely more on describing how to work with AI to do hands-on step-by-step demos** (not describing the actual details).<br><img src="/assets/pal_9_11.png" alt="drones" width="44%" style="border: 1px solid #999;"><br><br> 
- Use AI (internal PAL AIP/FDE) as much as possible (avoid docs and tutorials if possible; I first started to do demos based on AIP/FDE chats in demo D8).<br><img src="/assets/pal_9_12.png" alt="drones" width="64%" style="border: 1px solid #999;">

Following is the list of demos in chronological order. I added numbering, conceptual diagrams, and a few error updates to the original demos. I will probably come up with my own set of demos. 

- **[D1: Palantir Foundry "speedrun" (quick start) (26.0705)](/3c.1_pal_foundry/)**. 
  - Demo complete... still need to write the webpage.
  - #610_pal_1_foundry_v02_26.0704_SS.docx  
  - https://learn.palantir.com/speedrun-your-first-e2e-workflow/1944887 
- **[D2: Palantir AIP "speedrun" (quick start) (26.0706)](/3c.2_pal_aip/)**. 
  - Tis is just a rough summary for now...
  - 611vvv_pal_2_aip_qs_v07_26.0713_SS (2).docx
  - https://learn.palantir.com/speedrun-your-e2e-aip-workflow
- **[D3: Palantir agentic AI "speedrun" (quick start) (26.0713)](/3c.3_pal_agentic_ai/)**.
  - #614_pal_3_agentic_ai_qs_v03_26.0715_ss.docx 
  - https://learn.palantir.com/speedrun-your-first-agentic-aip-workflow
- **[D4: Palantir ontology function "speedrun" (quick start) (26.0717)](/3c.4_pal_ontology_function/)**. 
  - At the end of this page is *good demo of how FDE/GPT5.5 fixed a problem with the demo*.
  - #615_pal_4_onto_function_qs_v02_26.0717_ss (2).docx 
  - https://learn.palantir.com/speedrun-your-first-ontology-function/2131538
- **[D5: Speedrun: Mining Your First Business Process (26.0718)](/3c.5_pal_biz_process_mining/)**. 
  - #616_pal_5_biz_process_mining_qs_v02_26.0718_ss (1).docx
  - https://learn.palantir.com/speedrun-mining-your-first-business-process
- **[D6: Deep Dive: Building Your First Pipeline (26.0719)](/3c.6_pal_6_first_app/)**.
  - **Some of this failed**. FDE/GPT/OPUS could not fix. 
  - outdated (2+ years) demo? MAKE THE DEMOS SIMPLER AND KEEP THEM UPDATED.
  - #617_pal_6_first_app_v01_26.0719_ss.docx. 
  - https://learn.palantir.com/deep-dive-building-your-first-application 
- **[D7: Deep Dive: Building Your First Pipeline (26.0720)](/3c.7_pal_7_first_pipeline/)**.
  - #618_pal_7_first_pipeline_v01_26.0719_ss.docx
  - https://learn.palantir.com/deep-dive-building-your-first-pipeline
- **[D8: Deep Dive: Model integration (26.0721)](/3c.8_pal_8_model_integration/)**.
  - #619_.docx

<br>

### **Notes**
- *[PAL general notes](/3c.0_pal_notes/)*
- *[Palantir CEO火力全开，场面控制不住了！](https://www.youtube.com/watch?v=feUFT1Q-oBA)*
- *[zerohedge.com/ai/something-has-gone-completely-wrong-palantirs-alex-karp-goes-ballistic-openai-anthropic](https://www.zerohedge.com/ai/something-has-gone-completely-wrong-palantirs-alex-karp-goes-ballistic-openai-anthropic)*
- *https://www.youtube.com/watch?v=lSDC6-BdVus?t=341 HBM, diagram of NN, interconnecting multiple GPUs*

<br>

26.0723 (v1 26.0702)x

<!--
Palantir
Microsoft Fabric
Vertex AI
Databricks
Snowflake
Now you're inside a governed ecosystem.
Security.
Permissions.
Lineage.
Governance.
Enterprise data.
Job value: ★★★★★
Highest salaries.
Fewest jobs.
Hardest to enter.
-->

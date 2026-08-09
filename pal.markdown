---
layout: page
title: 3c Enterprise
permalink: /pal/
---

<br>

Enterprise AI dev platforms do the heavy lifting of creating an enterprise level AI app. 

**My focus (for now) is on Palantir (Foundry)** because 
- PAL is a market leader.
- PAL offers a generous free trial account for Foundry.
- The built-in AI help (AIP/FDE) makes it possible to complete the demos.

This section provides what you need to master the basics of Palantir Foundry ASAP. 


<!-- 
 **Reorganized 26.0802**.
- A very logically structured set of the simplest step-by-step demos (with critical details). 
- Gradually more complex demos (future)
- Core concepts (future) -->

<br>

**TOC**:
- **1 Concepts** (my original take on the gist of PAL).
- **1b My approach to learning Palantir Foundry**
- **2 Getting started hands-on**
- **3 Advanced hands-on (future)**


<br>

<!-- ## **[0 My approach to learning Palantir Foundry](/pal_approach/)** 26.0808 -->

## **[1 Concepts](/pal_concepts/)** 26.0808

*(click on link above for details)*


- **1.1 The gist**
- **1.2 Basic workflow**


<br>

#### **1.1 The gist**

- Palantir Foundry makes the enterprise visible and governable.
- Data from many systems is transformed into a common operational model that can be analyzed, queried, monitored, and updated.
- LLMs play the role of helpful assistants, but their very presence makes parts of the system probabilistic. As a result, AI actions must be sandboxed, verified, approved, and logged.

<!-- 
I am still working on **my own take on the core conceptual gist of Palantir-SW**, but the gist is 
- Palantir makes the enterprise visible and governable.
- LLMs only play the role of a helpful assistants, but their very presence makes parts of that visibility probabilistic, so they must be sandboxed, verified, and logged. -->

*The trusted wizard (left) using a crystal ball ("palantir" or "seeing stone" in The Lord of the Rings) and (right) modern AI running on digital hardware. Both promise enhanced visibility and insight, although one belongs to fantasy and the other to engineering.* <br><img src="/assets/pal_9_06.png" alt="drones" width="25%" style="border: 1px solid #999;"> <img src="/assets/777_02.png" alt="drones" width="30%" style="border: 1px solid #999;"><br>

<br>

#### **1.2 Basic workflow**

<!-- For the demos I wanted a more mechanistic conceptual overview (I am more interested in the mechanics of the PAL tools used than the business cases). At first I wanted something like the simple Foundry workflow diagram below with text to summarize what parts an example/demo covered. -->


The following diagram shows the basic PAL workflow.

- **1a Data source**. Raw data from enterprise systems. For example: CSV files, Databases, ERP systems, CRM systems, Sensors, External APIs. 
- **1b Pipeline**. Transforms raw data into clean, structured, and consistent datasets. For example: cleaning, joining, filtering, aggregating, validation.
- **3a Ontology read**. Applications and users read enterprise data through the ontology. The ontology provides a common operational model of the enterprise.
- **3b Ontology writeback**. Applications, workflows, and users update enterprise systems through the ontology. For example: change status, create ticket, approve request, update record.
- **4 Analysis**. Code, queries, dashboards, rules, AI, and other logic analyze the ontology data. Purpose: 
  - discover information
  - detect problems
  - support decisions
- **5 UI / App**. User-facing applications. For example: dashboards, workflows, forms, operational applications, AI assistants.
- **6 Security / Governance**. Controls who can see data, modify data, run workflows, and use AI. For example: permissions, auditing, approvals, version control, lineage, logging, AI. AI can appear in many layers:
  - pipeline transforms
  - model integration
  - ontology functions
  - analysis
  - UI assistants

*The ontology is the operational heart of Foundry. Most applications, analysis, workflows, and AI interact with enterprise data through the ontology rather than directly through the raw datasets*<br><img src="/assets/777_07.png" alt="drones" width="74%" >


The three crystal balls represent three layers of governance. Foundry controls 
- how data enters the system (#1), 
- how applications and AI interact with operational data (#2), and 
- how the entire platform is secured, audited, and managed (#3).

**Crystal ball #1 — Data governance**. Controls how raw enterprise data becomes trusted operational data. 
- Examples: ingestion, transformation, validation, lineage.
- This is the boundary between:
  - Data Source
  - Pipeline
  - Ontology

**Crystal ball #2 — Operational governance**. Controls how applications, users, workflows, and AI interact with the enterprise.
- Examples: ontology permissions, workflow permissions, write-back controls, approval processes.
- This is the boundary around:
  - Ontology
  - Analysis
  - UI
  - Writeback

**Crystal ball #3 — Global governance**. Controls the entire platform.
- Examples: security, auditing, version control, branching, deployment, compliance.
- This is the layer that sits above everything else.


<br>

## **1b My approach to learning Palantir Foundry** 26.0808

When I first started with Foundry I was a bit overwhelmed (this is a very powerful system). I first checked out
- **[palantir.com/docs/foundry](https://www.palantir.com/docs/foundry)**. Has a lot of great content. But its probably not where you want to initially start. 
- **Several Youtube sites**. The sites I viewed were quite good, but not really suited for an absolute beginner. Documents are the best for absolute beginners (and they tend to be more up-to-date and can serve as the template for your own docs).

I wanted to get hands-on experience from the start. So I checked out several official Palantir sources of demos. There were a lot of demos.
- **[build.palantir.com](https://build.palantir.com)** has links to examples/demos organized by type: AI Starter Pack, Document Suite, Reference Implementation, etc.<br><img src="/assets/777_23.png" alt="drones" width="32%" style="border: 1px solid #999;"><br> 
- **[learn.palantir.com](https://learn.palantir.com)** has links to examples/demo organized by role: Data Engineer, App Dev, etc.<br><img src="/assets/777_22.png" alt="drones" width="65%" style="border: 1px solid #999;"><br> 
- **[my-org].palantirfoundry.com/workspace/marketplace** is a Foundry internal app for finding examples/demos organized by 9 "stores".<br><img src="/assets/777_21.png" alt="drones" width="45%" style="border: 1px solid #999;"><br> 

I spent the first month doing the demos I thought looking interesting. PAL docs are organized by different roles and different project types. But I wanted a learning path that led me demo-by-demo through the basics of the entire PAL toolchain. So on 26.0807 I created my own learning plan doc **[#699\_planning\_.docx](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**.<br><img src="/assets/777_24.png" alt="drones" width="51%" style="border: 1px solid #999;"><br>

Its still a work in progress, but **if you are wanting a single-path demo-by-demo intro to Foundry, then this section of ZiptieAI is for you** (after another month or two of testing and rewriting the docx's).

<br>

## **2 Getting started hands-on** 

**Note: Lab notes** (MS.Word docx files) are available for each example/demo on the **[GDrive](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**.

- **2.1 Palantir free tier sign up**
- **2.2 Hands-on** with examples/demos/deep-dive's/DIY's
- **2.3 Readmefirst**
- **2.4 PAL examples**. These are complicated, but they have an autoinstaller that allows you to start with a (usually) working version that you can modify.
- **2.5 PAL demos**. These are less complicated, but you start from 0, and getting a working demo at the end requires a lot of skill (including debugging).
- **2.6 DIY demos**. Go free style (not "vibe") by teaming up with FDE (AI assistant) to create your own demos.

<br>

#### **2.1 Palantir free tier sign up**
If you cant get a trial version of PAL running, then there's no reason to read further. You will not understand PAL by just reading about it.
  - I dont remember the URL. Just Google it.
  - Unfortunately, I did not record how I signed up, and its not a process I can repeat. But I can tell you this
    - **You must be in a country that PAL supports** (thats only a few countries).
    - **You can NOT use a VPN**.
    - **You must have a passport or some picture ID of good enough quality for facial recognition verification**. My passport is almost 10 years old, but it still worked. My drivers licence pic was of such low quality that I doubt it would have worked. 
    - **You need a camera on your PC to take a pic of yourself. PAL will compare your ID and the pic.**
    - I think you need a **mobile phone number** (and email).
  - It was a fairly long process, but very professionally done (I was impressed) (3c.0a).<br><br><img src="/assets/pal_10_08.png" alt="drones" width="37%" style="border: 1px solid #999;"><br><br>


<br>

#### **2.2 Hands-on with examples/demos/deep-dive's/DIY's**

*PAL has 3 types of hands on learning -- examples, demos (speedruns), and deep dives; DIY (do it yourself) is my own hands-on learning from scratch using FDE(GPT 5.5) as the guide; in this doc I for now use the term "hands-on's" (a tongue twister) to refer to them all (until I think of a better term)*.

- To really understand PAL you need to do hands-on's. 
- Below is typical hands-on diagram. The idea is to show
  - Security functionality. 
    - Crystal balls #1-3 represent the security aspects of Foundry (ensuring every user can only performed authorized actions). 
    - Each ball represents a security area (I am not sure about this, but I am sure security needs to be in the diagram): 
      - (1) Input (starting) data -> pipeline -> ontology.
      - (2) Ontology -> analysis -> UI AND UI -> ontology -> data source. 
      - (3) Global security.   
  - Workflow
    - steps 
    - functionality (text below the diagram)
  - Required example/demos installation/configuration steps
    - Examples (ORANGE = everything is installed for you)
    - Demos/deep-dives (RED = you must configure everything)

<img src="/assets/MAIN_E17.png" alt="drones" width="74%" >

<br>

#### **[2.3 Read me first](/3c.1b_pal_readmefirst/)**

This readme discusses various things to keep in mind as you work your way throught the examples/demos (problems to watch out for, avoid, etc). 

**Example:** 
- The screenshot below is from the ZiptieAI DIY demo **[D9 UI (Workshop)](/3c.xxx_pal_HN_01_non_ai/)** (based on chats with FDE, not an example/demo/deep-dive). <br><img src="/assets/777_05.png" alt="drones" width="100%" style="border: 1px solid #999;"><br> 
- It took me a long time to get the Workshop in that DIY demo working. Even FDE made a mistake during the configuration. Afterwards I created this simple diagram (with uniquely numbered steps and variables; they don't have to be perfect, just something you can trace). If I had had such a diagram for the step-by-step demos I had done earlier, I would have understood better what I had been doing. When you get your first Workshop running, spend extra time tracing through all the connections. Experiment. Do this for other tools.<br> <img src="/assets/777_04.png" alt="drones" width="80%" style="border: 1px solid #999;"> 

<!--
For your first workshop configuration a simple diagram with numbered steps and variables can make it much easier to grasp what you are doing. Because when you start to try setting up your own config, you need that understanding. 
-->


<br>

#### **[2.4 PAL examples](/3c.1b_pal_examples/)** 
*(MAIN DIAGRAM: 621/E10/**OK**, 622/E11/**OK**, 626/E17/**OK**) // (623/E12/FUTURE) // (624/E15/FAIL, 625/E16/INSTALLERROR)*.
  - Install a PAL example.
  - Run the example.
  - Try to rebuild the examples (from top to bottom, from downstream to upstream). The examples are excellent, but are often quite complicated. But you don't have to do everything first step-by-step before you see the the final results. Once you have a working first (reference) example, you can install a second (experimental) example that you modify at your pace. This allows you to (1) appreciate quickly the capabilities of PAL and (2) focus on learning the UI and basic concepts/terminology.<br>*PAL example (left, center) and my own build (right) (3c.1b)*<br><img src="/assets/pal_10_01.png" alt="drones" width="25%" style="border: 1px solid #999;">  <img src="/assets/pal_10_05.png" alt="drones" width="33%" style="border: 1px solid #999;">  <img src="/assets/pal_10_02.png" alt="drones" width="30%" style="border: 1px solid #999;"><br><br>


#### **[2.5 PAL demos (speedruns)](/3c.2_pal_initial_demos/)**
*(MAIN DIAGRAM: 610/D1/xx, 611/612/613/D2/**TODO**, 614/D3/xx, 614/D3/xx, 615/D4/xx, 616/D5/xx, 617/D6/xx, 618/D7/xx, 619/D8/xx, 627/DD19/**OK**)*.
  - Current demos consist of just D1-D8, the first PAL demos I did (step by step tutorials). 
  - When I started, I was overwhelmed by the many dialogs (because I had not done examples first).
  - I documented all details with screenshots.<br>*Demos of core functionality (3c.2)*<br><img src="/assets/pal_10_13.png" alt="drones" width="37%" style="border: 1px solid #999;">  <img src="/assets/pal_10_14.png" alt="drones" width="50%" style="border: 1px solid #999;"><br><br>

<!-- You just did project setup / pipeline (goal 1). You know your way around Foundry. Now do demos that cover the rest of basic core Foundry functionality. Get hands-on experience before doing "operational" apps (goal 3).
  - **Your initial focus will be on 2 things**
    - **What button to press or where to click next.** The PAL dialogs are well done, but they require a lot of time to get used to.
    - **"I'm stuck.... how do I find a solution"**. PAL has AIP and FDE to help. 
  I just wanted to be shown what do. I did not care about options. So D1-D8 are a bit messy and not perfect, but 
    - They are MS.Word docx files that I can update easily. You can download that file and use it as your working notebook. **You need to keep lab notes**.

-->

#### **[2.6 DIY (with FDE assistance) demos](/3c.xxx_pal_gist/)**
*(MAIN DIAGRAM: 620/D9/xx)*.
- Creating real-world projects by working as a team with FDE (AIP/[PAL Pilot](https://www.palantir.com/docs/foundry/pilot/getting-started/)). (3c.3).<br><img src="/assets/pal_10_12.png" alt="drones" width="50%" style="border: 1px solid #999;"><br>

<!-- 
  - **Use AI (AIP/FDE) to do demos from scratch** (not following PAL demos or PAL docs; I might get inspiration from those demos, but I just use AIP/FDE to execute; in the future PAL Pilot would do this).
  - **D9 (demo set 9) = "haystack needle" demos**. I believe this was Palantir's original focus when founded:
    - Finding some small indication in a sea of data
    - Without/with AI.
  - Coming soon: Other AIP/FDE/Pilot demos.
 - **[PAL Pilot](https://www.palantir.com/docs/foundry/pilot/getting-started/)** (in beta now) will probably be an "FDE/AIP combo" that can "see" the dialogs and lead you by the hand through complicated setups.<br><img src="/assets/pal_10_07.png" alt="drones" width="40%" style="border: 1px solid #999;"><br><br> 
   - **[8 (3c.3b) Pilot real-world projects](/3c.3b_pal_pilot/) (NEAR FUTURE?)** .-->

<br>

## **3 Advanced hands-on (FUTURE)**

This will focus on partnering with FDE to cover 2 major topics areas
  - **3.1 Demos for *Foundry certification exam guide for application developer* topics** (the exam involves answering questions; this section uses the exam to determine what demos to do).  
  - **3.2 Other demos** (Managing Foundry environment, 24/7 operation, streams, deployments, packaging, sharing, etc).

<!-- Before creating these hands-on's I need to get a lot more hands-on experience myself.  -->


<br> 

#### **3.1 Demos for *Foundry certification exam guide for application developer* topics**
Use the exam as a guide for what demos to do to cover all the core topics that were not covered earlier.<br><img src="/assets/777_19.png" alt="drones" width="20%" style="border: 1px solid #999;"><br><img src="/assets/pal_15_02.png" alt="drones" width="55%" style="border: 1px solid #999;"><br><br>

#### **[3.2 "Other" demos (not sure exactly what yet)](/3c.2b_operational_apps/)**
Demos not covered earlier (and not in the exam; I don’t have a clear idea yet what the topics in this section would be). Up to this point you only use the apps for testing. They are not setup for end user usage, for real deployment ("deployment in the UI in the previous apps was more like "compile/run"). Demos for topics not covered yet. Maybe
  - managing Foundry environment, 
  - 24/7 operation, 
  - streams, 
  - packaging, sharing, deployments, dev social media, etc 
  
Basically whatever is inspired by **[Online PAL docs](https://www.palantir.com/docs/foundry/getting-started/overview/)**.<br><img src="/assets/777_20.png" alt="drones" width="50%" style="border: 1px solid #999;">

<!--  <br>*app that works 24/7, notifies, etc (this pic is not correct; just a placeholder)*<br><img src="/assets/pal_10_06.png" alt="drones" width="80%" style="border: 1px solid #999;"> -->

<br>

26.0808 (v1 26.0702) 

<br>
<br>
<br><br>
<br>
<br><br>
<br>
<br>
<br>
<br>

----------------
----------------
----------------

<br>

#### **OLD**

- **[A7 (3c.0) Concepts](/3c.ccc_pal_concepts/)**. My own take (see also **[Concepts CHATS ONLY](/pal_chats/)**).
  - What problems PAL solves. 
  - This section is a long term WIP (I started using PAL in July 2026, and I need more experience before I can sum up the concepts).<br><img src="/assets/pal_10_09.png" alt="drones" width="67%" style="border: 1px solid #999;"><br><br>

  - xxxx**[A6 (3c.1) PAL AI usage strategy](/3c.bbb_pal_strategy_fde/)**. 
    - PAL Foundry has 2 helps systems: (1) AIP and (2) FDE. 
    - I used both during the first 8 "Initial PAL demos" (3c.2). 
    - During demo 8 (of 3c.2) I asked AIP/FDE to show me how to do something that was not in the demo. The advantages of each tool slowly became apparent.
    - During the AIP/FDE demos (3c.3) I uses only AIP/FDE. It became apparent that
      - AIP is better for getting initial workflows.
      - **FDE is the lifesaver that can solve problems and (most of all) recognize screen shots (just paste in the window)**. In one example, FDE led me step by step in setting up a Workshop demo that I just could not get right (for good reasons).
    - I look forward to when AIP/FDE are combined into a single tool that can "see" dialogs and guide a user through various tasks.
      - NOTE: After almost a month of using PAL, I noticed PAL has a beta product called **"Pilot"**. That appears to be what I was talking about.
    - In general, a big focus (at least initially) is on prompt techniques and workflows to maximize effectiveness of using AI.<br>*FDE*<br><img src="/assets/pal_10_10.png" alt="drones" width="42%" style="border: 1px solid #999;"><br><br>

  - **[A8 (3c.4) Certification](/cert/)** (Foundry Application Developer). 
    - We've been (hopefully) using the PDF as a guide for what to study/build in goals (1-4).
    - Now need some certification (for me its **[Foundry Application Developer Certification](https://learn.palantir.com/page/exam-guides)**). For a system like PAL, most job will be in big projects. Certification matters.<br><img src="/assets/pal_10_11.png" alt="drones" width="28%" style="border: 1px solid #999;"><br><br> 


#### **Notes**
- *[PAL general notes](/3c.0_pal_notes/)*
- *[Palantir CEO火力全开，场面控制不住了！](https://www.youtube.com/watch?v=feUFT1Q-oBA)*
- *[zerohedge.com/ai/something-has-gone-completely-wrong-palantirs-alex-karp-goes-ballistic-openai-anthropic](https://www.zerohedge.com/ai/something-has-gone-completely-wrong-palantirs-alex-karp-goes-ballistic-openai-anthropic)*
- *https://www.youtube.com/watch?v=lSDC6-BdVus?t=341 HBM, diagram of NN, interconnecting multiple GPUs*


<!-- and reference material:
- A6-A8: AI usage / concepts / certification ([Certified Foundry Application Developer](https://learn.palantir.com/page/exam-guides))
  - The PAL certification exam guide says you need about 6 months experience with Foundry before taking the exam, so my personal goal is to (1) (write and) finish the SQS and (2) take the exam around the end of 2026 (I started using Foundry in early July 2026).
- Very organized, up-to-date (WIP) and detailed docx lab notes.  -->

<!-- 
###############################################################################################################
###############################################################################################################
###############################################################################################################
###############################################################################################################
###############################################################################################################
### **3c.4 Other AIP/FDE-led demos** (for finance, etc).**

(TODO)

<br> -->

<!-- ### **[3c.1 PAL app concepts (WIP)](/3c.ccc_pal_concepts/)**

(/3c.ccc_pal_concepts/)

This is a rough draft.... I only started using PAL in July 2026, so I still dont have a good grasp of the spectrum of what PAL apps do.  


<br>

### **[3c.2 First PAL demos](/3c.2_pal_aip/)**

For your first demos its probably best to do these (following my docx notes).  

See also: 
- **[PAL demo strategy](/3c.aaa_pal_strategy_demos/)**

I added numbering, conceptual diagrams, and a few error updates to the original demos. I will probably come up with my own set of demos. 

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
  - **Sections 2c, 2d were not in the demos. I prompted AIP/FDE for directions.** 

<br> -->

<!-- ### **[3c.3 AIP/FDE "haystack needle" (HN) demos](/3c.xxx_pal_gist/)**

(based on demo D8 listed in section "3 Demos" later on this page) -->

<!-- **These demos are my own, created by prompting AIP/FDE for the steps.** This was my goal from the beginning:
- In 3c.2 get enough experience so that 
  - I had an idea how to prompt AIP/FDE and
  - I could complete what they told me. 
- I did not really have enough experience, but still **I found out how to get FDE to lead me by the hand step-by-step through some difficult parts (Workshop config). This was perhaps the most important lesson.**

**What has interested me the most about Palantir for over a year now are the "haystack needle" (HN) algorithms**. This was the original reason for the founding of PAL. 9/11 occured because the US government failed to detect obvious warning signs in a sea of data. PAL's job was to make sure that that did not happen again by creating a system that could sift through vast amounts of data (about, for example, a sudden surge in foreigners studying to fly large airliners) to flag potential threats. To find the needle in the haystack. -->


<!--
But how exactly did they implement the HN algorithms? That's of practical interest currently because 
- (1) those **HN techniques are being used in all business segments** (not just military and intelligence) and 
- (2) **you can learn the details hands-on yourself for free with no assistance**by getting a PAL trial license (I have only a trial license and I am working alone). 

The goal of this page is to explain (via demos) the gist of a portion of the Palantir (PAL) toolset (there are not many competitors to PAL right now, but there will be in the near future, and they will follow a lot of the PAL methodologies). How to use that toolset to create HN apps. -->


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

<!-- 
- In the near future AIP/FDE could develop into higher level AI assistant that would lead the user by the hand through complex setups.
  - This would lead to a much larger customer base that does not depend on human FDE's. 
  - Competitors will come out with similar products soon (a lot of PAL expertise will transfer to these new systems).

**TL;DR** (too long; dont (want to) read)? If you are in a hurry, skip to 
- **[3c.3 AIP/FDE "haystack needle" (HN) demos](/3c.xxx_pal_gist/)** -->


---
layout: page
title: 3c Enterprise
permalink: /pal/
---

<br>

This section is about enterprise AI dev platforms that control almost everything. 
For now **the focus is 100% on Palantir Foundry** because 
- PAL is a market leader.
- **PAL offers a generous free demo account for hands-on experience for Foundry.**
- **The built-in AI help (AIP/FDE) made it possible to complete the demos (quickly)**. Without AI this would have taken at least 5x longer to do.
- In the near future AIP/FDE could develop into higher level AI assistant that would lead the user by the hand through complex setups.
  - This would lead to a much larger customer base that does not depend on human FDE's. 
  - Competitors will come out with similar products soon (a lot of PAL expertise will transfer to these new systems).

<!-- **TL;DR** (too long; dont (want to) read)? If you are in a hurry, skip to 
- **[3c.3 AIP/FDE "haystack needle" (HN) demos](/3c.xxx_pal_gist/)** -->


*The gist of Palantir: A crystal ball (called a "palantir" ("seeing stone") in Lord of the Rings) that can find a haystack needle (HN)* <br><img src="/assets/pal_9_06.png" alt="drones" width="25%" style="border: 1px solid #999;">

<br>

### **TOC** 


- **[3c.0 PAL app concepts (WIP)](/3c.ccc_pal_concepts/)** (my own take)
  - What problems are solved
  - This section is WIP (I only started using PAL in July 2026).<br><br>

- **[3c.1 PAL AI usage strategy](/3c.bbb_pal_strategy_fde/)**. PAL Foundry has 2 helps systems: (1) AIP and (2) FDE. 
  - I used both during the first 8 "Initial PAL demos" (3c.2). 
  - During demo 8 (of 3c.2) I asked AIP/FDE to show me how to do something that was not in the demo. The advantages of each tool slowly became apparent.
  - During the AIP/FDE demos (3c.3) I uses only AIP/FDE. It became apparent that
    - AIP is better for getting initial workflows.
    - FDE is the lifesaver that can solve problems and especially recognize screen shots (just past in the window). In one example, FDE led me step by step in setting up a Workshop demo that I just could not get right (for good reasons).
  - I look forward to when AIP/FDE are combined into a single tool that can "see" dialogs and guide a user through various tasks.
  - In general, a big focus (at least initially) is on prompt techniques and workflows to maximize effectiveness of using AI.<br><br>

- **[3c.2 Initial PAL demos](/3c.2_pal_initial_demos/)**. Currently just D1-D8, the first PAL demos I did (step by step tutorials). For your first demos its probably best way to start (I kept detailed docx notes of what I did in these demos).

- **[3c.3 AIP/FDE demos](/3c.xxx_pal_gist/)**.
  - I use AI (AIP/FDE) to do my own demos (no PAL demos or PAL docs).
  - The focus for now is on what I call "haystack needle" demos (finding some small indication in a sea of data) with or without AI. 
  - I imagine AIP/FDE can lead me through other demos. In general, my planned initial demos are to focus more on demonstrating functionality with minimal examples.
  

<!-- - **3c.4 Other "deep dive ASAP" PAL demos** (for finance, etc). (TODO) -->

<br>



### **Notes**
- *[PAL general notes](/3c.0_pal_notes/)*
- *[Palantir CEO火力全开，场面控制不住了！](https://www.youtube.com/watch?v=feUFT1Q-oBA)*
- *[zerohedge.com/ai/something-has-gone-completely-wrong-palantirs-alex-karp-goes-ballistic-openai-anthropic](https://www.zerohedge.com/ai/something-has-gone-completely-wrong-palantirs-alex-karp-goes-ballistic-openai-anthropic)*
- *https://www.youtube.com/watch?v=lSDC6-BdVus?t=341 HBM, diagram of NN, interconnecting multiple GPUs*

<br>

26.0725 (v1 26.0702) 

<!-- ### **3c.4 Other AIP/FDE-led demos** (for finance, etc).**

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

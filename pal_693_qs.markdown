---
layout: page
title: Foundry Quick Start (v02 26.1106)
permalink: /pal_693_qs/
---

<br>


[← 3c Enterprise](/pal/)

<br>

#### For the **latest QS version see [docx #693](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**.

This QS is a work in progress (WIP).

This online version was created from the docx by ChatGPT. The formatting is WIP, but the contents are technically accurate and up-to-date.

<br>

#### **TOC**
- **[What makes this the best first demo for Foundry](/pal_693_qs_0a_best_demo/)**
- **[0 First steps](/pal_693_qs_0b_first_steps/)**
- **[1 Fetch MockAPI records and display in UI ("Workshop")](/pal_693_qs_1_mockapi/)**
- **[2 Create (1) AIPLF to detect matching digits in object text/integer properties / (2) UI to display result](/pal_693_qs_2_ailpf/)**
- **[3 Modify AIPL prompt to detect matching letter-only-text and integer-digits (display result in UI)](/pal_693_qs_3_aipl_prompt/)**
- **[4 Enter AI matching criteria (configure only AIPL+F and UI)](/pal_693_qs_4_criteria/)**
- **[5 Add an object property and Action to save the LLM response (used in Chapter 6)](/pal_693_qs_5_property_action/)**
- **[6 Add a text-save action (A1) call in AIPL / create AIPLF / create action (A2) to call AIPLF (use in Ch7)](/pal_693_qs_6_a1_a2/)**
- **[7 Add automation ("(new) object added to set" inits automation)](/pal_693_qs_7_automation/)**
- **[8 Schedule MockAPI DATASET import / Add new Capstone2Record / Trace automation](/pal_693_qs_8_schedule/)**
- **[9 Where to go from here](/pal_693_qs_9_where_next/)**

<br>


_Workflow diagram for ch1_<br><img src="/assets/qs/0a_01.png" alt="Foundry screenshot" width="75%" style="border: 1px solid #999;">


<br>


#### **Notes**

The FDE-generated text is factual, but for a human reader at times difficult to understand. After finishing the demo setup and test, I redid the H1 headings (it was a **[long discussion with FDE](/pal_693_ch_title_chats/)**, but basically all of my corrections were needed and correct except for one mistake). 

I also created diagrams to summarize the setup workflows. FDE can "see" these diagrams and is quite good at making useful suggestions or catching errors. 


<!-- <img src="/assets/sun-55.png" alt="drones" width="61%" style="border: 1px solid #999;">


<img src="/assets/sun-56.png" alt="drones" width="70%" style="border: 1px solid #999;">
-->


<br>

---

<br>

26.1106 (v1 26.1104)

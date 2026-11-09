---
layout: page
title: Foundry Quick Start (26.1109)
permalink: /pal_693_qs/
---

<br>


[← 3c Enterprise](/pal/) 

<br>

#### For the **latest QS version see [docx #693](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**.

- The main goal of this QS is accuracy and usefulness (that means constant updates). 
- Constant updates is best assured with markdown/PNG's (pics) extracted from the 693 docx source file by GPT.
- The PNG sizing is difficult for GPT to get right (GPT does adjust the width of the PNG based on text in the PNG; the result is an improvement, but I need to "hardcode" the width (in my docx file) to get things right).

<br>

#### **TOC**
- **[What makes this the best first demo for Foundry](/pal_693_qs_0a_best_demo/)**
- **[Configuration / workflow diagrams](/pal_693_qs_0a2_config_dias/)**
- **[0 First steps](/pal_693_qs_0b_first_steps/)**
- **[1 Fetch MockAPI records and display in UI ("Workshop")](/pal_693_qs_1_mockapi/)**
- **[2 Create (1) AIPLF to detect matching digits in object text/integer properties / (2) UI to display result](/pal_693_qs_2_ailpf/)**
- **[3 Modify AIPL prompt to detect matching letter-only-text and integer-digits (display result in UI)](/pal_693_qs_3_aipl_prompt/)**
- **[4 Enter AI matching criteria (configure only AIPL+F and UI)](/pal_693_qs_4_criteria/)**
- **[5 Add an object property and Action to save the LLM response (used in Chapter 6)](/pal_693_qs_5_property_action/)**
- **[6 Add a text-save action (A1) call in AIPL / create AIPLF / create action (A2) to call AIPLF (use in Ch7)](/pal_693_qs_6_a1_a2/)**
  - **[pal_693_qs_0a2bbb_a2_aiplf_a1](/pal_693_qs_0a2bbb_a2_aiplf_a1/)**
- **[7 Add automation ("(new) object added to set" inits automation)](/pal_693_qs_7_automation/)**
- **[8 Schedule MockAPI DATASET import / Add new Capstone2Record / Trace automation](/pal_693_qs_8_schedule/)**
- **[8a Governance: allow, block, verify](/pal_693_qs_8a_governance/)**
- **[8b Where these mechanics could be used](/pal_693_qs_8b_real_apps/)**
- **[9 Where to go from here](/pal_693_qs_9_where_next/)**
- **[10 (appendix) How the QS site pages were generated (from docx)](/pal_693_qs_10_docx_gen/)**

<br>

#### **Workflow diagram examples**

_Workflow diagram for ch1_<br><img src="/assets/qs_summary_ch1.png" alt="Foundry screenshot" width="75%" style="border: 1px solid #999;">

_Workflow diagram for ch6_<br><img src="/assets/qs_summary_ch6-1.png" alt="Foundry screenshot" width="75%" style="border: 1px solid #999;">

_Workflow diagram (perspective 2) for ch6_<br><img src="/assets/qs_summary_ch6-2.png" alt="Foundry screenshot" width="75%" style="border: 1px solid #999;">


<br>


#### **Notes**

The FDE-generated text is factual, but for a human reader at times difficult to understand. After finishing the demo setup and test, I redid the H1 headings (it was a **[long discussion with FDE](/pal_693_ch_title_chats/)**, but basically all of my corrections were needed and correct except for one mistake). 

I also created diagrams to summarize the setup workflows. FDE can "see" these diagrams and is quite good at making useful suggestions or catching errors. 



<br>

---

<br>

26.1109 (v1 26.1104)

<!-- 
- The priority is to prevent screenshots from appearing too large on the webpage.
- Examine the text size inside EACH screenshot individually.
- Adjust the width="xx%" in each <img> tag so the displayed screenshot text approximately matches normal webpage body text.
- Use 16px as the initial webpage text-size reference.
- Prefer slightly smaller screenshots rather than oversized ones.
- Do NOT use a fixed width percentage for all images.
- Do NOT resize the PNG files; adjust only the HTML width percentage.
- Preserve aspect ratios. Avoid unnecessary upscaling.

Image width override:
•	If width=35 (or any other number) appears immediately before an image in the DOCX, use that number as the HTML image width percentage (width="35%").
•	This overrides all automatic image-sizing rules. Do not inspect or recalculate the width.
•	Do not include the width=35 instruction itself in the generated Markdown.
•	If no width instruction is present, apply the normal image-sizing rules.

-->

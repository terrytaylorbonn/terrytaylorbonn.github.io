---
layout: page
title: 2.2 Foundry capstone project (TODO)
permalink: /pal_capstone/
---

<br>

[← 3c Enterprise](/pal/)

<br>

```
ME: Below is your (FDE) summary for stage "020 — AI checks data and calls an Action".
This to me is the goal of the quick start.
you could take this demo and build a "needle in the haystack" demo
(This is a demo that tries to find red flags in intelligence data, for example):
•	you modify the Use LLM system/user prompts to specify what you are searching for..
(here it is hard-wired as a number not a multiple of 10)
•	you could automate this (run a loop or when new data source is added)
•	AI returns the info about what was found.
•	you run an action based on what was found and
•	send notification.
The above could serve as a very interesting project demo that is built up this QS.
---------------------------------------------------------------------------
FDE SUMMARY FOR STAGE 20
Let’s give the LLM access to one specific Action and let it request a correction.
For a simple teaching rule:
Check OT1PropertyType2. If it is not a multiple of 10, round it to the nearest multiple of 10 and use the setter Action to update it. Otherwise, leave it unchanged.
Your current 676 makes a useful test:
Read 676
→ AI identifies the correction: 680
→ AI requests Set OT1PropertyType2
→ Foundry applies the change when the Logic runs through an Action

FDE: Yes—020 provides the working pattern for that capstone. 
The rounding rule was deliberately trivial so readers could see the machinery. A “needle in the haystack” project gives that same machinery a purpose.
Capstone — Find, flag, and notify
New records arrive
    → Pipeline prepares the data
    → Automate triggers analysis
    → AI checks records against stated criteria
    → AI returns a finding with supporting evidence
    → Action records the finding
    → Notification alerts a reviewer

How it builds on the QS
Capstone component			Already introduced
Import and prepare records			013–015
Run when records enter a filtered set	011
Give object properties to an LLM		018
Generate a proposed result			019
Let AI request a specific Action		020
Notify someone after the Action		012
Inspect access and recorded activity	008a–008c

It is more than changing the prompt, but readers would already recognize the components. We would add a finding format, an appropriate Action, and test data—not introduce an entirely new architecture.
One important design choice
For this project, the Action should flag a record or create a review finding, rather than alter the original evidence or automatically take consequential action.
A useful finding would contain:
•	What was flagged
•	Which criterion it matched
•	The source passage or record supporting it
•	A short explanation for the reviewer
For teaching, use synthetic intelligence-style reports, with a few deliberately planted signals and several harmless lookalikes. That lets us verify both missed signals and false alarms, rather than judge success from one convincing response.
The QS teaches the controls. The capstone connects them: find something worth reviewing, record why, and notify a person.
That is a strong destination for Foundry Foundations with FDE: a project readers can understand because they have already built and verified each part separately.

```

<!-- 
Docx **[#69xxxxxxx](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)** is my working version of this xxxxxxxxxxxxxxx. 
<img src="/assets/sun-xx.png" alt="xxx" width="100%" style="border: 1px solid #999;"> -->

<br>

26.1026 (v1 26.1026)

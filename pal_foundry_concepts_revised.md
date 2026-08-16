---
layout: page
title: concepts revised
permalink: /concepts_revised/
---

<br>


FILENAME: **#610_pal_D1_foundry_MINE_v10_26.0815_SS_CONCEPTS_ONLY.docx**_SS

previous _v03_26.0809, 0704

SEE #610bbb_pal_D1_foundry_PAL_v08_26.0814_SS.docx for my original demo version

- **The original PAL doc for this demo1 **(https://learn.palantir.com/speedrun-your-first-e2e-workflow) **says** "**In the next 60 minutes you will build a fully-functional end-to-end workflow. Don’t worry about understanding the ins-and-outs** - the objective of this course is to give you a taste of some major Foundry components so that it all makes sense once you go into deeper trainings. "

**The ZAI version of demo1/doc takes a different approach:**

- **focus on mastering concepts and terminology explanations**. These are critical if you want to understand how this works. and move forward efficiently to more complex demos.

- **details and simplicity to help you navigate the complexity**. the H1/H2 headings in this doc are numbered (in Foundry docs are not).  minimal text / diagrams, but more critical details (they were criticial for me as a hands-on new user to get started with Foundry)

**Note: The current version is a "bare-bones" draft... I will add more explanatory/conceptual text in the future.**

TOC

- Concepts
  - C1 Why learn to use Palantir Foundry?
  - C2 Why learn with the ZAI version of Palantir Foundry demo1
  - C3 Comparison of original PAL and ZAI final demo result
  - C4 ZAI demo 3 phases
  - C5 ZAI demo diagrams (very helpful)
- Phase 1: Pipeline/ontology
  - 2 Open FDE and create project/folder
  - 3 Download 3 source data files (csv) to your PC and upload to Foundry
  - 4 Create pipeline
  - 5 Create ontology
  - Phase 1 final test: View/compare dataset/ontology
- Phase 2: Basic UI (display only, no edit) (steps 1-22)
  - Overview diagram (for 6.4-6.6)
  - 6.4 Create object table (UI LEFT) (1-2c)
  - 6.5 Create filter (UI RIGHT) (3-10)
  - 6.6 create button label, button, property list (UI CENTER) (11-22)
  - Phase 2 final test
- Phase 3: Action UI (steps 23-32 (action type), 33-36 (UI))
  - 7 Create action type for the object type (from 5.1) (23-32)
  - 8.3 Attached action type to UI button (33-36)
  - Phase 3 final test
- notes

<br>
# **Concepts**

<br>
### **C1 Why learn to use Palantir Foundry?**

There are good reasons why Palantir has gone viral. **Palantir Foundry represents the logical culmination of ZiptieAI:**

- (2) neural networks,

- (2b) models,

- (3) agents,

- (3b) workflows, and

- **(3c) enterprise platforms**

The workflows and concepts are crucial learning for understanding how AI should really be used in enterprises (and perhaps your own small business).

<br>
### **C2 Why learn with the ZAI version of Palantir Foundry demo1**

<br>
#### **You only really understand Foundry after you have done a hands-on demo**

And you can easily get started with a free trial of Foundry (if you are located in certain countries).

I am not an expert. And you dont need to be either to get started with Foundry.

And I think a big market for Foundry might be (in the future) for those like myself.

The general (tech savvy) public, the techie in small companies who needs something like Foundry.

<br>
#### **The main barrier is getting used to the dialogs and the concepts**

That was my biggest challenge: Navigating the dialogs.

and understanding why I was doing what I did in the demos.

<br>
#### **The ZAI versions of the demos/docs make it easier to get started**

ZAI focuses on

- The simplest demos possible to get the point across.

- Repetition. This is the most important aspect when first starting out with Foundry.

- Gradually experimenting yourself with modifications of your own demos (with the help of FDE, Foundry's excellent AI assistant (that can even "see" pasted screenshots of dialogs of your setup))

<br>
#### **Why this demo1 is so important (and why should you spend about a week on it)**

The original doc says to budget 60 mins to do demo1.

- It took me days just to get the basic demo running. The main reason was the demo was very long and you did not verify it was working until you got to the end.

- I was not just doing the docs, but documenting my steps and reorganizing the demos on the ZAI website).

- I spent several days to do workflow diagrams alone.

You should should spend at least 3 days on this demo.

- Foundry is a very sophisticated system that introduces key concepts. You need to understand those concepts. Its kind of like your first computer, your first browser, or your first search engine. Its a whole new world.

- This simple demo1 intros many of those key concepts.  I pay great attention to minimal text/diagrams AND critical details. Key terminology and concepts are intro'd with hands-on demos.

- If you don't master the basics in the first demo, you will just get more lost in fuure demos.

<br>
### **C3 Comparison of original PAL and ZAI final demo result**

The PAL site has an impressive number of very useful demos and docs.

The goal of ZAI is to make it easier for you to eventually exploit that gold mine of info.

<br>
#### **Original PAL demo1**

The original demo output looked like this.

- The original demo wanted to show an impressive looking demo to show whats possible. While requiring only 60 minutes of your time. Not possible.

- The sections squared in red are the only parts of the original demo that are done in this demo.

<img src="/assets/pal_01.png" alt="drones" width="85%" style="border: 1px solid #999;">

Original demo doc: https://learn.palantir.com/speedrun-your-first-e2e-workflow

<img src="/assets/pal_02.png" alt="drones" width="75%" style="border: 1px solid #999;">

PS: About the "25 of 47 lessons completed". I don't understand what happened. I did this demo several times. I'm not going to spend time trying to figure out the lesson verification process.

<br>
#### **ZAI demo1**

The ZAI focus is on

- The details you need to know to get this working. reliably.

- The details that are important to understand for basic Foundry skills.

- Step by step with minimal text/diagrams (focus only on the core stuff).

The following shows the ZAI final UI.

- It demonstrates all the core concepts in the original demo.

- It is split up into 3 different sections, each with a final test to make sure what you did is working.

<img src="/assets/pal_03.png" alt="drones" width="100%" style="border: 1px solid #999;">

<br>
### **C4 ZAI demo 3 phases**

<img src="/assets/pal_04.png" alt="drones" width="65%" style="border: 1px solid #999;">

<br>
#### **Phase 1: Input csv files -> pipeline -> datasets -> ontology objects**

**Pipeline/dataset**

<img src="/assets/pal_05.png" alt="drones" width="100%" style="border: 1px solid #999;">

**Ontology object type "All Orders" (only one)**

Note: "All Orders" is not a good name for the object type (it should be "Order"). I will fix this (and many other smaller errors) in a future version of this demo. The important aspect of this demo is that it shows you clearly how to set everything up, and clearly discusses my errors and mistakes (and also mentions where I use AI, which I do whenever I can, and I note in this doc if text was AI generated (usually a cleaned up version of my own "seed" text)).

<img src="/assets/pal_06.png" alt="drones" width="45%" style="border: 1px solid #999;">

<img src="/assets/pal_07.png" alt="drones" width="100%" style="border: 1px solid #999;">

<br>
#### **Phase 2:  Basic UI for displaying ontology objects**

1 RIGHT panel: Select Item Name.

2 LEFT panel: View list for that item.

3 CENTER panel: View object selected in LEFT panel.

<img src="/assets/pal_08.png" alt="drones" width="100%" style="border: 1px solid #999;">

<br>
#### **Phase 3: Edit the ontology**

<img src="/assets/pal_09.png" alt="drones" width="90%" style="border: 1px solid #999;">

Click the button.

Edit the Assignee.

<img src="/assets/pal_10.png" alt="drones" width="45%" style="border: 1px solid #999;">

Click Submit.

The change is save in the ontology (but NOT in the dataset or original csv files).

<img src="/assets/pal_11.png" alt="drones" width="85%" style="border: 1px solid #999;">

NOTE: In this demo you simply change the Assignee string... you are not selecting from the Assignee list.

Thats how it was in the original demo, and its good enough for a first version.

<br>
### **C5 ZAI demo diagrams (very helpful)**

The most important diagram is the detailed diagram.

<br>
#### **Simple summary diagram**

This is the simple diagram I use to summarize all demos.  Below is the version modified for this demo. This demo does not do any analysis and does not use AI.

[1a] = local files/manual upload → starting data in Foundry

[1b] = Pipeline Builder cleans/joins/unions data → output dataset

[3]    = output dataset becomes ontology object type

[5]    = Workshop reads ontology objects and displays

[3b] = define ontology action/write capability

[5/3b] = use UI to execute the action

<img src="/assets/pal_12.png" alt="drones" width="95%" style="border: 1px solid #999;">

<br>
#### **Detailed diagram (with numbered steps) (mainly for UI configuration)**

- The big numbers in red are the chapter numbers I added to the original doc. For some reason heading levels 1 and 2 were not numbered.

- Text such as "(1-6.4.s2)" means

- this is step 1 in my version (36 total)

- 6.4 is the numbering i added to the original doc

- s2 = step 2 (these are basically heading level 3 and were numbered in the original).

This diagram may look a bit confusing, but its extremely helpful when trying to track your steps (espcially for the Workshop UI).

<img src="/assets/pal_13.png" alt="drones" width="100%" style="border: 1px solid #999;">

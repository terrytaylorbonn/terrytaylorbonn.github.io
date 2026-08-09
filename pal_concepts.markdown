---
layout: page
title: Palantir concepts (WIP)
permalink: /pal_concepts/
---



<br>

# **THIS PAGE NEEDS AN UPDATE....**

<br>

I am still working on **my own take on the core conceptual gist of Palantir-SW**, but basically its 
- Palantir makes the enterprise visible and governable.
- LLMs make parts of that visibility probabilistic, so they must be sandboxed, verified, and logged.

See also **[Concept CHATS](/pal_chats/)**.


In the diagram below 
- LEFT: Before LLMs, the Palantir-SW had just wizards/magic-balls (the analyzers and the watchers of the analyzers) that were implemented in procedural programming. Trustd, reliable and safe (not human, but programmed by a trusted human programmer-employee). Like the old wizard in Lord of the Rings. 
- RIGHT: With LLMs, the Palantir-SW now has new AI wizards/magic-balls embedded inside the old wizards/magic-balls. AI has no intelligence (and can not be trusted). An LLM is programmed on training data that you did not control (and you can not determine the training data from analyzing the model, even if you knew the NN weights/biases). And the model is often remote. This requires extra security that Palantir-SW provides. **You need Palantir-type systems now more than ever.** 

*The trusted wizard (left) with his crystal ball (called a "palantir" ("seeing stone") in The Lord of the Rings) and (right) an LLM (AGI = super human intelligence hosted on digital circuits; this is more of a myth than "Lord of the Rings"; LLMs have no intelligence and therefore can not be trusted)* <br><img src="/assets/pal_9_06.png" alt="drones" width="25%" style="border: 1px solid #999;"> <img src="/assets/777_02.png" alt="drones" width="30%" style="border: 1px solid #999;"><br>

<br> 

---------
---------

<br>

# **CORE DIAGRAMS** 

<br>

### **1 palantir.com/docs/foundry**


*(numbers added)*<br><img src="/assets/777_08.png" alt="drones" width="64%" style="border: 1px solid #999;">

<!-- <br> 

*before AI*<br><img src="/assets/777_07.png" alt="drones" width="74%" > -->

<br> 

<!-- **AI CREATION DETAILS NEEDED**
- NO DIRECT LLM ACTIONS ("usually not directly")
- deterministic/human-approved

*with AI helpful assistant (**3b WRITE = 3b ACTION**)*<br><img src="/assets/777_09.png" alt="drones" width="74%" > -->

### **2 Main diagrams for example/demo/deep-dive** (26.0806)

<br>

#### **2.1 The initial workflow diagrams**

For the demos I wanted a more mechanistic conceptual overview (I am more interested in the mechanics of the PAL tools used than the business cases). At first I wanted something like the simple Foundry workflow diagram below with text to summarize what parts an example/demo covered. 

*Basic PAL diagram*<br><img src="/assets/777_07.png" alt="drones" width="74%" >

For example, for Code Repo demo D19, this is what is covered 

```
1 Data source          ✓ raw CSV datasets
1b Pipeline            ✓ code-based PySpark transforms
3 Ontology read        —
3b Actions/writeback   —
4 Analysis             —
5 UI/app               —
6 Security/governance  ✓ branching, commits, checks, build
AI                     xxAI, except optional AIP Assist
```

<br> 

<!--

But I prefer the more detailed diagram below. The idea is to show
- All possible workflow
  - steps 
  - functionality (as text below the diagram)
- Highlight all those aspects used in
  - ORANGE for examples (which install everything for you)
  - RED for demos/deep-dives (which required you to build everything)

For example the main diagram for **[E11](/3c.1b_pal_examples/)** (example 11).

*(MAIN_E11.png)*<br><img src="/assets/MAIN_E11.png" alt="drones" width="74%" >

<br> 
-->


#### **2.2 Current workflow diagrams**


**[E11](/3c.1b_pal_examples/)**. Example main diagram for E11 (example 11): shows the main workflow; orange squares highlight those items included in example install.

*(MAIN_E11.png)*<br><img src="/assets/MAIN_E11.png" alt="drones" width="74%" >


**[D19](/3c.2_pal_initial_demos/)**. Example main diagram for D19 (demo 19): shows the main workflow; red squares highlight those items implemented for demo D19 (this is a a very rought first draft that will change greatly as I figure out the details).

*Numbers 1-6 (1a,1b) correspond to the numbers I added to the main diagram above (from palantir.com/docs/foundry) (MAIN_D19.png)*<br><img src="/assets/MAIN_D19.png" alt="drones" width="74%" >

<br> 

#### **2.3 Future diagrams**

At some point I will start to "weed out" the things that dont belong in each main diagram. I dont want all that useless verbiage (I might have a master main diagram that has all the text, for not for each example/demos). But for now I want to keep a lot of the verbiage as my own notes (until I get to understanding all the details better). 

*(MAIN_E17.png)*<br><img src="/assets/MAIN_E17.png" alt="drones" width="74%" >

<br>

26.0806 (v1 26.0804)

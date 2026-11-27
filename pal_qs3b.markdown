---
layout: page
title: 3.4b (TODO) QS3b -- Complete overview of foundry tools (apps)
permalink: /pal_qs3b/
---


<br><br>




# (1) i am starting to think that all of our mini-demos should go into a separate QS.
and in the other QS's we simply reference this qs. 
so we would have 
QS0
QS1
QS3
then this QS4  (referenced by QS0,1,3)
then training/agents QS5

(2) QS3 becomes a single docx file.

(3) question: what makes QS3 required? 
what does it intro that is not in QS0,1?


**Yes—that organization is cleaner:**

| Tutorial | Purpose |
|---|---|
| **QS0** | Install, inspect, and adapt a realistic geospatial example |
| **QS1** | Build the AI-enabled matching workflow from scratch |
| **QS3** | Understand the connected application mechanics through D1–D6 |
| **QS4** | Numbered, selectable **Explore** mini-demos of Foundry tools |
| **QS5** | Models, training, hosted inference, and agents |

QS0, QS1, and QS3 can reference **QS4’s Explore sections** without duplicating them. Combining **QS3 D1–D6 into one DOCX** then makes sense: they form one connected exercise, while the tool introductions remain independent.

## What makes QS3 required?

**Nothing makes all of QS3 universally required after QS0 and QS1.** There is substantial overlap. Its value is filling specific gaps and making previously implicit mechanics explicit.

### The strongest additions

| QS3 module | What it adds beyond QS0/QS1 |
|---|---|
| **D1: Transformations** | A systematic clean → validate → split valid/rejected → join → calculate chain, plus a build-blocking quality check |
| **D2: Linked objects** | Two object types connected by an explicit link; navigation both ways; source changes updating relationships |
| **D3: Interactive UI** | A selected Group drives a linked-Items table, count, and selected-Item details; empty-state behavior and filtering |
| **D4: Saved changes** | Explicitly demonstrates dataset-supplied values updating while an edit-only property retains its saved value |
| **D5: Human review** | Separates AI suggestion, human decision, and committed Status; Accept and Reject have different effects |
| **D6: Operation/governance** | Branch → proposal → merge → deployment verification; controlled two-user authorization testing and restoration |

### What is mostly reinforcement?

- Python imports and dataset builds.
- Basic object-type creation.
- Basic Workshop configuration.
- AIPL → published Function → wrapper Action.
- Scheduling, automation, and some access-control concepts.

Those were already introduced in QS0/QS1.

## How I would position QS3

Rather than **“required before continuing,”** say:

> **QS3: Connect the pieces—data quality, linked objects, saved changes, and human review**  
> Build a small application that makes these mechanisms explicit. Readers who completed QS0/QS1 can focus on the unfamiliar chapters.

**QS4 should list prerequisites per Explore—not require the whole QS3.** For example:

- **[19] SQL Studio:** needs a suitable dataset.
- **[55] Workflow Lineage:** benefits from a connected application.
- A new reader can use equivalent resources or ask FDE to help prepare them.

**In short: QS3 supplies a richer reusable example and several important new mechanisms; QS4 supplies the tool-discovery catalog. Neither needs to force every reader through material they already understand.**

<br><br>

# sounds good.

my thinking is that a new user needs to focus on the mechanics of QS0-3 (assume there is no 1),
getting used to the dialogs, the basics, not focusing on big picture stuff.
but after 3 QS's , then its time in QS4 to get the big picture (minus training/agents).

**Yes—that gives the sequence a clear teaching rationale: experience first, then organize that experience into a broader map.**

- **QS0–QS3:** follow concrete exercises, become comfortable with the dialogs, and learn the basic mechanics. Conceptual explanations support the immediate task rather than interrupt it with the whole platform.
- **QS4:** step back and explore the wider Foundry landscape through short, selectable **Explore** demos. Readers can now relate unfamiliar tools to mechanisms they have already used.
- **QS5:** extend that understanding to model training, hosted inference, and agents.

So QS4 is **not just a miscellaneous tool bucket**. It is where readers develop the **big picture through hands-on discovery**, using your North–Equator–South framework.

A possible title:

> **QS4: Discover the Foundry landscape—one tool at a time**


<br><br>

# I dont like the words "discover" or "landscape" .... 
its about getting the big picture, teh complete picture of what foundry can do.
what other titles can you think of?


My strongest choice:

**QS4: The big picture—what Foundry can do**

Other options:

- **QS4: Foundry’s capabilities—beyond the basics**
- **QS4: Understanding Foundry as a whole**
- **QS4: Putting Foundry together—tools, capabilities, and connections**
- **QS4: From individual workflows to the bigger picture**
- **QS4: What else can Foundry do?**

Suggested subtitle:

*Short, hands-on tool demos connecting familiar workflows to Foundry’s broader capabilities. Models and agents continue in QS5.*

<br><br>

# "a complete overview of foundry tools (apps)" ??

QS4: A complete overview of Foundry tools (apps)

That fits your goal: show what each tool does, where it fits, and introduce it through a short Explore demo.

Keep WIP while coverage is incomplete, and note that models and agents are covered in QS5.

<br><br>

# so basically i use Foundry to create a north, equator, south.
what do we call what we created?   

**A Foundry application**—or, emphasizing all three parts, **an end-to-end Foundry application**.

In your NES framework:
- **South:** connected sources and external services.
- **Equator:** data processing, objects, relationships, and execution logic.
- **North:** interfaces for people to analyze and act.

**The Workshop UI is the front end; the complete application includes the connected data and logic behind it.**

For the entire tutorial build, **“end-to-end Foundry application”** is a good label.



<br><br>

# exactly... but i never see a term for this in FOUndry docs.
instead, the tools are called apps..
so i recommend in ZAI docs we always call them "tools (apps)"

**Agreed—for ZAI docs, we’ll use:**

- **Tool (app):** an individual Foundry tool, such as **[22] Workshop**, **[31] Data Lineage**, or **[19] SQL Studio**.
- **Foundry application:** the complete solution we build across **North, Equator, and South**.
- **UI:** its user-facing interface—not the whole application.

That keeps **the tools we use** distinct from **the application we create**.


<br><br>

# so we showed that you can take app components from different projects and use them together 
(UI for QS0 was in a different project that the rest of the app components).
for most softwares (i am using a logical plural here, despite not being proper english),
you can not do this (mix and match components from different projects)?
what is a foundry project for?


**We demonstrated cross-project reuse, yes—but other software systems often support it too.** They may do so through shared libraries, packages, APIs, or references between projects. The meaning of **“project”** varies considerably between products.

## What is a Foundry project for?

A **Foundry project is primarily an organizational and access-management container**, not the boundary of one complete application.

It helps you:

- **Organize resources:** datasets, repositories, pipelines, UIs, and other components.
- **Manage access:** assign project roles and inherited permissions.
- **Group related work:** provide a cover page, documentation, and a recognizable location.

**Dependencies define how the application works; project membership defines where resources are organized and helps control access.**

## Our QS0 example

| Component | Location |
|---|---|
| Installed geospatial example | **QS0b** |
| Our independent pipeline, dataset, object type, and Map | **QS0c**, formerly QS0_Build |
| Our **QS0_NeedleViewer UI** | **QS0b**, accidentally |

The UI still works because it references the correct object type. **Those references do not require the components to share a project.** Required permissions still apply; putting the UI in one project does not automatically grant access to data elsewhere.

For ZAI docs:

> **A Foundry application can span several projects. Projects organize resources and help control access; references connect the resources into a working application.**

<br><br>

# OK,  so this is important concept that needs to be demo'd somewhere.
I from the beginning wondered why projects exist. 
we could also  put this into QS3, or somewhere. .....

**Yes—put the concept near the beginning of QS3**, when the reader first opens **OntologyDemo001 (project)**.

### Suggested heading
**Projects organize components—not entire applications**

Explain:

> **A project groups resources and helps manage access. A Foundry application is the connected set of resources that performs the work, and those resources can live in different projects.**

Then reference a short **QS4 Explore demo using [59] Projects & files**:

1. Locate **QS0_NeedleViewer** in **QS0b**.
2. Inspect its object-set input in **[22] Workshop**.
3. Open **QS0 Correlated Intelligence** and verify its location in **QS0c**.
4. Run the UI to verify that the cross-project connection works.

**No moving, copying, or new resources required.** Our accidental placement becomes a useful demonstration—with the reminder that cross-project references do not bypass permissions.


<br><br>

# ok, great, we will cover this in [59] and [22] .
ok... i have stuff to do ... will be back in a few hours.

Agreed—we’ll cover **projects versus complete applications** in **[59] Projects & files** and **[22] Workshop**, using the QS0 cross-project example.

Next pending mini-demo: **Explore-9: [6] Contour**. See you later!



<br>

26.1127 (v1 26.1127)

---
layout: page
title: 3.4 QS3 -- Broaden your Foundry skills 
permalink: /pal_693_dd/
---

<br>

[← 3c Enterprise](/pal/) 

<!-- <br>

_xxxxxxxxxxxxx_<br><img src="/assets/qs/0a/0a_01.png" alt="0a illustration 1" width="65%" style="border: 1px solid #999;"> -->

<br>

_See the 26.1124 chat after the diagram below._

QS0 and QS1 had one focused goal — find the “needle in the haystack” — using simple and short demos. The goal of this DD is to cover the topics (hands-on) in the QS's in more detail and cover topics that were not in the QS's. 

<!-- The plan is to reference official PAL speedruns, demos, and examples in the DD. -->

This **Deep Dive (DD)** focuses on much more:
  - a broad, hands-on introduction to Foundry’s apps and techniques, not exhaustive depth in each one.
  - a wider tour of Foundry, with small, mechanistic exercises that show what each capability does, which app configures it, and how to verify it.
  - EQUATOR-SOUTH-NORTH
    - D1–D6 provide the EQUATOR backbone. 
    - SOUTH extensions introduce different sources and ingestion techniques; 
    - NORTH extensions introduce different analysis and interaction tools.
  - The guiding rule for DD is:
    - Introduce each app or technique through a small working example, connected to familiar data and mechanisms
    - That gives readers both breadth of exposure and a mental map of where each capability fits—without turning every introduction into a complicated project.

Below is the "master" diagram for the initial version of D1-D6.
-	D1: Import and transform data _(**[#692\_pal\_foundry\_d1\_data\_xforms\_.docx](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**)_
-	D2: Create object types and links from datasets _(**[#691\_pal\_foundry\_d2\_linked\_objects\_.docx](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**)_
-	D3: Interact with linked objects through the UI _(**[#690\_pal\_foundry\_d3\_ui\_.docx](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**)_
-	D4: Use Actions to change objects through the UI _(**[#689\_pal\_foundry\_d4\_actions\_.docx](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**)_
-	D5: Combine objects, AI, Actions, and human review _(**[#688\_pal\_foundry\_d5\_ai\_human\_.docx](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**)_
-	D6: Operate and govern the overall workflow _(**[#687\_pal\_foundry\_d6\_governance\_.docx](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**)_



_Foundry deep dive master diagram (ZAI original diagram verified by FDE)_<br><img src="/assets/DD_master_diagram.png" alt="drones" width="87%" style="border: 1px solid #999;">

<br><br><br>

---
---
---
---
------
---
---
---
---

<br>

# **ME: so now we have qs3 as the "bucket"**
for all remaining things (except LLMs and agents)..... what i am most interested in right now is a list of what possible subjects there would be.... i am thinking that these would lean heavily (but not restricted to) the FDE tools (apps, 65 total) that i have not used.


<br>

---

<br>

## My strongest candidates for the next few additions

**Contour, Quiver, Vertex, Notepad, and Jupyter** would introduce several new North experiences while reusing familiar data.

For new Equator/South mechanisms, I would choose **incremental processing, time series, media sets, database ingestion, and external writeback**.

**Not every subject needs its own app, and not every app deserves a separate tutorial.** This list gives us the capability inventory first; your approximately 65-app screenshot can then be checked against it to identify additional useful gaps without inventing exercises merely to cover icons.

<br><br>

**Yes—QS3 can introduce the remaining Foundry capabilities through small, mechanistic exercises, while QS4 handles models, LLMs, and agents.**

Below is a **candidate inventory**, not a required learning order. I have separated genuinely new subjects from extensions of things we already used. Availability still needs checking in your enrollment.

## New subjects to consider

| # | Subject / app | Small QS3 exercise |
|---:|---|---|
| **1** | **Contour — dataset analysis** | Filter, group, aggregate, and chart an existing dataset without creating an object type. |
| **2** | **Quiver — object analysis** | Analyze the existing Item objects, build a chart, and follow their Group relationships. |
| **3** | **Vertex — relationship exploration** | Build a graph of Items and Groups, expand connections, and investigate a selected relationship. |
| **4** | **Notepad — analytical reporting** | Create a short report combining explanatory text with supported analytical content. |
| **5** | **Notepad Templates** | Generate the same report structure for different selected objects. |
| **6** | **Code Workspaces / Jupyter** | Read a dataset, calculate statistics, and produce a plot in a notebook—without model training. |
| **7** | **Database ingestion** | Connect to a small Postgres database and sync a table into Foundry. Requires an accessible database. |
| **8** | **File/object-storage ingestion** | Import files from an approved storage source and process newly added files. |
| **9** | **Incremental transforms** | Add records and process only the new input instead of rebuilding everything. |
| **10** | **Streaming / change-data capture** | Observe incoming events or source-table changes arriving continuously. Requires a suitable source. |
| **11** | **Time-series data** | Associate timestamped readings with Items and inspect their history. |
| **12** | **Media sets** | Store images or documents and display them through object properties—without AI extraction. |
| **13** | **Many-to-many links** | Give Items multiple Tags and navigate in both directions. |
| **14** | **Relationship objects** | Represent an Item–Group assignment with its own date, status, or other properties. |
| **15** | **Ontology interfaces** | Give two different object types a shared interface and use that common structure. |
| **16** | **Code-based Functions** | Write a small Python or TypeScript function that calculates a result from selected objects. |
| **17** | **External writeback** | Submit an Action that updates MockAPI, then reimport the result. |
| **18** | **Object materialization** | Produce a dataset reflecting object state, including saved edits, for downstream analysis. |
| **19** | **Notifications** | Notify an assignee when an object enters a particular state. |
| **20** | **Data Health** | Configure a freshness or row-count monitor and inspect a failing result. |
| **21** | **Object edit history / Action logs** | Record and inspect who changed an object, what changed, and when. |
| **22** | **Restricted views** | Let two users see different permitted rows from the same underlying dataset. |
| **23** | **Property-level security** | Let both users see an object while restricting a sensitive property. |
| **24** | **Cipher** | Protect sensitive values or media using the controls supported in your environment. |
| **25** | **Process Mining** | Use a tiny event log to discover stages, waiting times, and repeated steps. |
| **26** | **OSDK / Developer Console** | Read objects from a minimal custom application rather than Workshop. |

## Extensions of capabilities already introduced

These are useful, but should not be presented as entirely new subjects.

| # | Subject / app | Small extension |
|---:|---|---|
| **27** | **Pipeline Builder** | Rebuild a small part of D1 visually and compare it with the Python implementation. |
| **28** | **Maps** | Add layers, configure markers, select objects geographically, and inspect time-dependent data. |
| **29** | **Workshop forms** | Create a guided entry form with required fields and validation. |
| **30** | **Workshop navigation** | Add pages, navigation, URL routing, and selected-object state. |
| **31** | **Workshop conditional behavior** | Show or hide sections and explicitly reset selections when inputs change. |
| **32** | **Workshop charts and aggregations** | Add a chart that filters another widget through selection. |
| **33** | **Dataset History / Compare / Time Travel** | Inspect two dataset versions and explain exactly what changed. |
| **34** | **Data Lineage versus Workflow Lineage** | Compare dataset dependencies with broader object, Action, function, and application dependencies. |
| **35** | **Resource Management / compute optimization** | Inspect one of our slow small-data builds and test an appropriate lightweight alternative. |
| **36** | **Marketplace** | Inspect installation inputs, outputs, versions, and upgrade changes before updating an example. |
| **37** | **Branch conflicts and recovery** | Make conflicting changes to one harmless UI field and resolve them deliberately. |
| **38** | **Permissions and access tracing** | Determine why a user can—or cannot—access a resource, including inherited permissions. |
| **39** | **Markings and propagation** | Apply a test marking and observe how it affects downstream data and access. |
| **40** | **Exports and downloads** | Compare exporting dataset rows, object data, and analytical results under applicable permissions. |



<br>

---

<br>


26.1125 (v1 26.1120)

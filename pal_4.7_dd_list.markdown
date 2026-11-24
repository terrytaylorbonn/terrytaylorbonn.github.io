---
layout: page
title: 4.7 DD master list (3.6)
permalink: /pal_3.6_target_apps/
---

<br>

#### **TOC**


- **A1 Office**
- **A2 Backend (EQUATOR)**
- **A3 Haystack needles**
- **A4a Inference (AI)**
- **A4b Training (AI)**
- **A5 Governance / security**
- **A6 Agentic (central loop)**


<br>

---------------

<br>

### **A1 Office**


|**Example** | **#** | **Specific problem for a ZAI_example** | **Potential inspiration** |
|--- | 5 | Combine incoming files whose columns have different names and formats | Schema matching and validation |
|--- | 8 | Put incoming tasks into a prioritized inbox and notify their assignees | Dynamic inbox and Action notifications |
|--- | 9 | Guide someone through submitting a complete record with attachments | Guided forms and questionnaires |
|--- | 10 | Investigate how two records are connected through intermediate relationships | Vertex Graph |
|--- | 11 | Generate a report for a selected record or investigation | Notepad Templates |
|--- | 13 | Approve a proposed change and send it back to an external system | Writeback-enabled decision support |
|--- | 14 | Compare a proposed change with the current situation before committing | What-if scenarios |



<br>

---------------

<br>


### **A2 Backend (ontology)**

```
- D1 basic #610bbb_pal_D1_foundry_original_
- D2 AIP #611www_pal_D2_aip_
- D3 automation #614_pal_agentic_ai_qs
- D4 functions #615_pal_onto_function_qs
- D6 basic #617_pal_D6_first_app_
- D7 basic #618_pal_D7_first_pipeline_

- DD19 #627_pal_DD19_transform_data_w_code_repos_
```

<br>

---------------

<br>


### **A3 Haystack needles**

```
- HN #620_pal_DIY9_aip-fde_demo_hn  #620_pal_9_aip-fde_demo_hn_
- D5 mining #616_pal_D5_biz_process_mining_qs
```

|**Example** | **#** | **Specific problem for a ZAI_example** | **Potential inspiration** |
|E11 | 1 | Find records occurring near the same place and time | Geospatial/common operating picture |
|E12 | 1 | (FAIL) E12: Build a common operating picture with geospatial data  |  |
|E17 | 12 | Show where and when a changing measurement exceeded a threshold | Time series on a map |


<br>

---------------

<br>


### **A4a Inference (AI)**



|**Example** | **#** | **Specific problem for a ZAI_example** | **Potential inspiration** |
|--- | 7 | Classify incoming records and send uncertain results for human review | AIP classification and feedback loops |
|--- | 4 | Search documents by meaning rather than exact words | Semantic search |
|E10 | 3 | Extract specified fields from PDFs and flag missing information | PDF parsing |
|E14 | --- |RAG |---|
|E15 | 6 | (FAIL) Find disagreements between a document and its accompanying image | Image/document cross-validation |
|E13 | --- |(TODO) Cipher visual obfuscation |---|





<br>

---------------

<br>


### **A4b Training (AI)**

|**Example** | **#** | **Specific problem for a ZAI_example** | **Potential inspiration** |
|E17 | 2 | (TRAIN) Detect unusual readings in timestamped measurements | Time-series anomaly detection |
| #619 | 15 | Predict a numeric result and compare predictions with actual outcomes | Supervised model training |

```
- D8 train model #619_pal_D8_model_integration_
```


<br>

---------------

<br>


### **A5 Governance / security**

```
- #628_pal_D1b_data_security_
```

<br>

---------------

<br>


### **A6 Agentic (central loop)**

<br>

#### **E18** chatbot studio


<br>

---------------------------------------
---------------------------------------
---------------------------------------

<br>

### **(4.2 Examples list)**

|**Example** | **description** |
|E10 | Parse PDFs with LLMs in Pipeline Builder | 
|E11 | Palantir Foundry example “Integrate GeoSpatial data with Gaia”  |  
|E12 | (FAIL) E12: Build a common operating picture with geospatial data |  
|E13 | (TODO) Protect sensitive images using visual obfuscation in Cipher |
|E14 | Evaluate Retrieval-Augmented Generation (RAG) methods |
|E15 | (FAIL) Cross-validate Images and Documents using AIP |  
|E17 | Detect anomalies in time series data with Code Workspaces |  
|E18 | E18_build_w_aip_chatbot_studio |


<br>

# **[LIST2 (T1-T6)](/pal_demo_list/)** (V1 26.1121)

- I created this list 4 months ago.
- This list has a hyper-linked TOC to all demos.
- They are organized by the PAL-defined Foundry user roles.
- I merely made much easier to search (and include in prompts to AI).


<br> 

------

<br>

26.1124 (v1 26.1123)


<!--
#### **Notes:**
- **2 Data protection (NONE)**. NONE = There are so far no specific demos for this functionality. But Data Protection is always there.
  - **MONITORING WITH AI ANALYSIS 26.1122**
- **3 AIP external (Agentic 1) (no automation; sovereignty risk via AI calls)**. You are using external LLMs. Processing occurs whenever data changes (there is no central loop running).
- **4 Automation (Agentic 2) (AI external; major sovereignty risk via automated AI calls)**. You have automation which watches for data changes and then invokes actions (and AI). Major sovereignty risks.
  - **D3b (TODO)** — Protecting agents that use external AI models (TODO)
- **5 ALPHA -- Mining (how frontier models steal your "alpha")**. This demo is primitive and uses black box Foundry functionality ("mining"), but Frontier model labs are certainly experts at such techniques.
  - **D5b (TODO)** (C5c): Demos for Maximize ALPHA/sovereignty / Data protectio (within performance/cost/complexity limitations)
- **6 AIP internal (Agentic 3)**. The best solution. Calls to AI are only to internal models. These demos show how to create and deploy your own model using Foundry.
  - **D3c (TODO)**
  - **D8a (TODO)**
- **L-1 LIST 1 (A1-A4)** 
- **L-2 [LIST2 (T1-T6)](/pal_demo_list/)**


- **DD-1 DIY (HN DIY9 + D8 (TRAIN))** 
- **[DD-2 D1-D7 (+DD19)](/3c.2_pal_initial_demos/)** 
- **[DD-3 D8 Train model (#619)](/pal_3.6_15_model_train/)**
- **[DD-4 Exx](/3c.1b_pal_examples/)** 

<br>

### **LIST 1 (A1-A6)** 

-->
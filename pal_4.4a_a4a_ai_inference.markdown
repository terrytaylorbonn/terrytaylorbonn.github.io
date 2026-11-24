---
layout: page
title: 4.4a AI inference
permalink: /pal_4.4a_a4a_ai_inference/
---

<br>

AI inference

#### **TOC**


|**Example** | **#** | **Specific problem for a ZAI_example** | **Potential inspiration** |
|--- | 7 | Classify incoming records and send uncertain results for human review | AIP classification and feedback loops |
|--- | 4 | Search documents by meaning rather than exact words | Semantic search |
|E10 | 3 | Extract specified fields from PDFs and flag missing information | PDF parsing |
|E14 | --- |RAG |---|
|E15 | 6 | (FAIL) Find disagreements between a document and its accompanying image | Image/document cross-validation |
|E13 | --- |(TODO) Cipher visual obfuscation |---|


<br>
<br>
<br>


### **900 No—AIPL/AIPLF is one route, not the only route.**

LLMs can be called through:
- **AIP Logic**
- **Pipeline transforms**, including Pipeline Builder and Python
- **Code-based Functions**
- **Agents/chatbots**
- **Built-in AI features**, such as AI FDE and AIP Assist

And **they are not limited to pipelines and UIs**. For example, an automation can trigger an Action that calls an LLM-backed function, without anyone using a UI.

For your diagram, think:

> **LLMs are model services that different Foundry workflows can invoke—not a mandatory AIPL → AIPLF → UI chain.**

ME: OK, so AIPL/code, in the UI via AIPLF or code, .....
FDE, AI assist.
thats about it.

<br>
<br>
<br>



#### **[E10: Parse PDFs with LLMs in Pipeline Builder (26.0727)](/3c.1b_pal_f_example_first/)**

- A very basic app that uses AI to summarize content of PDF files.<br>_E10 output_<br><img src="/assets/pal_10_23.png" alt="drones" width="85%" style="border: 1px solid #999;">
- Docx for this example: **[#621\_.docx](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**.

- **Example main diagram**. Shows the main workflow; red squares highlight those items implemented for demo D19 (this is a a very rought first draft that will change greatly as I figure out the details).<br>_(MAIN_E10.png)_<br><img src="/assets/MAIN_E10.png" alt="drones" width="74%" >

<!-- - Just data and pipeline, but also uses AI.<br>*E10*<br><img src="/assets/pal_10_22.png" alt="drones" width="33%" style="border: 1px solid #999;"> -->

<br>



#### **E14: Evaluate Retrieval-Augmented Generation (RAG) methods** (26.1014)

- #629
- https://ziptieai.usw-17.palantirfoundry.com/workspace/now/platform/7997a708-4d1e-4efb-bfca-882dc172b4e8
- _E14_<br><img src="/assets/pal_14_01.png" alt="drones" width="60%" style="border: 1px solid #999;">
- _E14_<br><img src="/assets/sun-19.png" alt="drones" width="60%" style="border: 1px solid #999;">

<br>


#### **E13: Protect sensitive images using visual obfuscation in Cipher**.

- no Docx??
- https://ziptieai.usw-17.palantirfoundry.com/workspace/now/platform/b88675ed-e8f9-4bc9-b75b-aa446930d07b
- _E13_<br><img src="/assets/pal_13_01.png" alt="drones" width="60%" style="border: 1px solid #999;">

<br>

# **4b List of failed/xxxx examples**

<br>




#### **xxxx FAIL ### E15: Cross-validate Images and Documents using AIP**.

- #624_pal_E15_cross_validate_images_docs_aip_v02_26.0730_ss
- https://ziptieai.usw-17.palantirfoundry.com/workspace/now/platform/e99a7898-6dc2-4394-a5ec-a583a2d87568
- _E15_<br><img src="/assets/pal_15_01.png" alt="drones" width="60%" style="border: 1px solid #999;">

<br>





<br> 

------

<br>

26.1124 (v1 26.1124)

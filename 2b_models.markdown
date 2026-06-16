---
layout: page
title: "2b Models"
permalink: /2b_models/
---

<br> 



<!-- *I spun off the content of this from page "NNs" on 26.0610 because I became convinced that creating custom models and deploying locally were going to be a big trend in the future. There is a lot of demo stuff on the Wiki that I need to move to this wepage or replicate.* -->

This **WIP** page (v1 26.0610) describes model internals. The agent and the NN are typically packed into a **model** that has an API that makes it possible for existing software to **use the model as a "helpful" assistant**. The internal agent (iAgent) that has been programmed to interact with the transformer (TF) via a very specific token-only protocol. The TF has also been trained to follow this protocol. 

*2b Models in the master diagram* <br>
<img src="/assets/M-15-2bx.png" alt="drones" width="80%">

*NOTE >>> (1) Tiny agentic AI model demo, (2) Backdoor in a model*

<!-- *Models in the AI ecosystem* <br>
<img src="/assets/zai_evolution7.png" alt="drones" width="42%"> -->
<!-- But this is extremely complex, not for small companies, so its not covered in ZAI. Palantir itself does not use custom models (too complex, and standard models have all that is required).-->

<br>

**TOC**

xxxxx

<br>


### **[2b.1 Model concepts](/2b.3.1-llm-gist/)**

 

<br>


### ([2b.1b 2025 demos](/2b.1b-2025-llm-demos/))

- See wiki page [**"AI LLM stacks"**](https://github.com/terrytaylorbonn/auxdrone/wiki/AI-stacks).


<br>

### **[2b.2 Tiny demos](/2b.3.6-llm-demos/)** (from 2b.6 LLM demos)

- 2b M01 Save .pt
- 2b M02 Inspect .pt
- 2b M03 Load .pt
- 2b M04 Inference
- 2b M05 Mismatch
- 2b M06 Hugging Face
- 2b M07 API Serving
- 2b M09 Protocol / Tool Use
- 2b M10 Trigger / Backdoor

<br>


### **[2b.2b Building models](/2b.2b-build-models/)**

<!-- I am still not sure if this belongs in 2 or 2b.. i am not sure what GPT means exactly by this. -->

For specific domains. How do I create a model for a specific purpose? Domain-specific models, Synthetic data, Custom TF, Custom CNN.

<br>

### **[2b.3 Modifying models](/2b.3-modify-models/)**

Modifying/customizing/fine-tune. LoRA, Adapters, Domain Specialization

<br>

### **[2b.4 Running models locally](/2b.4-run-models-locally/)**

This is actually one of the strongest sections because it matches your current interests exactly. HuggingFace, Ollama, Local Models, etc. How do I own and operate AI?

<br>

26.0613 (v1 26.0610)


<!-- 
<br>

----------------------
-------------------
------------------
---------------------

<br>


### **[3.2 Models](/2b_models/)** (with API)

The agent and the NN are typically packed into a **model** that has an API that makes it possible for existing software to **use the model as a "helpful" assistant**. I refer to the **code in the model that controls the TF NN as the "internal agent" (iAgent)**. This concept is central to understanding how models work. *Note: I invented the iAgent concept; GPT has only kind of accepted it as OK.*


<br>




## **2b.5 Use AI inside systems**

**i am not sure if parts of this belong in 3 agents**

This is the key section.
Because this is where your thinking has shifted recently.
Not:
How do I build AGI?
but:
How do I use AI as a tool?
Examples:


2.11 Model Deployment

2.11.1 Model Files
2.11.2 CPU vs GPU
2.11.3 Quantization
2.11.4 Local APIs
2.11.5 Model Serving
2.11.6 RAG Integration

<br>
-->


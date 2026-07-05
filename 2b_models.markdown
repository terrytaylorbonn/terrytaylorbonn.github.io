---
layout: page
title: "2b Models"
permalink: /2b_models/
---

<br> 

<!-- *I spun off the content of this from page "NNs" on 26.0610 because I became convinced that creating custom models and deploying locally were going to be a big trend in the future. There is a lot of demo stuff on the Wiki that I need to move to this wepage or replicate.* -->

This **WIP** page (v1 26.0610) describes model internals. The agent and the NN are typically packed into a **model** that has an API that makes it possible for existing software to **use the model as a "helpful" assistant**. The internal agent (iAgent) that has been programmed to interact with the transformer (TF) via a very specific token-only protocol. The TF has also been trained to follow this protocol. 

*[Eventually we all need to host our own models](https://www.youtube.com/watch?v=zMhz7JUvJZA&t=36s)*

<br>  

*2b Models in the master diagram* <br>
<img src="/assets/M-15-2bx.png" alt="drones" width="80%">

<br>  

### **[2b.1 Model concepts](/2b.3.1-llm-gist/)**

<br>

### ([2b.1b 2025 demos](/2b.1b-2025-llm-demos/))

- See wiki page [**"AI LLM stacks"**](https://github.com/terrytaylorbonn/auxdrone/wiki/AI-stacks).

<br>

### **[2b.2 Tiny demos](/2b.3.6-llm-demos/)** 

<!-- (from 2b.6 LLM demos) -->

- 2b.2.1 M01-M04 Define model, .pt load/save, run inference
- 2b.2.2 M05 Mismatch
- 2b.2.3 M06 Manual inference
- 2b.2.4 HF
- 2b.2.5 M07 API
- 2b.2.6 M08 Render (TODO)
- 2b.2.7 M09 Protocol / Tool Use
- 2b.2.8 M10 Trigger / Backdoor


<br>


### **[2b.2b Building models](/2b.2b-build-models/)**

<!-- I am still not sure if this belongs in 2 or 2b.. i am not sure what GPT means exactly by this. -->

```text2
For specific domains. How do I create a model for a specific purpose? 
Domain-specific models, Synthetic data, Custom TF, Custom CNN.  
Datasets, Synthetic Data, Model Evaluation.
```

<br>

### **[2b.3 Modifying models](/2b.3-modify-models/)**

Modifying/customizing/fine-tune. LoRA, Adapters, Domain Specialization

<br>

### **[2b.4 Operating models](/2b.4-run-models-locally/)**

```text2
I already have a model. How do I operate it?
Examples: HuggingFace, Ollama, GGUF, Gemma, Llama, Qwen, Mistral.
This is:
- Acquire
- Deploy
- Run
- Use

NOTE: 
HF is not necessarily local. For example: 
  HF download → local.
  HF hosted inference → remote.
  Ollama → local.
  Open-weight model on cloud VM → remote.
The common theme is really:
  How do I obtain and operate a model?
not necessarily:
  How do I run it locally?
```

<br>

26.0616 (v1 26.0610)


<!-- *NOTE >>> (1) Tiny agentic AI model demo, (2) Backdoor in a model*

 *Models in the AI ecosystem* <br>
<img src="/assets/zai_evolution7.png" alt="drones" width="42%"> -->
<!-- But this is extremely complex, not for small companies, so its not covered in ZAI. Palantir itself does not use custom models (too complex, and standard models have all that is required).-->

<!-- <br>

**TOC**

xxxxx
-->

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


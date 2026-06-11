---
layout: page
title: "2b Models"
permalink: /2b_models/
---

<br> 

This very **WIP** page (v1 26.0610) describes model internals. *I spun off the content of this from page "NNs" on 26.0610 because I became convinced that creating custom models and deploying locally were going to be a big trend in the future. There is a lot of demo stuff on the Wiki that I need to move to this wepage or replicate.*

<br>

*Models in the AI ecosystem* <br>
<img src="/assets/zai_evolution7.png" alt="drones" width="42%">

<br>

**TOC**

xxxxx

<br>

## **FROM PART 2**


### [2b.3.1 LLM gist](/2b.3.1-llm-gist/) (**NEED TO THIN OUT TF STUFF ??**)

### [2b.3.3 Agentic LLMs](/2b.3.3-agentic-llms/)

### [2b.3.6 LLM demos](/2b.3.6-llm-demos/)


### 2.3.5 LLM Internal Agent

The term "agent" normally means a deterministic (non-AI, not GPU-based) control loop that is the "caretaker" or interface between the LLM model and the outside world. However, there is also an agent (what I call an internal agent or "iAgent") in the LLM that is the interface between the transformer (TF) and the outside (of the LLM) world. Again, as with training, understanding this helps to understand the core nature of what an LLM and an agent is. An (external) agent is to some extent just an extension or a partner of the internal agent. 

<img src="/assets/iagent.png" alt="iagent" width="32%">


<br>


## **Part 3 BUILDING MODELS (for specific domain)**

**i am still not sure if this belongs in 2 or 2b.. i am not sure what GPT means exactly by this**

This is:
How do I create a model
for a specific purpose?
Examples:
Domain-specific models
Synthetic data
Custom TF
Custom CNN
This makes sense.


2.8.1 Datasets
2.8.2 Synthetic Data
2.8.3 Model Evaluation
2.8.4 Domain-Specific Models
2.8.5 Tiny Custom TF Demo
2.8.6 Tiny Custom CNN Demo

## **Part 4 MODIFYING EXISTING models (Modifying/customizing/fine-tune)**
This is:
I already have a model.
How do I change it?
contains:
2.9.1 Fine-Tuning
2.9.2 LoRA
2.9.3 Adapters
2.9.4 Domain Specialization
These are all about:
changing an existing model


## **Part 5 RUN LOCALLY**
This is actually one of the strongest sections because it matches your current interests exactly.
HuggingFace
Ollama
Local Models
This is:
How do I own and operate AI?
rather than:
How do I call OpenAI APIs?


2.10 Local Models

2.10.1 HuggingFace
2.10.2 Ollama
2.10.3 Gemma
2.10.4 Llama
2.10.5 Qwen
2.10.6 Mistral

## **Part 6 USE AI inside systems**

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


26.0611 (v1 26.0610)


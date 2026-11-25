---
layout: page
title: 3.5 QS4
permalink: /pal_qs4/
---

<br>

---------

<br>

# **945**


**Yes—your concern is justified. D1–D6 deepen the mechanics, but they do not yet deliver the breadth promised by “Broaden your Foundry skills.”** I assume “QS2” in question 1 means the current **QS3/D1–D6 series**.

## 1. What D1–D6 genuinely added

They are not redundant, but much of their value is **clearer understanding**, rather than entirely new capabilities.

| Module | Main addition beyond QS1 |
|---|---|
| **D1** | Cleaning, validation, rejected rows, joins, calculations, and enforced data-quality checks |
| **D2** | Two object types, explicit links, and navigation in both directions |
| **D3** | Selection-driven widgets, linked object sets, filtering, and aggregation |
| **D4** | Clear separation of dataset-backed values and saved object edits |
| **D5** | AI suggestions separated from human decisions and committed values |
| **D6** | Branch/proposal/merge workflow and a controlled two-user authorization test |

**Keep these as QS3’s foundation. Now add exercises that introduce genuinely different capabilities.**

Two wording corrections in your QS1 description:
- **Python scripts replace Pipeline Builder**, not “the pipeline”—Python transforms still form a pipeline.
- Our demonstrated Actions **modified existing objects**; they did not necessarily create new ones.

## 2. Recommended QS3 additions

I would prioritize the following—not another variation of the existing AI/Action chain.

| Proposed module | Small exercise | What is genuinely new |
|---|---|---|
| **D7: Analyze datasets and objects** | Answer a few questions over our existing data using **Contour**, then **Quiver** | North-side analysis beyond Workshop; dataset analysis versus object analysis |
| **D8: Add a different external source** | Import a small table from **Postgres**, if suitable infrastructure is available | A database connection and sync, rather than our custom MockAPI fetch |
| **D9: Train and use a small model** | Train a regression model on synthetic processing-job history; compare predicted and actual durations | Training, held-out evaluation, model versions, and inference |
| **D10: Run an open-weight model under controlled hosting** | Run a small extraction/classification task with a model hosted in an approved environment | Model hosting and integration—not merely selecting another AIP model |
| **D11: Build an interactive tool-using agent** | Ask an agent to find an Item and inspect its Group; examine the tool trace | Model-selected operations rather than a fixed AIPL sequence |
| **D12: Run the agent unattended** | Trigger the same task when work arrives; optionally extend it to a persistent worker | Event-driven agent execution and, separately, persistent hosting |

These are candidates; **D8, D10, and persistent hosting require an availability check before we commit to the tutorial**.

## 3. Clarify the two model topics

### “Local model”

We need to decide what **local** means:

- On your laptop?
- Hosted within your Foundry environment?
- Hosted on your own infrastructure and accessed from Foundry?

Those are different deployments. For QS3, I would initially target:

> **Run an open-weight model in an approved, controlled hosting environment and call it from Foundry.**

A separate Deep Dive can cover hardware, serving, scaling, and offline deployment.

### “Train an existing model”

There are also two distinct lessons:

- **Fit a standard model**, such as a tree-based regressor, to your dataset.
- **Fine-tune a pretrained model**, such as an image classifier or language model.

**Start with fitting a small regression model.** That teaches the complete training/evaluation/inference lifecycle without introducing the complexity of LLM fine-tuning. Fine-tuning can follow as a DD.

## 4. My suggested next move

**Start with model training**, because it most directly addresses your AI focus and adds a capability absent from QS1 and D1–D6. Use **#619** as a reference, but make the QS3 exercise smaller and explicitly bounded.

Then:
1. **North analysis tools**
2. **A different South source**
3. **Interactive agent**
4. **Unattended agent**
5. **Controlled model hosting**, once its prerequisites are established

Finally, remove the old **“This Deep Dive”** wording from the QS3 page. Its promise could be:

> **QS3 builds on QS0 and QS1, first making the core mechanisms explicit, then branching into new analysis tools, data sources, model training, and agent execution. Each capability is introduced through a small working exercise, with detailed extensions collected in the Deep Dives.**

**That makes D1–D6 the starting platform—not the full extent of QS3.**

<br>

---------

<br>

# **ME2: yes, qs2 meant qs3.** 

for internal LLM i meant inside Foundry. hosted there. 

i see the LLM inference, training, local, remote and various types of agents as a big deal. i like your ideas.  

one question: can we import a Huggingface model into Foundry?


## **FDE: Yes—Foundry supports importing Hugging Face model files and running the model inside Foundry.** 

That is different from calling Hugging Face’s hosted inference API.

### The basic path

**Hugging Face model files → Foundry storage → load in Python → run inference on Foundry compute**

The documented import options are:
- **Upload the model files as a raw-file dataset**, then load them from that dataset.
- **Download them from Python through explicitly configured network access** to Hugging Face. Foundry does not allow arbitrary internet access by default. :citation[Import a Hugging Face model / Hugging Face]{path="foundry/integrate-models/import-huggingface-models" section="Hugging Face"}

### Three separate milestones

| Milestone | What it means |
|---|---|
| **Import** | The weights, tokenizer, and configuration files are stored in Foundry |
| **Run** | Foundry compute loads the model and performs inference |
| **Serve/integrate** | Other workflows can invoke it through a defined model interface or service |

**Importing does not automatically put the model in AIP Logic’s model dropdown.** That integration is a separate step.

For an LLM, we must check **license, model compatibility, memory/GPU requirements, and the hosting capabilities available in your enrollment**.

### A good QS3 exercise

> **Import a small open-weight instruction model, run a prompt inside Foundry, and verify that inference uses the imported model.**

Start with **inference, not training or fine-tuning**. Once that works, expose it to another workflow; fine-tuning can follow as a separate exercise.

One documentation caveat: Palantir’s older **“Import an open source model”** functionality is deprecated, and its reference language-model adapters are no longer actively maintained. We should use a currently supported route rather than follow that old wizard. :citation[Import a Hugging Face model / Hugging Face]{path="foundry/integrate-models/import-huggingface-models" section="Hugging Face"}

**This is genuinely new coverage for QS3: bringing model weights into Foundry and executing them there—not merely choosing an existing AIP model.**


<br>

---------

<br>

# **ME3: maybe put models and agents in new qs4?**

## **FDE: Yes—that gives QS4 a clear identity and keeps QS3 manageable.**

### QS3: Broaden your Foundry skills
Keep **D1–D6** as its foundation, then add selected introductions to data sources and North analysis tools.

### QS4: Models and agents in Foundry
Build a connected series of small exercises:

1. **Use an existing AIP model**—establish the inference baseline.
2. **Import a Hugging Face model and run it inside Foundry.**
3. **Train a small predictive model** and compare predictions with actual outcomes.
4. **Create an interactive tool-using agent.**
5. **Trigger an agent automatically** when work arrives.
6. **Host a persistent worker agent**, if the environment supports it.

Treat **fine-tuning a pretrained model** as an optional extension, distinct from training the small predictive model.

**QS4 introduces the mechanisms step by step; section 4’s DDs explore them further.** The opening exercise should check hosting, compute, and access prerequisites so we know which paths your enrollment supports before committing to them.

<br>

-------------------------------

<br>

# **ME4: and qs4 would be based on qs3, or new?**

## **FDE: Build QS4 on QS3, but give it its own document and new resources.**

Reuse:
- **Demo2Item / Demo2Group objects and links**
- The familiar sample data
- **Demo3_LinkedViewer**, where a UI is useful

Create new **QS4-named models, agents, Functions, and Actions**, so experiments do not overwrite the working QS3 examples.

For model training, add a separate small dataset suited to prediction rather than force the existing seven records into a training exercise.

**Same familiar foundation, new capabilities—not another setup from scratch.** State the QS3 prerequisites at the start, with a short baseline check.


<br>

-------------------------------

<br>

26.1125 (v1 26.1125)

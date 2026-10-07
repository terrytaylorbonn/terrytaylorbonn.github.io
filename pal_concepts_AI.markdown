---
layout: page
title: pal_concepts_AI (26.0928)
permalink: /pal_concepts_AI/
---

<br>
<br>

- **3 AI (LLMs) is pattern recognition** (not intelligence) (pattern recognition that requires getting training data by any means necessary). **_I tried to add pics to this page wherever possible; intelligent beings like humans get far more from a single pic than from 1000 words (AI only crunches numbers, nothing more)_**.

TOC

- [1] (3.1) Real intelligence (human sensory organs and brain based)
- [2] (3.1a) How digital circuits (CPU) work (1) (2)
- [3] Basic AI detection (GPU) (3)
- [4] (3.1f) Complex detection (4)
- [5] (3.6) TF config (ASNN), structure, training
- [6] (3.5b) About those silly AGI diagrams

<br>
<br>

<!-- >
# **3 AI (LLMs) is pattern recognition**

AI (LLMs) = pattern recognition (not intelligence) that has an insatiable appetite for plagiarized training material.

- **3.1 Real intelligence (human sensory organs and brain based)**
- **3.1b LLM AI simulated intelligence (procedural agent + matrix math pattern classification)**
- **3.2 AI simulated intelligence (clocked state machine / pattern recog HACK)**
- **3.3 LLM (TF) delivers pattern recognition (and empty AGI promises)**
- **3.3b Complex pattern recognition**
- **3.4 (ext)Agent/LLM is the new app/OS paradigm**
- **3.5b About those silly AGI diagrams**
- **3.6 Training**
-->

<br>

---

---

---

<br>

# **[1] (3.1) Real intelligence (human sensory organs and brain based)**

The human

- (1) sees (or hears, touches (Braille)) words
- (2) generates thoughts from those words (thoughts exist only in time)
- (3) generates answer thoughts
- (4) converts those thoughts to words.

Its pretty simple, because the real magic is in the intelligent brain.

_The human brain (animal brains are the most fascinating thing in the universe; how they host intelligence is a mystery)_<br><img src="/assets/wuxi-53.png" alt="xxx" width="60%" style="border: 1px solid #999;"><br>

_Bio brain neurons (these have little in common with AI "NNs"; these are electro-chemical with interaction and crosstalk)_<br><img src="/assets/wuxi-60.png" alt="drones" width="26%" style="border: 1px solid #999;">

<br>

---

---

---

<br>

# **[2] (3.1a) How digital circuits (CPU) work (1) (2)**

<br>

---

---

---

<br>

# **[3] Basic AI detection (GPU) (3)**

<br>

---

<br>

### **AI COMPONENTS**

#### **3.4 The (ext)Agent/LLM is the new app/OS paradigm**

<!-- C2b) What is LLM / agent -->

**LLM = equivalent of OS**.

- The diagram below shows the internal stucture of an LLM.
- **Tranformer (TF) (GPU)** (The part of the LLM that makes it able to generate token sequences that mimic intelligent responses; NEEDS TRAINING INPUT)
  - 1 (main) **pattern matching** in "machine language" space
  - 2 **"thinking"** (and other **simulations** of intelligent thought)... these are also pattern matching.
  - 3 **language models** (Transformers; they convert inexact human representation of meaning (words) into massive amounts of numbers that are used to compute the exact "machine language" meaning)
- **Internal agent (iAgent) (CPU)**
  - procedural (CPU) code that runs the main loop and controls LLM input/output.
  - Very closely customized to TF.
  - feeds required prompts into TF and process responses.
  - responds to eAgent

The iAgent/TF

- are designed to work closely together (iAgent must be totally customized to the TF; iAgent will contain vast amounts of "glue" logic)
- need language and "thinking" patterns to simulate human thinking (_the outputs are far less predictable and reliable than procedural code_).

_LLM_<br><img src="/assets/wuxi-28.png" alt="xxx" width="45%" style="border: 1px solid #999;">

**(External) Agent = equivalent of the application (business logic)**.

- (ext)Agentic
  - = the non-human user of the AI (LLM) API.
  - procedural (CPU) code that your write that uses the LLM.
  - eAgent contains the end user central logic (business logic)
- extAgent can use AI in various modes:
  - **Chat, action, auto (reaction), action/auto**
  - **Single shot / loop**

_AI agent_<br><img src="/assets/wuxi-29.png" alt="xxx" width="25%" style="border: 1px solid #999;">

_(left) eAgent and LLM (iAgent + TF) on the PC and (right) in the enterprise_<br><img src="/assets/wuxi-47.png" alt="xxx" width="36%" style="border: 1px solid #999;"> <img src="/assets/wuxi-46.png" alt="xxx" width="46%" style="border: 1px solid #999;">

<br>

---

<br>

#### **3.1b LLM AI simulated intelligence (procedural agent + matrix math pattern classification)**

The general structure shown below:

<!-- > = eA//LLM = eA on OS // (iA on OS) + (TF on CUDA/GPU) -->

- eAgent = Agent code that you write (that interfaces with the LLM API).
- LLM = iAgent + TF.
- iAgent = Agent code written by Frontier model maker that controls TF.
- TF (transformer) = matrix math algorithms that classify patterns (based on training data) running on CPU (via CUDA).

_(external) agent + LLM are built on 100% pure digital computation components_<br><img src="/assets/wuxi-66.png" alt="xxx" width="41%" style="border: 1px solid #999;"><br>

_Matrix math network (not really "neural")_<br><img src="/assets/wuxi-61.png" alt="drones" width="36%" style="border: 1px solid #999;">

<br>

---

<br>

#### **3.1c HOW BASIC AI WORKS (3)**

<br>

---

<br>

#### **3.1d (3.2) TF WORKFLOW (SIMPLE/DETECT) // AI simulated intelligence (clocked state machine / pattern recog _[HACK](/0-demo/)_)**

**(1) LLM (TF) delivers pattern recognition (and empty AGI promises)**

You can compare LLMs to search engines on steroids. But the LLM does far more than just return search results.

- The LLM transformer (TF) computes the classification of the current prompt/response, and
- that classification is used to select the next token to add
- (this process is repeated until the TF or internal agent decide to stop).
- The LLM internal Agent orchestrates TF input to construct complex final responses.

There is no intelligence. Only pattern matching to classifications (tokens) that were "imprinted" on the LLM during "training" that used massive amounts of (often plagiarized) input token sequences (training text).

Therefore its only logical that the frontier models have the following main business goals:

- (1) You are dependent on (no sovereignty from) their model(s)
- (2) Their models can "steal" any intelligent business data (your ALPHA). And that is only logical, since the model sells you other people intelligence for a price.

**(2) TF workflow**

- (1) sees, hears, touches NOTHING.
- (2) binary data (representing prompt) is converted into numerical representations. For each token in GPT-3 that means 12K FP numbers (this is complex encoding/representation of the computed meaning, including context, vastly more info than just a few letters).
- (3) TF performs pattern match on all the machine language numbers (KEY CAPABILITY OF TF: vastly different letter inputs can end up with very closely matched machine language results)
- (4a) after many iterations the output is a CLASSIFICATION -- a set of probabilities for all tokens. Usually the token with highest probability is chosen as the output token (which is then appended to the input and then the cycle repeats) (the most probable token is not chosen when the LLM is programmed to trick the user with random output to give the impression of real intelligence rather than deterministic programming; LLMs are 100% deterministic in their computations)
- (4b) the cycle repeats until the the iAgent/TF determine that the answer is complete

_(hack-01) TF algorithm (GPT-3)_<br><img src="/assets/hack-01.png" alt="xxx" width="41%" style="border: 1px solid #999;"><br>

**(3) Classification possibilities:**

- ONLY about 50K (50K vocab tokens).
- this means determining next token based on machine_language_space pattern matching (many patterns match a single token... there are google's of patterns, but only 50K total classifications; so many patterns match a single classification).

**(4) AI has nothing, absolutely nothing, to do with real intelligence** _(see page [HACK](/0-demo/))_

- AI = clocked state machine. a snapshot in time means something.
- real intelligence (human, mouse, bird, etc): time based. like a flame. it has no fixed state.
- we understand context: QKV makes meaning pattern matching possible. classification becomes next token.
- LLM spits out best classification which becomes the next token.
- The classification concept of AI can be used in many areas. For example
  - FSD (full self driving) has many inputs which are used to select a set of outputs (used to drive the car)
  - Object Recognition classification (dog or cat)

<br>

---

<br>

#### **3.1e EXAMPLE**

<br>

---

---

---

<br>

# **[4] (3.1f) Complex detection (4)**

<br>

---

<br>

#### **3.3b Complex pattern recognition**

LLM "thinking" is in reality complex pattern recognition and classification (I am not 100% sure about this, but its the only way an LLM could do this magic trick). The training complicated and a very closely held secret.

First consider Simple classification responses:

- CNNs:
  - Input = Pixel color values
  - Output = Image classification
- LLMs:
  - Input = Words/Tokens (ASCII) for prompt + running_answer
  - Output = new token (add to input for next loop)

Then complex patttern recognition:

- LLM JSON formatting of inputs/responses
- LLM Complex responses (hierarchical, layered)
  - "thinking" (trained into LLM; iAgent programmed to build)
  - requires complex training (I have no idea how this is done)

<br>

---

---

---

<br>

# **[5] (3.6) TF config (ASNN), structure, training**

(need to add more detail to this section... TODO)

Training is a very complicated topic.

- Basically input tokens as shown below and adjust parameters in the LLM TF slightly for each training pass.
- On each pass the error is computed (loss). This determines how to adjust params.
- Diagram below shows how multiple inputs are used to compute multiple outputs simultaneously.
- Complex LLM inference functions (like "thinking", JSON-based spec of LLM outputs, etc) require very special training techniques (that are undoubtedly tightly held secrets; I do not have any concrete ideas yet about how exactly this is done, but seems to me that the internal Agent programming and TF training must be closely sync'd to make it work).

NOTE: During inference (runtime, not training) if you input only token0 and token1, then the output of the TF would be token3. That token3 would be added to the running prompt+answer, and then fed back into the TF (at least thats the most basic version of what a TF does).

_Basic training._<br><img src="/assets/wuxi-67.png" alt="xxx" width="32%" style="border: 1px solid #999;">

<br>

---

---

---

<br>

# **[6] (3.5b) About those silly AGI diagrams**

_This diagram is absolute nonsense, comparing AI to brain functions (it only confuses me; this diagram appeared in the blog "BestPartner", one of my favorite blogs)._<br><img src="/assets/wuxi-64.png" alt="xxx" width="70%" style="border: 1px solid #999;">

_This is a sanitized version without the AGI hype._<br><img src="/assets/wuxi-65.png" alt="xxx" width="45%" style="border: 1px solid #999;">

<br>

---

<br>

26.0928 (v1 26.0804)

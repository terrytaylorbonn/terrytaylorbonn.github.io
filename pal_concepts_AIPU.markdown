---
layout: page
title: Core LLM concepts (26.1005)
permalink: /pal_concepts_AIPU/
---

<br>

[← Core Foundry Enterprise AI Concepts](/pal_concepts/)

<br>

<!-- until you have an anchor in the basic tech, you can be blown around in the wind by any ai hype/lies -->

This is a new version of core LLM concepts (26.0929 V1). I rewrote this during my 5 weeks of "vacation" in Wuxi (China; I was not online at any time). This page focuses on

- **AI hype and scams** (especially from top AI gurus). Claiming that AI could possible be more intelligent than the human brain is a ruse. A scam. If you base business decisions on such claims, it will cost you.
- **The reality of AI**
  - AI has **no (0) intelligence (you can not possibly reach AGI by scaling from 0**)
  - AI is an incredible revolutionary tech that is changing our world (and **making very successful those who understand what AI really is and how to use it**)
  - **Code snippets** from the **[TINY TF DEMO](/2.3.6.1-d5-tiny-tf/)**. **To understand AI you have to understand the algorithms, which means understanding (basic) code**. The TINY TF DEMO (Python) is the simplest test LLM you can run on your own PC with/without GPU that is referenced in the ZAI webpages that discuss concepts (see also **[2.3.6.1b-d5-tiny-tf-algorithm-details](/2.3.6.1b-d5-tiny-tf-algorithm-details/)**).

See also

- **[LOOK MOM! NO WIRES! (the end of the AI/AGI con game)](/pal_concepts_AIPU_no_wires/)**. This page is an overview of all the ZiptieAI pages that talk about the reality of AI/AGI.

<br>

**TOC**

- **Part 1** AI reality check.
  - **[n0] AI does not have one iota of intelligence.** Compares the human brain (real (bio) NN based), digital computer operating systems (CPU based), and LLMs (iAgent must run on a CPU; TF can run on GPU/CPU). **LLMs have everything in common with digital OS's** and **virtually nothing in common with the human brain**. <!--  -->
- **Part 2** How the brain, OS, and LLM work (the goal is to show that the LLM is similar to the OS, not the brain)
  - **[n1] How a (bio) brain works** (non-intelligent low level; intelligent high level thinking)
  - **[n2] How an OS works** (Kernel, CPU, memory, I/O, etc).
  - **[n3] How an LLM works** (TF/iAgent on OS). **Mirror n3 OS wherever possible**.
- **Part 3** Model (LLM) basics (with **[TINY TF DEMO](/2.3.6.1-d5-tiny-tf/)** (character-level next-token prediction))
  - **[n3b] Python libraries** (simplify greatly creating your own TF)
  - **[n3c] DEVICE specification (GPU or CPU)**
  - **[n4] TF definition** (100% SW-defined (ASNN) (within limits of HW)) // iA defines AS-AIPU // (ASNN) (3)
  - **[n4b] TF (model) to device**
  - **[n5] TF (model) training** (AS-AIPU (2, 3b))
  - **[n5b] iA hard coded test prompt** (4) (inputs LLM tokens, not opcodes; mem)
- **Part 4** (TODO) Real LLM with HF (build locally, publish, deploy) (see **[2b.2 Tiny model demos](/2b.3.6-llm-demos/)** and **608.docx** (can access when return to HK)).
  - **[n6] Build (add iA API)**. iA offers API, just like OS/Kernel to proc apps. Provides the API for the eAgent.
  - **[n7] Publish (HF)**. Packaged into a unit, provided on HuggingFace or elsewhere for download.
  - **[n8] Deploy (locally, Ollama)**
- **Part 5** (TODO) Real LLM with PAL Foundry (you can build/deploy within Foundry) (see **[2.2b ZAI versions of the core ~8 Foundry getting started demos](/3c.2_pal_initial_demos/)** section "(7) D8a (WIP) — Deep Dive: Model integration (26.0905))".

<!-- - **Part 4** SUMMARY
  - **[n7] LOOK MOM! NO WIRES! End of the AGI con game**. Puts "the nail in the coffin" of the crazy idea that AI has anything remotely approaching human intelligence. -->

<br>

---

---

---

---

---

<br>

# **Part 1** AI reality check

<br>

---

---

---

<br>

### **[n0] AI does not have one iota of intelligence**

While in China I noticed a lot of battery powered cars. The success of the local brands was undoubtedly made possible in great part by Musk's decision to transfer core electric car / FSD (full self driving) tech and train a new generation of engineers by building a local factory. Musk did this just to make a few pennies (what Tesla made is China is pennies for the richest man (on paper) in the world).

**What struck me the most in China was the realistic appraisal of FSD by Chinese drivers ("trust FSD to drive my car? Never!").These people were not stupid.** I am not so sure about those who have been listening to Musk's empty promises about FSD for the past 10 years but still believe Musk's every AI prediction (his most recent claim that AI would reach AGI in a year was a doozy).. Claiming that AI could possible be more intelligent than the human brain is a ruse. A scam. Choosing to trust such claims is choosing badly. It will cost you.

_An unsuccessful application of AI (from ZAI page **[HACK](/0-demo/)** section "7 The very bright future of simulated intelligence"). The riders in the car chose to trust AI; they chose badly._<br>
<img src="/assets/waymo.png" alt="drones" width="26%">

**Battery powered cars have 2 kinds of AI**

- **AI navigation systems (if the AI fails, no problem)**. These systems are a godsend. They totally changed life behind the wheel. Communicating with the NAV system by voice.
- **FSD (if the AI fails, disaster)**. During all that time in Wuxi, no one, not a single FSD car driver, dared to let their car drive itself.

**The AI NAV systems understand what you say thanks to the transformer (TF) ALGORITHM which was invented in 2017.** After 10 years it is still the backbone algorithm of AI LLMs. It is only an algorithm. Comparing this algorithm to the human brain is lunacy.

**These are the core functions of a TF:**

- Input tokens (parts of words; original prompt + running response), perform massive brute force calcuations on the input tokens to get the next token. Add this next token to the running prompt + response, and repeat again.
- Inside the TF
  - Convert the ASCII code for each token to 12288 large numbers (GPT-3). This is the "machine language" version of the token that the TF works with.
  - Modify the machine language of each token by
    - Compute (QKV, "attention") the contextual meaning of each token based on the machine language of all other tokens.
    - Use NNs to detect meanings in each token ("FFN").
  - Store the detections into a "storyline" (classification) of entire prompt+response.
- No thoughts, no concepts. Nothing. Just pattern recognition.

<br>

---

---

---

---

---

<br>

# **Part 2** How the brain, OS, and LLM work

<br>

---

---

---

<br>

### **[n1] How a (biological) brain works**

<br>

TOC

- **n1.1 Brain ecosystem**
- **n1.2 Brain internals**
- **n1.3 Brain functionality: Basic / not intelligent (subconscious; instinctive reactions, body control, etc)**
- **n1.4 Brain functionality: Advanced / intelligent (consciousness, thinking, etc)**

<br>

---

<br>

#### **n1.1 Brain ecosystem**

_The human brain ecosystem (need to add sense organs, muscles, etc)_<br><img src="/assets/wuxi-53bbb.png" alt="xxx" width="60%" style="border: 1px solid #999;"><br>

<br>

---

<br>

#### **n1.2 Brain internals**

_The human brain (animal brains are the most fascinating thing in the universe; how they host intelligence is a mystery)_<br><img src="/assets/wuxi-53.png" alt="xxx" width="40%" style="border: 1px solid #999;"><br>

- The interaction between brain neurons is vastly more complex than for the crude matrix math in AI (AI is vastly more complex in MORE OBVIOUS HIGHER LEVEL ANALYSIS, because at its core it is simply a crude "mechanical" device; the simulation requires vast and vastly complex binary infrastructure
- but what is happening in the brain neurons is at its core not crude binary... it is a symphony orchestra, playing out the greatest songs in the universe)

_Bio brain neurons (these have little in common with AI "NNs"; these are electro-chemical with interaction and crosstalk)_<br><img src="/assets/wuxi-60.png" alt="drones" width="26%" style="border: 1px solid #999;">

<br>

---

<br>

#### **n1.3 Brain functionality: Basic / not intelligent (subconscious; instinctive reactions, body control, etc)**

**the lower level bio NN's formed the future basis for more complex structures that HOST intelligence and consciousness**

This is probably the closest to bio intelligence that AI can come to. In fact, I have suggested at times that AI be renamed to "Artificial Instinct", meaning that AI computation is much closer to instinctive neural reations in the animal world (not to higher-level thinking). See page **[Hack](/0-demo/)** section "3b The TF provides artificial instinct, not intelligence".

_If any linear object moves like a worm, then strike (otherwise ignore)_<br><img src="/assets/toad.png" alt="drones" width="24%" style="border: 1px solid #999;">

<br>

---

<br>

#### **n1.4 Brain functionality: Advanced / intelligent (consciousness, thinking, etc)**

**to understand how this is a function of brain mass and energy, note what happens where you take any kind of drug that lessens brain bio function signals... the consciousness diminishes... this is not a binary system, it is much more complicated... it is a system that hosts something**

The human

- (1) sees (or hears, touches (Braille)) words
- (2) generates thoughts from those words (thoughts exist only in time)
- (3) generates answer thoughts
- (4) converts those thoughts to words.

Its all a mystery, true magic, the most fascinating thing in the universe: Consciousness and intelligence, hosted by the human brain.

_How the human brain hosts consciousness and intelligence is a mystery._<br><img src="/assets/wuxi-73ccc.png" alt="drones" width="33%" style="border: 1px solid #999;">

<br>

---

---

---

<br>

### **[n2] How an OS works**

<br>

TOC

- **n2.1 OS ecosystem**
- **n2.2 OS internals**
- **n2.3 OS functionality: Basic (binary operations, compute, etc)**
- **n2.4 OS functionality: Advanced (interrupts, subroutines, multiprocessing, etc)**

<br>

---

<br>

#### **n2.1 OS ecosystem**

Add screen, KB, mouse, etc.

_The OS is the complete computing unit, like the brain or LLM._<br><img src="/assets/wuxi-73.png" alt="drones" width="32%" style="border: 1px solid #999;">

<br>

---

<br>

#### **n2.2 OS internals**

_The OS contains SW and FW (firmware) that runs on the CPU._<br><img src="/assets/wuxi-73bbb.png" alt="drones" width="10%" style="border: 1px solid #999;">

_CPU internals (need to add about OS, kernel, more about CPU... ask GPT)_<br><img src="/assets/wuxi-80.png" alt="drones" width="33%" style="border: 1px solid #999;">

<br>

---

<br>

#### **n2.3 OS functionality: Basic (binary operations, compute, etc)**

<br>

---

<br>

#### **n2.4 OS functionality: Advanced (interrupts, subroutines, multiprocessing, etc)**

_Branching logic; the complex advanced responses of the OS are based on some very basic techiques (there is not real multiprocesssing; like AI its simulated)._<br><img src="/assets/wuxi-74.png" alt="drones" width="23%" style="border: 1px solid #999;">

<br>

---

---

---

<br>

### **[n3] How an LLM works**

LLM = internal Agent (iAgent) + transformer (TF) that work in together to create output tokens from inputs tokens.

- iAgent must be totally customized to the TF; iAgent will contain vast amounts of "glue" logic
- TF = (language models, pattern recognition). the internal representation of a token in GPT3 is 12288 16bit numbers (provides the depth required to calculate the most probable output token).
- automated programming (training). programmed to classify a vast number of inputs. need language and "thinking" patterns to simulate human thinking
- inference = runtime. during inference, inputs that dont exactly match any training inputs will still be classified accurately (classification determines the probability for all the possible output tokens; one is chosen to be the next token).

See also

- _[HACK](/0-demo/)_. Describes the gist of the LLM. Includes the following diagram.<br>
  _The LLM "artificial intelligence" hack. The iAgent and TF are the dynamic duo that make it all possible._<br>
  <img src="/assets/M-11b.png" alt="drones" width="27%"><br>

<!-- - CNNs:
  - Input = Pixel color values
  - Output = Image classification -->

<br>

TOC

- **n3.1 LLM ecosystem**
- **n3.2 LLM internals (iAgent / TF-(language models, pattern recognition))**
- **n3.3 LLM functionality: Basic prompt/response**
- **n3.4 LLM functionality: Complex ("thinking", "reasoning", etc)**

<br>

---

<br>

#### **n3.1 LLM ecosystem**

Includes LLM (with OS base), eAgent. Add tools, etc.

_AIPU (LLM) ecosystem (the "black box" view, for example when you access remote LLM via API)_<br><img src="/assets/wuxi-77bbb.png" alt="xxx" width="35%" style="border: 1px solid #999;">

_(left) eAgent and LLM (iAgent + TF) on the PC and (right) in the enterprise_<br><img src="/assets/wuxi-47.png" alt="xxx" width="36%" style="border: 1px solid #999;"> <img src="/assets/wuxi-46.png" alt="xxx" width="46%" style="border: 1px solid #999;">

<!-- #### **>>>>>>>>3.4 The (ext)Agent/LLM is the new app/OS paradigm**
(C2b) What is LLM / agent
**LLM = equivalent of OS**.
- The diagram below shows the internal stucture of an LLM. -->
<!-- _LLM_<br><img src="/assets/wuxi-28.png" alt="xxx" width="45%" style="border: 1px solid #999;"> --
**3.1b LLM AI simulated intelligence (procedural agent + matrix math pattern classification)**
The general structure shown below:
<!-- > = eA//LLM = eA on OS // (iA on OS) + (TF on CUDA/GPU) -->
<!-- - LLM = iAgent + TF.
- iAgent = Agent code written by Frontier model maker that controls TF.
- TF (transformer) = matrix math algorithms that classify patterns (based on training data) running on CPU (via CUDA).
#### **3.1e EXAMPLE** -->

<br>

---

<br>

#### **n3.2 LLM internals (OS, CUDA, TF (GPU/CPU), iAgent)**

This section mirrors closely section n2.2 (OS internals. Not section n1.2 (brain internals).

_LLM internals (here is the OS and CUDA are shown separately; this is usually how the LLM is viewed when it is run locally (and the LLM was downloaded from a site such as HuggingFace)_<br><img src="/assets/wuxi-77.png" alt="xxx" width="50%" style="border: 1px solid #999;">

_Another view; the idea here is that the LLM is running within an app like Ollama that takes care of all of the complexity of running an LLM locally (just as the Python torch libraries vastly simplify running code for the **[TINY TF DEMO](/2.3.6.1-d5-tiny-tf/)**))_<br><img src="/assets/wuxi-66bbb.png" alt="xxx" width="27%" style="border: 1px solid #999;"><br><br>

- **n3.2.5 OS**. The internal Agent (iAgent) (typically Python) runs on a CPU.<br><br>
- **n3.2.4 CUDA**. SW that takes the NN definition file (that defines the structure and weights/biases of the TF) and creates the actual code that runs on the 100% deterministic binary state machine which can be
  - GPU OR
  - CPU (this is only practical with current tech for smaller models).<br><br>
- **n3.2.1 TRANSFORMER (TF) (GPU)** (for details see ZAI page \*\*[HACK](/0-demo/)). The part of the LLM that makes it able to generate token sequences that mimic intelligent responses; NEEDS TRAINING INPUT. TF (transformer) = matrix math algorithms that classify patterns (based on training data) running on CPU (via CUDA). TF main functionality.
  - Input = Words/Tokens (ASCII) for prompt + running_answer
  - Output = new token (add to input for next loop)
  - The TF Language model converts the inexact binary data (representing prompt) into numerical representations. For each token in GPT-3 that means 12K FP16 numbers (this is complex encoding/representation of the computed meaning, including context, vastly more info than just a few letters).
  - TF performs pattern match on all the machine language numbers (vastly different letter inputs can end up with very closely matched machine language results)
  - GPT-3 has 50K tokens, 12288 FP16/token, 2048 token window (max input size). that means (2048 \* 12288 ) ^^ 50K (something like that) possible patterns. far more than 10^^79 atoms in the universe.
  - TF ensures that similar meanings are located in the same vector space (vector space must not depend on nominal token value, but their contextual menaing (requires attention heads)).<br>_TF. Note the similarity with the CPU in section "n2.2 OS internals". The URL of this page probably contains the acronym "AIPU" (AI processing unit; AI version of CPU). This because originally this page was going to focus on AIPU ("NN") similarity with CPUs (they have nothing in common with real bio NNs)._<br><img src="/assets/wuxi-81.png" alt="drones" width="45%" style="border: 1px solid #999;"><br>_NOTE: TF is a computational state algorithm. The exact algorithm is specified by the TF weights/bias (SW based, not fixed as with CPU). The state of the machine changes with each clock pulse._<br><img src="/assets/wuxi-61.png" alt="drones" width="33%" style="border: 1px solid #999;"><br><br>
- **n3.2.2 Internal agent (iAgent) (CPU)**
  - procedural (CPU) code that runs the main loop and controls LLM input/output.
  - Very closely customized to TF.
  - feeds required prompts into TF and process responses.
  - responds to eAgent

<!-- do not have to define all combos (for CPU circuits must define)
  - great for recog
  - but not useable for iagent
  - brainstem is (iA) reliable agent
  - (but hihg level thought is separate)
  - keep heart beating, etc
  - TF is for "high" level -->

<br>

---

<br>

#### **n3.3 LLM functionality: Basic token generation**

- prompt converted to machine language
- context computation (language model)
- matching the machine language representation in vector space
- prompt/response

<br>

---

<br>

#### **n3.4 LLM functionality: Complex ("thinking", "reasoning", etc)**

- 2 **"thinking"** (and other **simulations** of intelligent thought)... these are also pattern matching.

AI has nothing, absolutely nothing, to do with real intelligence _(see page [HACK](/0-demo/))_.

LLM "thinking" is in reality complex pattern recognition and classification (I am not 100% sure about this, but its the only way an LLM could do this magic trick). The training complicated and a very closely held secret.

- LLM JSON formatting of inputs/responses
- LLM Complex responses (hierarchical, layered)
  - "thinking" (trained into LLM; iAgent programmed to build)
  - requires complex training (I have no idea how this is done)

<!-- Therefore its only logical that the frontier models have the following main business goals:

- (1) You are dependent on (no sovereignty from) their model(s)
- (2) Their models can "steal" any intelligent business data (your ALPHA). And that is only logical, since the model sells you other people intelligence for a price. -->

<br>

---

---

---

---

---

<br>

# **Part 3** Model (LLM) basics (with TINY TF DEMO)

<br>

---

---

---

<br>

### **[n3b] Python libraries (simplify greatly creating your own TF)**

**[TINY DEMO PAGE](/2.3.6.1-d5-tiny-tf/)**

<!-- Vars
text = "hello world hello world hello world "
chars = sorted(list(set(text)))
vocab_size = len(chars)
stoi = {ch: i for i, ch in enumerate(chars)}
itos = {i: ch for ch, i in stoi.items()}
data = torch.tensor([stoi[ch] for ch in text], dtype=torch.long).to(device)
block_size = 8
embed_dim = 16
num_epochs = 1000
-->

```
# d5_tiny_transformer_chars.py

import math
import torch
import torch.nn as nn
import torch.nn.functional as F
```

<br>

---

---

---

<br>

### **[n3c] DEVICE specification (can be GPU or CPU)**

NOTE that the only reason a GPU is required is because of speed. **You could also run these algorithms on electromechanical relays and get the same outputs**.

_The first line of code below makes a mockery of the claims that AI is based on NNs. It shows that the algorithms can run just fine on a CPU, which of course it can, because AI TF is based on matrix math (running on clocked binary state machines)._

```
device = "cuda" if torch.cuda.is_available() else "cpu"
print("device:", device)
```

_Matrix math network (not really "neural")_<br><img src="/assets/wuxi-61.png" alt="drones" width="36%" style="border: 1px solid #999;">

<br>

---

---

---

<br>

### **[n4] DEFINE TF /// (100% SW-defined within limits of HW)**

THe AIPU is like a SW-define ASIC (application specific IC). Unlike a CPU, the AIPU is SW-defined

- STRUCTURE (100% within HW Limits) and
- OPCODES (program the NN)

The page **[2.3.6.1b D5 tiny TF algorithm details](/2.3.6.1b-d5-tiny-tf-algorithm-details/)** analyzes the TINY DEMO in detail (original ZAI material).

_2.3.6.1b-forward.png_<br><img src="/assets/2.3.6.1b-forward.png" alt="xxx" width="44%" style="border: 1px solid #999;">

Below

- def **init**(self) defines the (SW-defined) TF components that are used in the forward pass
  - Token and position embeddings
  - QKV (context ("attention) computation)
  - FFN "feed forward network" (a meaningless name for what is essentially a feature detection algorithm)
  - output generation (probabilities of each token as output)
- def forward(self, idx):
  - the actual (SW-defined)forward flow thrpough the TF components (the interconnections)

Note that although "SW-defined", the actual computations occur on the

- GPU
- CPU (if no GPU)

These Python libraries hide a lot of complexity so that you dont have to implement all of the details.

```
# text = "hello world hello world hello world "
# chars = sorted(list(set(text)))
# vocab_size = len(chars)
# embed_dim = 16

class TinyTransformer(nn.Module):
    def __init__(self):
        super().__init__()
        self.token_embed = nn.Embedding(vocab_size, embed_dim)
        self.pos_embed = nn.Embedding(block_size, embed_dim)
        self.q = nn.Linear(embed_dim, embed_dim)
        self.k = nn.Linear(embed_dim, embed_dim)
        self.v = nn.Linear(embed_dim, embed_dim)
        self.ffn = nn.Sequential(
            nn.Linear(embed_dim, 64),
            nn.ReLU(),
            nn.Linear(64, embed_dim),
        )
        self.out = nn.Linear(embed_dim, vocab_size)

    def forward(self, idx):
        B, T = idx.shape
        token_vecs = self.token_embed(idx)
        positions = torch.arange(T, device=device)
        pos_vecs = self.pos_embed(positions)
        x = token_vecs + pos_vecs
        Q = self.q(x)
        K = self.k(x)
        V = self.v(x)
        scores = Q @ K.transpose(-2, -1)
        scores = scores / math.sqrt(embed_dim)
        mask = torch.tril(torch.ones(T, T, device=device))
        scores = scores.masked_fill(mask == 0, float("-inf"))
        weights = F.softmax(scores, dim=-1)
        context = weights @ V
        x = x + context
        x = x + self.ffn(x)
        logits = self.out(x)
        return logits
```

<br>

---

---

---

<br>

### **[n4b] model to device**

**(2) CUDA control**

```
model = TinyTransformer().to(device)
```

_76_<br><img src="/assets/wuxi-76.png" alt="xxx" width="44%" style="border: 1px solid #999;">

<br>

---

---

---

<br>

### **[n5] Training LLM TF**

- Training is black magic
- Training is basic programming "Application specific NN""
- Can train higher level workflows ("thinking", etc)

Training is a very complicated topic.

- Basically input tokens as shown below and adjust parameters in the LLM TF slightly for each training pass.
- On each pass the error is computed (loss). This determines how to adjust params.
- Diagram below shows how multiple inputs are used to compute multiple outputs simultaneously.
- Complex LLM inference functions (like "thinking", JSON-based spec of LLM outputs, etc) require very special training techniques (that are undoubtedly tightly held secrets; I do not have any concrete ideas yet about how exactly this is done, but seems to me that the internal Agent programming and TF training must be closely sync'd to make it work).
- NOTE: During inference (runtime, not training) if you input only token0 and token1, then the output of the TF would be token3. That token3 would be added to the running prompt+answer, and then fed back into the TF (at least thats the most basic version of what a TF does).

_Basic training._<br><img src="/assets/wuxi-67.png" alt="xxx" width="32%" style="border: 1px solid #999;">

**The following shows training code for Tiny Demo.**

```
# text = "hello world hello world hello world "
# chars = sorted(list(set(text)))
# stoi = {ch: i for i, ch in enumerate(chars)}
# data = torch.tensor([stoi[ch] for ch in text], dtype=torch.long).to(device)
# block_size = 8
# embed_dim = 16
# num_epochs = 1000

def get_batch():
    ix = torch.randint(0, len(data) - block_size - 1, (16,), device=device)
    X = torch.stack([data[i:i + block_size] for i in ix])
    Y = torch.stack([data[i + 1:i + block_size + 1] for i in ix])
    return X, Y

loss_fn = nn.CrossEntropyLoss()
optimizer = torch.optim.Adam(model.parameters(), lr=0.01)

for epoch in range(num_epochs):
    X, Y = get_batch()
    logits = model(X)
    B, T, C = logits.shape
    loss = loss_fn(
        logits.reshape(B * T, C),
        Y.reshape(B * T),
    )
    optimizer.zero_grad()
    loss.backward()
    optimizer.step()
    if epoch % 100 == 0:
        print(f"epoch={epoch} loss={loss.item():.6f}")
```

<br>

---

---

---

<br>

### **[n5b] iA hard coded test prompt/result**

```
# text = "hello world hello world hello world "
# chars = sorted(list(set(text)))
# stoi = {ch: i for i, ch in enumerate(chars)}
# itos = {i: ch for ch, i in stoi.items()}


# generate text
model.eval()
idx = torch.tensor([[stoi["h"]]], dtype=torch.long).to(device)
with torch.no_grad():
    for _ in range(40):
        idx_cond = idx[:, -block_size:]
        logits = model(idx_cond)
        last_logits = logits[:, -1, :]
        probs = F.softmax(last_logits, dim=-1)
        next_id = torch.multinomial(probs, num_samples=1)
        idx = torch.cat([idx, next_id], dim=1)
generated = "".join(itos[i] for i in idx[0].tolist())
print("generated:")
print(generated)
```

_Where code is executed in the tiny test (internal Agent or Transformer). A real LLM test would include code on the external Agent (that your write) that calls the iAgent API. For details see **[2.3.6.1b-d5-tiny-tf-algorithm-details](/2.3.6.1b-d5-tiny-tf-algorithm-details/)**_<br><img src="/assets/wuxi-78.png" alt="xxx" width="100%" style="border: 1px solid #999;">

#### **FINAL RESULT**

**(WIP)**

In D5 (diagram below):

- Loop 1
  - Input the letter "h" (T1).
  - Infer. Result = "e".
- Loop 2
  - Input the letters "h", "e" (T1,T2).
  - Infer. Result = "l".
- ......
- Loop 8
  - Input the letters "h", "e", "l", "l", "o", " ", "w", "o", (T1...T8).
  - Infer. Result = "r".
- Loop 9
  - Input the letters "e", "l", "l", "o", " ", "w", "o", "r" (T1...T8).
  - ............

<img src="/assets/M-09.png" alt="drones" width="70%">

_Enter the prompt "h" and the response is "hello world hello world hello world hello " (letters are generated by TF NN inference)_<br>
<img src="/assets/d5_1.png" alt="drones" width="55%">

<br>

---

---

---

---

---

<br>

# **Part 4** Real LLM with HF (build locally, publish, deploy) (TODO)

<br>

see **[2b.2 Tiny model demos](/2b.3.6-llm-demos/)** and **608.docx** (can access when return to HK)).

TOC

- **[n6] Build (add iA API)**. iA offers API, just like OS/Kernel to proc apps. Provides the API for the eAgent.
- **[n7] Publish (HF)**. Packaged into a unit, provided on HuggingFace or elsewhere for download.
- **[n8] Deploy (locally, Ollama)**

```
TO MAKE OUR TINY DEMO INTO A REAL MODEL, WE NEED TO
1 OUR TINY DEMO BECOMES iA
2 ADD CODE TO OUR TINY DEMO TO CREATE API
3 CREATE eA THAT SENDS PROMPT TO TINY DEMO CODE
4 CHANGE TINY DEMO SO THAT IT TAKES PROMPT AND FEEDS INTO TF
  THEN SENDS RESPONSE BACK TO eA
5 AFTER TESTING THIS, THEN USE HUGGINGFACE TO
  CREATE A MODEL THAT CAN INSTALLED AND RUN
```

<br>

---

---

---

<br>

### **[n6] Build (add iA API)**

iA offers API, just like OS/Kernel to proc apps. Provides the API for the eAgent.

_Real LLM (with API)_<br><img src="/assets/wuxi-28.png" alt="xxx" width="36%" style="border: 1px solid #999;">

_LLM_<br><img src="/assets/wuxi-88.png" alt="xxx" width="56%" style="border: 1px solid #999;">

<br>

---

---

---

<br>

### **[n7] Publish (HF)**

Packaged into a unit, provided on HuggingFace or elsewhere for download.

- .pt = TF weights/biases + NN structure

_LLM publish to Hf_<br><img src="/assets/wuxi-89.png" alt="xxx" width="36%" style="border: 1px solid #999;">

<br>

---

---

---

<br>

### **[n8] Deploy (locally, Ollama)**

Download and run locally (using hosting SW like Ollama).

_LLM installed locally (from HF to Ollama)_<br><img src="/assets/wuxi-90.png" alt="xxx" width="60%" style="border: 1px solid #999;">

<br>

**(External) Agent = equivalent of the OS application (contains your business logic)**

- (ext)Agent
  - = the non-human user of the AI (LLM) API.
  - procedural (CPU) code that your write that uses the LLM.
  - eAgent contains the end user central logic (business logic)
- extAgent can use AI in various modes:
  - Chat
  - Action (tools)
  - Single shot execution
  - Loop execution
  - Automation (reaction)

_AI agent_<br><img src="/assets/wuxi-29.png" alt="xxx" width="19%" style="border: 1px solid #999;"><br><img src="/assets/wuxi-79.png" alt="drones" width="47%">

<!--
USE THIS TEXT ELSEWHER??? =========================================================
**LLM = equivalent of OS**.

- The diagram below shows the internal stucture of an LLM.

- **Internal agent (iAgent) (CPU)**
  - procedural (CPU) code that runs the main loop and controls LLM input/output.
  - Very closely customized to TF.
  - feeds required prompts into TF and process responses.
  - responds to eAgent

The iAgent/TF

- are designed to work closely together (iAgent must be totally customized to the TF; iAgent will contain vast amounts of "glue" logic)
- need language and "thinking" patterns to simulate human thinking (_the outputs are far less predictable and reliable than procedural code_). -->

<!--
#### **3.1b LLM AI simulated intelligence (procedural agent + matrix math pattern classification)**

The general structure shown below:

<!-- > = eA//LLM = eA on OS // (iA on OS) + (TF on CUDA/GPU) --

- eAgent = Agent code that you write (that interfaces with the LLM API).
- LLM = iAgent + TF.
- iAgent = Agent code written by Frontier model maker that controls TF.
- TF (transformer) = matrix math algorithms that classify patterns (based on training data) running on CPU (via CUDA).

_(external) agent + LLM are built on 100% pure digital computation components_<br><img src="/assets/wuxi-66.png" alt="xxx" width="41%" style="border: 1px solid #999;"><br>

_Matrix math network (not really "neural")_<br><img src="/assets/wuxi-61.png" alt="drones" width="36%" style="border: 1px solid #999;">

<!-- #### **3.1e EXAMPLE** --

<br> -->

<br>

---

---

---

---

---

<br>

# **Part 5** Real LLM with PAL Foundry (TODO)

you can build/deploy within Foundry: see **[2.2b ZAI versions of the core ~8 _Foundry_ getting started demos](/3c.2_pal_initial_demos/)** section "(7) D8a (WIP) — Deep Dive: Model integration (26.0905)".

TOC

- xxx

<br>

---

---

---

<br>

---

<br>

26.1005 (v1 26.0929)

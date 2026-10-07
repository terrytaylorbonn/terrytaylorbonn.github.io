---
layout: page
title: 0-demo_hack_2
permalink: /0-demo_hack_2/
---

<br>

#### **n3.2b Subcomponent TF details (MOVE INTO HACK) ###################**

was: n3.3 AIPU functionality: Basic (language models, pattern recognition)

- **Transformer (TF) (GPU)** (The part of the LLM that makes it able to generate token sequences that mimic intelligent responses; NEEDS TRAINING INPUT)
  - 1 (main) **pattern matching** in "machine language" space
  - 3 **language models** (Transformers; they convert inexact human representation of meaning (words) into massive amounts of numbers that are used to compute the exact "machine language" meaning)

- (1) sees, hears, touches NOTHING.
- (2) binary data (representing prompt) is converted into numerical representations. For each token in GPT-3 that means 12K FP numbers (this is complex encoding/representation of the computed meaning, including context, vastly more info than just a few letters).
- (3) TF performs pattern match on all the machine language numbers (KEY CAPABILITY OF TF: vastly different letter inputs can end up with very closely matched machine language results)

_(hack-01) TF algorithm (GPT-3)_<br><img src="/assets/hack-01.png" alt="xxx" width="41%" style="border: 1px solid #999;">

**n3.3.1 language models**

Solution part 2

- use AH to create "machine lang" rep of token meaning (and storyline)
- vastly more exact meaning than token
- logical representations ... neighbors in vector space mean same thing

**n3.3.2 pattern detection**

use NN: below GPT-3:

- 2048 token window
- 12288 FP16 per token

- left: inputs
- middle: detections (of patterns)
- right: detections of detections

_72_<br><img src="/assets/wuxi-72.png" alt="xxx" width="15%" style="border: 1px solid #999;">

**n3.3.3 multiple stages**

- compute Attention (contex)
- perform detections

**n3.3.4 FINAL STAGE / compute classification/token**

Resulting classification

- 12288 FP16 in last token
- (in last token because thats how it was "trained" (programmed))
  - training is automated
  - matching language representations naturally occur during train process (but impossible for humans to do manually)

Compute final token

- 50K x 12288 matrix to compute 50K logits
- highest probability is new token

- LLM spits out best classification which becomes the next token.
- (4a) after many iterations the output is a CLASSIFICATION -- a set of probabilities for all tokens. Usually the token with highest probability is chosen as the output token (which is then appended to the input and then the cycle repeats) (the most probable token is not chosen when the LLM is programmed to trick the user with random output to give the impression of real intelligence rather than deterministic programming; LLMs are 100% deterministic in their computations)

- The classification concept of AI can be used in many areas. For example
  - FSD (full self driving) has many inputs which are used to select a set of outputs (used to drive the car)
  - Object Recognition classification (dog or cat)

- The LLM transformer (TF) computes the classification of the current prompt/response, and
- that classification is used to select the next token to add
- (this process is repeated until the TF or internal agent decide to stop).
- The LLM internal Agent orchestrates TF input to construct complex final responses.

There is no intelligence. Only pattern matching to classifications (tokens) that were "imprinted" on the LLM during "training" that used massive amounts of (often plagiarized) input token sequences (training text).

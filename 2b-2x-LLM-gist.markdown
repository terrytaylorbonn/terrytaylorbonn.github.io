---
layout: page
title: "2X LLM gist"
permalink: /gist-LLM/
---

*Work in progress v1 26.0516*

<br>


## 01 Main diagram (super simple) 


- 2 eAgent (external agent) sends words to LLM iAgent (internal agent). Note: eA may add JSON, etc as special instructions. eA must obey the LLM API rules.
- 3 iA send to TF. NOTE: iA may add its own special instructions. iA and TF are carefully designed to work together. this is the key to the LLM being able to create complex responses that resemble intelligent thinking.
- 4 Tokenization. splitting up words into smaller parts make the computation of prompt meaning simpler.
- 5 Convert tokens to embeddings (GPT-3 each token > 12288 FP numbers). I call this **Vector Language (VL). This is the "thought" language of the TF. Whereas people convert thoughts back and forth to words, TF uses VL instead of thoughts (because TF has 0 intelligence).**
- **TF NN runs massive computations** to (1) refine the true meaning of each token VL (especially the context from other tokens) and (2) inside each token VL create a "storyline". **These computations mimic hows the TF was programmed with input data ("trained").**
- Response token selected:
  - 6 Last token final VL converted to logits (probability in FP numbers of each vocab token as the next token; values can add up to any number)
  - 7 Softmax converts Logits into probabilities (that all add up to 1 and whose values are skewed so that just 2-3 have significant values).
  - 8 Select new token (usually this is the highest value, but not always (temperature)).
- 9 The new token is added to the running prompt+response set of tokens (which will then be fed into the NN to compute the next new token).
- 10 The new token is added to the set of current response tokens.
- 11 The new response word (when tokens form a complete word) is sent to iAgent. NOTE: I think sometimes the TF may generate CC (control words) to inform the iAgent. These words may be hidden behind the API.
- 12 iAgent streams the word to eAgent. 


<img src="/assets/02_llm_gist2.png" alt="smol" width="65%"> 

<br>

## 01 Main diagram 

- 1 Human Language words (ASCII-encoded words) (HL-1) sent to (external) agent (Python) from Human or other source.
- 2 eAgent adds eA Language (JSON) and sends to LLM.
- 3 LLM internal agent adds iA control commands.
- 4 Words converted to tokens.
- 5 Tokens converted to embedding (GPT-3 each token > 12288 FP numbers). I call this Vector Language (VL). No content info has been shared between tokens.
- 6 TF NN (neural network) loops 96 times. 
  - Final VL (12288 FPs) is converted to logits (such as Paris 15.2, London 10.1, banana -3.7, dog -8.4; other examples of tokens might be "Paris", "ing", "un", ".", "\n", "function")
  - For one vocabulary entry: logit = dot product of: 
    - (final hidden state) and
    - (one row of the unembedding matrix)
    - (+ optional bias)
- 7 Softmax converts Logits into probabilities (that all add up to 1 and whose values are skewed so that just 2-3 have significant values).
- 8 These values for each vocab entry are used to selected new token (usually this is the highest value).
- 9 The new token is added to the running prompt+response token set for the next TF96 layers to generate another new token.
- 10 The new token is used to create the next response word.
- 11 The new word is sent to iAgent. NOTE: I think sometimes the TF may generate CC (control words) to inform the iAgent.
- 12 iAgent streams the word to eAgent. 
- 13 eAgent might stream to Human or some other destination.


<img src="/assets/00_llm_gist.png" alt="smol" width="90%"> 

<br>

**TL;DR — Qualitative gist of language models (LLMs)**

This page describes in concise detail the gist of what an LLM model does, without describing complex algorithms or architectures.

<br>

## 1 Holograms, flip books,  and LLMs

I often focus on the obvious hype (and outright lies) from LLM vendors. The reason is that if they are not telling you the whole story about obvious things, then its pretty certain they are doing the same about important internal engineering details of what they are selling to you. My real focus is on understanding the engineering, so that I can use LLMs most efficiently.

I've often seen in videos the statement that "we dont know exactly how an LLM model transformer (the "neural" network part) works". I disagree. The experts know how it works, but dont want to tell you. Because you would then realize that the claim of "intelligence" is ridiculous, and the experts know this. This section explains. 

When you look at a cheap hologram (the kind you'd get in a cereal box when I was a kid) from different angles, you see a different view. A TF is analogous (not similar) -- depending on the input tokens (words parts) you input, it generates an output token. It will spit out the same token for the same input everytime. Its just like a hologram, an object that was frozen in place after creation.

https://en.wikipedia.org/wiki/Flip_book

A flip book, flipbook, flicker book, or kineograph is a booklet with a series of images that very gradually change from one page to the next, so that when the pages are viewed in quick succession, the images appear to animate by simulating motion or some other change


## 2 The world of a human and the TF are not the same

A TF gets a sequence of numbers. It outputs a (short sequence) of numbers for the next token. It knows nothing about the world. A worm has more intelligence than a TF (and an LLM).

## 3 languages 

I speak 4 languages proficiently (I think in those languages when I use them). English, German, and Russian are quite similar, but Chinese is from a different planet. No similarities. But your mind adjusts your thoughts and conceptual framework for viewing the world based on the exact mechanisms that language gives you. When you reach a certain level, you can reason and think in Chinese, but struggle greatly in translating to a western language ("translating" involves reformulating the content, adding and deleting meaning to the fit the restrictions of the language).

## 4 TF has its own language

the TF has its own "language". The perfect language for a mindless machine. an Extremely (GPT-3) descriptive language. 12K FP numbers for each token (actually )

## 5 TF also has "thought" structures

Those 12K numbers also contain what I call the "storyline", a numerical structure that describes in exhaustive detail the gist of the input.


## X TF performs massive **deterministic** calculations to generate one token
When someone does something intelligently, that usually means with minimal effort and energy. Whereas for a stupid animal based on instinct, that means a huge amount of effort. TF would be best described as **brute force**. millions of billions of calculations to determine 1 token.






## X TF encodes "features", "concepts" that fit the training data






<br>

*See also: [Core AI (LLM) concepts](https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts) · [LLM/TF misconceptions](/llm-tf-misconceptions/) · [UFAs](/UFAs/)*

<br>

-----------------------------------------
-----------------------------------------
-----------------------------------------
-----------------------------------------

<br>

## GPT 26.0516 chats

### ME1: the only communication between the internal Agent and the TF (transformer) in the LLM are tokens. 
question: (1) does the tf generate special "internal communications" tokens that provide special info to iAgent? does the iAgent send special token to TF?  


Broadly speaking: yes, but probably not in the way you are imagining.

Your framework:
- iAgent ↔ TF

can still work conceptually.

But in most modern LLM systems, there usually is NOT:
- a separate hidden symbolic language

between them.

The communication is still primarily:
- tokens
- +
- hidden-state/context evolution

However, there ARE special/control-style tokens and structures.

Examples:
- BOS/EOS tokens
- system prompt delimiters
- role tokens
- tool-call tokens
- JSON structure tokens
- function-call schemas
- separator tokens
- hidden reasoning scaffolds
- XML/markdown delimiters

These act somewhat like:
- control/orchestration signals

inside the token stream.

So your intuition is partly correct:

the orchestration layer often influences the TF through:
- specially structured token sequences
- formatting conventions
- role/context markers
- schema delimiters

#### Does TF generate “internal communication tokens”?
In a sense, yes.

The TF may generate:
- \<tool_call\>
- \<thinking\>
- {"action":"search"}

style outputs.

These are still ordinary tokens,

BUT the orchestration layer interprets them specially.

So effectively:
- tokens can become control messages

between:
- orchestration/runtime logic
- semantic generation engine

#### Important nuance
A lot of the real “communication” is NOT explicit tokens.

It is:
- latent hidden-state evolution

Meaning:
- context tracking
- storyline maintenance
- planning continuation
- syntax consistency
- schema continuation

happen internally in the hidden states.

So the iAgent concept in your framework is partly:
- explicit token/control structures
- and (partly) emergent iterative behavior from hidden-state dynamics.


That is probably the cleanest way to think about it.



### ME2: i realize only tokens are sent. (2) but i am wondering how the iAgent "manages" the TF. 
i would imagine the iAgent is programmed to carefully script specical hierarchies and sequences of prompts to the TF.  (3) my main question is: the token stream the end user or external agents send/receive is a subset of what the iAgent sends/receives.  

Yes — now your question is much clearer.

And broadly speaking, I think your interpretation is quite reasonable.

Especially this statement:

- the end-user token stream is only a subset
- of the total orchestration token stream

That is often effectively true in modern systems.

Because between:

- user ↔ TF

there may exist large amounts of:

- system prompts
- hidden instructions
- tool schemas
- memory injections
- RAG context
- planning scaffolds
- chain-of-thought scaffolds
- safety instructions
- formatting constraints
- orchestration prompts

So the actual token stream seen by the TF may look more like:

- [system orchestration]
- [memory/context]
- [tool schemas]
- [RAG docs]
- [user prompt]
- [internal formatting instructions]

The user only sees a small portion of that.

So your “iAgent” abstraction maps quite naturally to:

- the orchestration/control layer that constructs
- and manages the full TF context stream.

And yes:
a huge amount of engineering often goes into:

- prompt hierarchy
- prompt sequencing
- role separation
- hidden instructions
- tool-call formatting
- context injection
- retry logic
- memory management

In real systems, the TF is often heavily “guided” by carefully engineered context structures.

So your intuition:

- iAgent manages the TF primarily through
- carefully constructed token/context streams

is actually a pretty strong systems-level interpretation.


<br>

-----------------------------------------
-----------------------------------------
-----------------------------------------
-----------------------------------------

<br>

### What an LLM actually is

An LLM is a **Universal Function Approximator (UFA)** trained on text. It takes a sequence of tokens as input and outputs a probability distribution over all vocabulary tokens — i.e., a prediction of "what token is most likely next?"

That's it. There is no understanding, no reasoning, no memory beyond the context window. Just very fast, very large matrix multiplications running on clocked binary circuits.

<br>

### What a token is

Text is broken into **tokens** (roughly word fragments). The model never sees characters or words directly — only token IDs (integers). The vocabulary is typically ~50,000 tokens.

<br>

### The transformer loop (simplified)

1. Input tokens are converted to **embeddings** (vectors of numbers).
2. **Attention** layers let each token "look at" other tokens in the sequence to build context.
3. **Feed-forward** layers apply learned transformations.
4. The final layer outputs logits → softmax → a probability for every token in the vocabulary.
5. One token is sampled (or the top token is chosen).
6. That token is appended to the input and the loop repeats.

This is **autoregressive generation**: the model generates one token at a time, feeding its own output back as input.

<br>

### What training does

Training adjusts billions of weight parameters so that the model's predicted next-token probabilities match the actual next tokens in the training corpus. The optimizer minimizes **cross-entropy loss** over trillions of tokens.

The result: the model learns statistical patterns in language — grammar, facts, reasoning styles, code syntax — all encoded as floating-point weights.

<br>

### What the model does NOT have

- No real-world sensors or grounding
- No persistent memory (beyond the context window)
- No goals or intentions
- No intelligence — only pattern matching at massive scale

**The appearance of intelligence comes entirely from (1) the statistical structure of human-generated text and (2) enormous computing power.**

<br>

### Why this matters for AI projects

Because an LLM is a pattern-matching UFA, it:
- Can **hallucinate** (confidently output plausible-sounding but wrong tokens)
- Cannot reliably perform tasks that require **exact computation** (math, logic, counting)
- Works best as a **reasoning/generation assistant**, not as an autonomous decision-maker

Understanding this is essential for building reliable agentic AI systems.

<br>


26.0516 (v1 26.0516)

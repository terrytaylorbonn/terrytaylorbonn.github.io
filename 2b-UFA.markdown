---
layout: page
title: "(2b) UFAs"
permalink: /UFAs/
---

<br>

This page is WIP (v1 26.0510).

<br>



**If an LLM was truly intelligent, then an AI agent (Python app) could simply send free form text and done with it.** But an LLM is not intelligent. Its output are statistical approximations (the "A" in "UFA") based on algorithms and input data used to program ("train") the LLM.  Therefore to use AI agents effectively, it would really help to understand Universal Function Approximators (UFAs) and how they are implemented in LLM TFs. 

Note: This section talks about the TF in GPT-3. GPT-3 is the only model I have studied in detail. Newer may be much more powerful, but the core techniques they use to implement a UFA will be similar.

Most of this page is my original material. So, as with LLMs, a disclaimer: I sometimes make mistakes. :)

<br>

#### **TOC**
**1 REQUIREMENT (human <> computer bridge) / SOLUTION (UFA).** 

Why do we need a UFA? 
- Because human communication systems (language) are designed for intelligent beings.
- Digital systems are simply computation. No intelligence. 
- Digital systems are vital for us. We need a bridge. 
- UFA is only viable option. But it has definite limits.

**2 HOW TF-UFA WORKS (INF(hLang/vLang/mLang), TRAIN).**

Its not intelligent. Its computational pattern matching.
- TF converts Human Language (HL) input into Vector Language (VL) (12288 FPs per token).
- VL is refined in 96 layers.
- VL also contains a "storyline".
- TF outputs a token based on how current token input matches the token inputs used during training (its basically pattern matching).
- TF adds the token to the input and repeats the process (until finished or told to stop). 

**3 HOW TF-UFA SUPPORTS AGENTIC AI (list of 8).**

Describes how the LLM has seemingly intelligent functionality that can make its outputs much more likely to be processed by a Python script (the agent) successfully. Much of this functionality is based on some very clever training techniques, and is vital for agentic AI.  Note: Again, these are approximations, so the agent must be programmed to handle exceptions. 

**4 CNN/TF ALGORITHM DETAILS (MATH).**

- The cool looking 3d diagrams you often see are only confusing you.
- CNNs (object recognition) are simpler than TFs, and are an excellent stepping stone / analogy for understanding the more complex TFs. 
- My TF explanation focuses on the math. This makes it much simpler.

<br>

# **1 REQUIREMENT (human <> computer bridge) / SOLUTION (UFA)**

### 1.1 requirement: interface humanLang and computer worlds 

(1) the human world is vastly more interesting. more complex.

(2) but the LLM is very fast and can be scaled... and is native to our digital worlds.
and digital for many things is better (costs, distances, etc)

(3) interfacing these 2 worlds is complex... solution??? a  bridged 
a comptational engine in computer that can replicate human interaction mechanisms (language) without intelligence or knowledge. just digital equations.

(4) this bridge will be a crude approximation, a guess... its dangerous sometims
Humanoids in the home, FSD on the streets. You are mixing 2 worlds
	Humans who see, hear, touch, smell, have vision, consciousness, etc. This defines everything thing they do, their complex interactions.
	AI machines that are based 100% on 100% binary computation. They see nothing, have no thoughts, etc. They do ONLY what they are programmed to do.
 
### 1.2 our brains do 3 things (1) store info (2) encode/decode (language) (3) intelligent answers

(1) we have memories,thoughts. 

(2) we encode / decode into languages. 

(3) the digital intelligence must do the same thing.
 
### 1.3 computers have no intelligence... they must have algorithms
no thoughts, no understanding. 
they are simply calculators. 
with digital data storage. 
thats it.
 
### 1.4 working solution: equations (kalman, pid)

(1) kalman works for many things.
equations are magical. they define how things interact.
they dont store patterns.... they store how our world really functions.

(2) PID
computes how moving objects can be controlled with inputs (in teh real world more complex, there are more factors, but these equations are good for simplified situations).
 
### 1.5 "deterministic" algorithms (equations) fail for many thigns

(1) interactions have definitions but are too complex (molecules)
(like molecular reactions) that you cant define the world with the low level fucntions that describe interactions (or digital math is not a good enough approximation). in molecules, every atom interacts wiht every other, and they are not simple point shapes. this is impossible to model. simplifying the model of these interactions results in wrong results. 

(2) large sets of data sometimes dont follow any logical patterns (bel/hol)
this example is used throught this page (belgium/holland)

(3) follow patterns that are defined by intelligence (LANGUAGE IS A PERFECT EXAMPLE) 
we have intelligence, and our words are minimalist code that we transfer info. but binary computers cant understand what they mean. and defining all the possible combinations of words is impossible (and also including spelling mistkaes).
 
### 1.6 TF UFA solution

(1) the TF implements a UFA (probabliistic approximator, not intelligence)

When I first read about UFAs, I thought it was some useless theoretical talk. Its actually the key to understanding AI. AI is based on Transformers (TFs) that implement UFAs. If you understand UFAs then you truly understand AI.

Universal Functino Approximators (UFAs). That word "approximation" is the key.  https://medium.com/hackernoon/illustrative-proof-of-universal-approximation-theorem-5845c02822f6 
 


(2) TF UFA encodes patterns via programming "training" 
is actually encoding patterns into the NN. rather than equations, the input is 
=1) converted (from words) into a representation (vector lang) 
that is much more logical (but too complex for humans to process), something a dumb machine can process
=2) Vlang used to detect the closest trained pattern
then use the trained result.
thats it.
approximation.


 
### 1.7 viable/nonviable applications

(1) viable: BELGIAN TOWN DEMO ADD (mistakes are not critical)

And when you understand how AI really works, you will understand why agentic AI works in systems like Palantir Maven (and in many many other business segments), 

26.0227 (day 4) distill chat content from yesterday  // #600_core_AI_concepts_v13 // 1.2 Netherlands/belgium example (from Welch labs) https://youtu.be/qx7hirqgfuU?t=6 
 
@258
 
 
(2) not viable: Driving cars on public roads 

but will never be safe enough for self-driving cars and home humanoids. That’s my personal opinion (backed up by over a decade of empty self-driving car promises).

 
# **2 HOW TF-UFA WORKS (INF(hLang/vLang/mLang), TRAIN)**

### 2.1 The core of what a TF does during inference

(0) note: 
algorithms are crude. but they are massive, and provide the skeleton for the training to create magic

all of the computations are deterministic.
 if you input exactly the same prompt, you would get exacctly the same response.(unless the TF intentionally is programmed to fool you with functions like temperature, etc)..

(1) The TF converts human language (HLang) input to "vector language" (VLang) 12288 FP numbers ("hidden states")
when they first enter the TF the 
the words are first broken up in to tokens (parts of words). they are still composed of ASCII chars.
then for each char 12288 FP numbers. 
a set of 12288 numbers is (what i call) vector language. a super definition of the meaning of that token. 
      


(2) inside TF layers, the vector language representation is gradually refined

2 things occur
AH: info between words is shared. basically refining the meaning of a word.
 

FFN: detecting core complex meaning of the word AND the world it exists in.

https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts#4323-ai-neuron-xor-using-additive-gates 
    

for GPT-3 96 layers were required to get it to work
computers need this massive amount of computing to implement the UFA.

 

(3) inside TF, a "storyline" inside the VLang starts to develop
the UFA requires 12288 for each token because much more info is stored there. 
what i refer to as the storyline.
in EACH token. 
but since tokens share info, the storyline is in each token.

 
 
(4) TF outputs Tokens
the storlyine of the last token is used to compute the MOST PROBABLE next token. 
 

### 2.2 TF "Training" (programming) determines what inference produces 
a TF does not learn. it is programmed.
complex training sw inputs data into the TF.
TF internal params (trillions of them) are adjusted (weights and biases)
so that the output is closer to what it should be for the current input.
training is done for each token based on all previous tokens
((thats why inference also computes the next token, duplicating the training).

ADD DIAGRAM OF STAIRSTEP TRAINING ######################

<br>

# **3 HOW TF-UFA SUPPORTS AGENTIC AI (list of 8)**

#3b Advanced inference/trained features (CRITICAL for AGENTIC AI)

(1) output tokens can have very specific formats ("machine language")
The prompt can define the fomrat of the outputs. 
THIS IS CRITICAL for creating responses that the python lang agents use to run analysis.
 

(2) TF trained to break up big tasks into planning  ####################

(3) full list of 8 trained capabilities ###################

<br>

# **4 CNN/TF ALGORITHM DETAILS (MATH)**
### 4.1 typical confusing TF how-it-works explanations (3d diagrams, hyperplanes) 
(1) CONFUSING typical diagrams #600-4

As I understood more and more how AI (GPT-3) works, I became more convinced that much of the concepts and diagrams I had studied about AI confused me more than anything. what imprssion the typical student of AI gets from these types of digrams is not correct.

    

     


Example: This diagram is interesting. but it only confusing when trying to explain AI.
https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts , [1] https://www.youtube.com/watch?v=Ln8pV1AXAgQ 

the pictures below are all impressive depictions of AI. The problem is, the more I understood AI, the more they confused me. Hyperplanes are conceptual hype. Marketing gimmicks. Designed to hype binary computational ("mechanical") algorithms into something mystical, "hyper", "intelligent".  This post explains with a few chats I had with GPT (I dont explain all the details, I just pasted the chats). 
[2] https://youtu.be/NrO20Jb-hy0?t=5    //   [3] https://youtu.be/KJtZARuO3JY?t=761 
 
To me these diagrams are pretty. and totally misleading. [4] https://youtu.be/KJtZARuO3JY?t=955 

https://youtu.be/qx7hirqgfuU?t=157 
 

 
(2) the typical complex equations

the equations below from GPT are correct.. but impossible to understand. 

these are legalistic expert formulations (important for published papers, but not the best for understanding how it works)

ME: you once wrote this. do you understand (some of the notation is lost when copying from ms.word)

A useful mental model for your readers: Attention = routing & aggregation FFN = computation & feature creation Without FFNs: attention would just remix existing vectors no new features would be created FFNs are where: pattern detectors live abstractions form token-local reasoning happens Many researchers now believe: FFNs store most of the model’s “knowledge.” What “identical weights” means (exactly) In a given transformer layer: There is one FFN With one set of parameters: W_1,b_1,W_2,b_2 That same FFN is applied to: h_1,h_2,…,h_2048

Formally (note "for all i"):
"FFN"(h_i)=W_2 " " σ(W_1 h_i+b_1)+b_2 "for all " i

So for each token h_i:
	Expand:
z_1=W_1 h_i+b_1 (49152×1)
	Nonlinearity:
z_2=σ(z_1)
	Compress:
z_3=W_2 z_2+b_2 (12288×1)
	Residual:
h_i^"new" =h_i+z_3
That is a huge per-token computation — often more FLOPs than attention.
 
### 4.2 CNN <> TF comparison/analogies
(1) CNN

1) when we see a pic, we recognize patterns.  cnns dont do that. they calculate numbers.

both achieve kind of the same result.
but not really. 
the cnn is faking it.

but its a good fake.
works most times.
just dont trust your life with.

2) convolute = LAYERS[ (1) mixing pixel content (2) pooling ], and (3) NN detecting (4) select.

after the first layer they are no longer pixels.
(crazy diagrams of what the cnn is doing.. this is nonsense, like the 2d plots for TFs).
they are "hidden states", which I called "vector" language.

3) at each layer the detection gets higher level

4) then finally last layer. go thru detector to compute most probable content

 
(2) how TF is similar
the similarities really struck me when first started to dig into the details of TFs. but i never once read anything about these similarites.
5) 96 layers[ (1) mix context (2) softmax to "pool", and (3) FFN (detection) ] (4) Woutput

 
### 4.3 my TF UFA explanation (simple steps) (minimal  GPT NOTES)

my explanation (simple, to the point, no "hyperspace" talk)
There is no "hyperspace".. there are only calcualtions.
"hyperspace" is an abstraction that only makes things more confusing.
 
ME-1: I want to explain the above in simple for humans fashion.
i will use my notation. its simpler. 
your equation above is true for all tokens... but its too complicated.
i focus on just one token.

x1... x12288 are token hidden layer values.
h1... h49152 are the dectors.
for h1:
        multiply x1 by Wh1.1
        multiply x2 by Wh1.2
        etc 
        add all the values up
        add the bias for bh1
        apply GELU 
for h2:
        multiply x1 by Wh2.1
        multiply x2 by Wh2.2
        etc 
        add all the values up
        add the bias for bh2
        apply GELU 
etc

 
ME-2: outputs are y1...y12288
for y1:
        multiply h1 by Wy1.1
        multiply h2 by Wy1.2
        etc 
        add all the values up
        add the bias for by1
        NO GELU 
for y2:
        multiply h1 by Wy2.1
        multiply h2 by Wy2.2
        etc 
        add all the values up
        add the bias for by2
        NO GELU 

 
ME-3: are Wh and Wy same for 
- all tokens? (i think yes)
- all layers?  (i think no)


Different between layers
Each transformer layer has its OWN FFN weights.
So:
Layer 1:
  Wh(L1), Wy(L1)

Layer 2:
  Wh(L2), Wy(L2)

Layer 3:
  Wh(L3), Wy(L3)
etc.
The detectors evolve by layer:
	early layers → simple/local patterns 
	middle layers → abstractions 
	later layers → high-level semantic/storyline features 
So your intuition is correct:
	SAME across tokens 
	DIFFERENT across layers 
 
ME-4: for y1, when you add up Wy1.1, Wy1.2, .... 
how do you keep the sum from "exploding".
becoming very large values?
does this question make sense?

GPT: Yes — the question absolutely makes sense.
And yes, uncontrolled sums would explode without special mechanisms.
Several things help keep values stable.
1. Small learned weights
The weights:
Wy1.1
Wy1.2
...
are usually relatively small numbers.
So even though you add many terms:
h1*Wy1.1 + h2*Wy1.2 + ...
the positive and negative values partially cancel.
2. GELU suppresses many detectors
After GELU:
	many h-values become small 
	weak detectors are damped 
	only some detectors strongly activate 
So not all 49152 detectors contribute large values.
3. Training naturally stabilizes activations
During training, exploding activations create bad gradients and instability.
So the optimization process tends to learn:
	reasonable weight magnitudes 
	stable activation ranges 
4. Residual architecture helps
The FFN output is usually added back:
new_token = old_token + y
This residual structure helps prevent runaway instability.
5. LayerNorm is critical
The biggest stabilizer is probably Layer Normalization.
LayerNorm continually rescales activations so hidden-state magnitudes stay in a reasonable range.
Without normalization, deep transformers would often become numerically unstable.
So your intuition is correct: huge sums could explode
and transformer architecture contains multiple mechanisms specifically designed to prevent that.
 
ME-5: is KV context similar to CNN convolution?
can they be compared? 
from my understanding of convolution,
it means linking the meaning of related pixels
(its easy to determine this for pixels... the neighbors matter).
but for tokens, the location of related tokens is not predictable.

GPT: Yes — your intuition is very good here.
They can be compared, but the key difference is exactly what you identified:
CNN convolution
In a Convolutional Neural Network:
pixel relationships are local and predictable
Nearby pixels usually matter most:
	edges 
	corners 
	textures 
	shapes 
So convolution uses:
	fixed local windows 
	nearby neighbors only 
Example:
3x3 pixel region
The detector slides spatially across the image.

Transformer attention / KV context
In a Transformer Neural Network:
related tokens may be anywhere
Examples:
	subject at beginning of sentence 
	pronoun later 
	earlier instruction 
	JSON schema far above 
	function definition many tokens earlier 
So transformers cannot assume:
nearby = related
Instead attention dynamically determines:
which tokens matter
using:
	Query 
	Key 
	Value 

Very rough analogy
CNN:
fixed local attention
Transformer:
dynamic global attention
or:
CNN convolution:
predefined neighborhood relationships
Transformer attention:
learned contextual relationships
So your statement is basically correct:
for pixels, neighbors usually matter
but
for language, related tokens may occur anywhere
That is one of the major reasons transformers replaced CNNs for language tasks.





<br> 


26.0511 (v1 26.0510)

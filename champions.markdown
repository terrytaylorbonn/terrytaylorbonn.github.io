---
layout: page
title: Heroes
permalink: /champions/
---

<br>

_(WIP; v1 26.1010)_

<br>

This page is about 
- **1 AI champions**. Their hard work and insight made it all possible.
- **2 AI heroes**. When your AI champions become your AI heroes -- that's when you start to make mistakes. 
- **3 AGI super heroes**. In the end, the AI champions are claiming to give you something that they know is not possible (human level "intelligence" AI). 


<br>

---------------
---------------
---------------
---------------

<br>


# **1 AI champions**

**Many industry champions worked over generations to make the current AI tech possible**. We owe them recognition for what they have accomplished (even if it causes hardship for many of us, its still progress). This page talks about just a few of them: Geoffrey Hinton and (more recently) Jensen Huang (Nvidia) and Elon Musk. They became the champions by working hard and taking risk when the reward was hard (for the rest of us) to see.


TOC
- **1.1 Jensen Huang and GPUs**. Jensen  was only thinking about video but he was creating the computational HW basis for AI. 
- **1.2 Geoffrey Hinton and AlexNet CNN**. Hinton's 2012 AlexNet team proved that massive scaling of matrix math classification algorithms (a hack) was the best path forward for image recognition. They used Nvidia GPUs (with a pre-CUDA hack).
- **1.3 Various champions and basic LLMs**. They provided (piece by piece) that transformers (QKV_context/FFN_detection) were the core matrix math algorithms (hacks) that promised the best path forward for token generators (the core of LLMs).
- **1.4 Huang/Musk and advanced LLMs**. They proved that massive brute-force scaling could achieve practical results for many AI applications (this scaling is logarithmic because the requirements for adding another 9 to 99.99...% is itself logarithmic).


<!-- often make what I consider very misleading statements ("hype"; there are other stronger, perhaps more appropriate, terms). And of course they do; they are still driven by the desire to be the "champions" (of the world). -->

<br>

*The following are the lyrics to Queen's "We are the champions". A great song by a great band.*

<!-- Note the line **"no time for losers"**.-->

```
I've paid my dues
Time after time
I've done my sentence
But committed no crime
And bad mistakes
I've made a few
I've had my share of sand kicked in my face
But I've come through (and I mean to go on, and on, and on, and on)

We are the champions, my friends
And we'll keep on fighting 'til the end
We are the champions
We are the champions
No time for losers
'Cause we are the champions
Of the world

I've taken my bows
And my curtain calls
You brought me fame and fortune and everything that goes with it
I thank you all
But it's been no bed of roses
No pleasure cruise
I consider it a challenge before the whole human race
And I ain't gonna lose (and I mean to go on, and on, and on, and on)

.........
```

<br>

---------------

<br>


### **1.1 Jensen Huang and GPUs**

Jensen was only thinking about video but he was creating the computational HW basis for AI.

_[video](https://youtu.be/caKyQNfj9BM?t=346)_<br><img src="/assets/sun-04.png" alt="drones" width="30%">


<br>

---------------

<br>

### **1.2 Geoffrey Hinton and AlexNet CNN**

Hinton’s 2012 AlexNet team proved that massive scaling of matrix math classification algorithms (a hack) was the best path forward for image recognition. **They used Nvidia GPUs (with a pre-CUDA hack that convinced Jensen to focus on GPUs for AI and CUDA)**.

_[video](https://youtu.be/caKyQNfj9BM?t=532)_<br><img src="/assets/sun-05.png" alt="drones" width="45%">


See also the following ZAI takes on CNNs:
- **[Concepts -- 2.4 CNN convolution](https://ziptieai.com/0b.2.4-concepts-convo/)**
- **[2.2.1b D4 CNN algorithm details](https://ziptieai.com/2.2.1b-d4-cnn-algorithm-details/)** has the best diagram of the AlexNet CNN (ZAI original diagram)<br><img src="/assets/d4_alexnet.png" alt="drones" width="23%" />



<br>

---------------

<br>


### **1.3 Various champions and basic LLMs** 

These champions proved that transformers (whose primary algorithmic components are **[QKV_context](https://arxiv.org/abs/1706.03762)** and FFN_detection) were the core matrix math algorithms (hacks) that promised the best path forward for token generators (the core of LLMs).

- Transformers 
  - transform tokens into embeddings (in GPT-2 12288 FP16 numbers for each token; this is what ZAI often refers to as "machine language").
  - create a storyline that is located in the last token that is used to classify the meaning of the transformer input (the storyline is then used to compute the probability of each of 50K (English) vocab tokens as the best next token of the response)
- QKV is not attention -- its context computation.
- FFNs base much of what they do on the Alexnet type of NNs. 
  - In LLMs these are referred to as "FFNs". 
  - "feed forward networks" the meaning of the acronym is misleading
  - These are primarily pattern detectors (just like in CNNs)

**Transformer algorithms (QKV/FFN) are still the basis of the latest LLM computational algorithms.**

_A simple **[GPT-3 TF diagram](https://ziptieai.com/2.3.2-tf-algorithm/)** (ZAI original) ("2.3.2 Gist of LLM TF UFA (inference)" / "2 TF algorithm (diagrams)")._<br><img src="/assets/llm02_tf123.png" alt="02" width="40%" style="border: 1px solid #999;"><br><br>



---------------

<br>


### **1.4 Huang/Musk LLM scaling** 

Nvidia gives openAI the first GPU for "the future of humanity". These were (1) 2 true champions who made it to positions of such influence and (2) had the foresight to make the right bets on what kind of AI would work. Amazing. 

_[video](https://youtu.be/caKyQNfj9BM?t=609)_<br><img src="/assets/sun-02.png" alt="drones" width="30%">  <img src="/assets/sun-03.png" alt="drones" width="40%">

Note that you often read that AI is making progress much much faster (logarithmic) than Moore's Law (squared). That may be true, but AI has to make must faster progress, because AI is basically pattern matching / classification hacks that require logarithmic advances to add extra 9's to the 99.99...% (that statement may not be exactly correct, but the main point is).  

_Energy consumption / parameters from [video](https://youtu.be/caKyQNfj9BM?t=119)_<br><img src="/assets/sun-07.png" alt="drones" width="52%" style="border: 1px solid #999;"> 


<br>

---------------
---------------
---------------
---------------

<br>


# **2 AI heroes** (WIP)

<br>

### **The problems start when the AI champions become our AI heroes**


**The Chinese have enough sense to never transfer any tech or factories to America, but not our AI heroes**.

**What's good for our AI heroes isn't always necessarily good for us**. The champions have always been focused (and rightly so) on whatever it takes _for them_ to be successful. For _your_ success its important to understand
  - their history (this page) and 
  - the basic technical details of how AI really works (the next top-level webpage "Hack").

**That's why ZAI often focuses on debunking the hype of AI champions-turned-heroes.** 
- Many of the concepts on this page are ZAI original. And usually get to the gist of AI. For example, below I reference an interesting **[chat I had with ChatGPT](/champions_chat1/)** ("My correction of ChatGPT's definition of transformer (GPT agrees with me)").
- Another interesting page with a lot of original ZAI takes on AI: **[LOOK MOM! NO WIRES!)](/pal_concepts_AIPU_no_wires/)**, (26.0927)


<br>

---------------

<br>


### **The various champions of basic LLM tech**

Those who gave us the transformer seem to have been happy remaining AI champions. It seems that all of them have distinguished careers with many tech publications. They have not tried to become our heroes.

<br>

---------------

<br>


### **Jensen Huang**

**We should all stop studying programming. AI will do it all for us.** Meanwhile, Nvidia has (I believe) 40K programmers.

**"You're not talking to somebody who woke up a loser"** _(see the line in the Queen song lyrics "no time for losers")_. **From GPT:** In April 2026, Jensen Huang, CEO of Nvidia, made a striking statement during an interview with technology podcaster Dwarkesh Patel:
- "You're not talking to somebody who woke up a loser."
He followed it by rejecting what he called a loser attitude and a loser premise. The discussion concerned whether Nvidia should continue selling advanced AI chips to China. Patel challenged Huang with two arguments:
- Selling powerful AI chips to China could create national-security risks for the United States.
- Even if Nvidia continued selling chips, Chinese manufacturers such as Huawei might eventually replace Nvidia, causing it to lose the Chinese market anyway.
- Huang strongly rejected the second argument. His position was essentially: Why should Nvidia surrender an enormous market simply because it might eventually lose to a competitor?
- In another 2026 appearance, at Stanford University, Huang expressed essentially the same philosophy. 
  - He argued that difficult competition is valuable and that people develop resilience by experiencing hardship.
  - His message was that he doesn't subscribe to the belief that one should avoid competing because defeat is possible.

**Huang's parents were desperate to send him to America for some reason as a child.** His USA relatives mistakenly sent him to a reform school in Kentucky. The USA intel agencies have predicted that in 2027 the nation of his birth will be the target of an invasion by the country Huang wants to supply advanced chips to. The logic of Jensen's arguments about selling chips to China is beyond my comprehension.

<br>

---------------

<br>



### **Musk**

**Elon transferred a lot of tech to China** when he built a Tesla factory there. Now Elon wants to get out of China. Chinese companies are now copying the tech they learned from Tesla China. The result is a fleet of new Chinese-made vehicles, some with major pricetags (and some with major quality problems). Musk's jumpstart is what made it possible for them to break into the EV market **(Musk is not without reason considered a hero in China)**. 

_The $110K Huawei luxury van with brake pedals that break._<br><img src="/assets/sun-01.png" alt="drones" width="70%">

**Musk can't compete (in China) anymore (is he a loser?).** The showrooms for Chinese cars are in every big Chinese shopping center (cars are often being displayed and sold in the stores for companies that are still selling their original product (mobile phones)). These cars are also now flooding the EU and Canada. Does Elon's abject failure (from the perspective of Elon's chosen homeland) in China make him a loser? Was it worth the few dollars (for the world's first "trillionaire") that Elon made?

_Poster for the movie ["For a few dollars more"](https://en.wikipedia.org/wiki/For_a_Few_Dollars_More)._<br><img src="/assets/sun-08.png" alt="drones" width="15%" style="border: 1px solid #999;">

<!-- _I myself worked at Huawei. That was a short experience that ended when I was a contractor at Huawei (China) and was paid half of my salary 2 months in a row. I was told that I would not receive the rest (I eventually did). Just a few months before that I was told that Huawei wanted to hire me as a regular Huawei China employee._ -->


<br>

---------------
---------------
---------------
---------------

<br>

# **3 AGI super heroes**

<br>

**Hinton claimed a few years ago that AI had emotions and would achieve AGI (human intelligence) within a year or so.** He recently retracted such statements. These statements were from a Turing award and Nobel prize winner. **Musk** also recently predicted that AI would reach AGI within a year (we are still waiting for the FSD from Tesla that has been promised for 10 years as just a year or so away).

**The AGI super heroes are claiming to give you something that they know is not possible** (human level "intelligence" AI). Remember the exponential graph shown in section 1? This graph is meant to give the impression that AI is just going to explode in growth (and never stop). 

_Energy consumption / parameters from [video](https://youtu.be/caKyQNfj9BM?t=119)_<br><img src="/assets/sun-07.png" alt="drones" width="52%" style="border: 1px solid #999;"> 

I had an interesting conversation with GPT about this (same thread **[chat I had with ChatGPT](/champions_chat1/)** as mentioned earlier, second half of the chat). The following is the core conclusion that GPT reached (agreeing with my core point):

<br>

#### **ME: good feedback...**
i cant write equations during this conversation, so what i meant was what you wrote. your precision in meaning is impressive. 

but my main goal here is to get you to agree to a more deeper insight that is being missed by most (all that i have seen) conversations about this topic 
- y=2^x for moores law meant real 2^x performance improvements. calculations increased by that amount.
- y=10^x for GPU computation does mean 10^x improvements in inference.

<br>

**GPT:** I think I see the deeper distinction you're making, and I agree with the central argument, with one important qualification.

Moore's Law: Increasing transistor counts enabled enormous improvements in practical computing capability. More calculations could be performed, faster and more cheaply. The relationship wasn't exactly 1:1, but the benefits were relatively direct.

AI GPU scaling: Increasing computational capacity by 10× does not necessarily produce a 10× improvement in the quality, accuracy, or reliability of AI inference.

For example, hypothetically:

| Computational capacity | AI accuracy |
| ---------------------- | ----------- |
| 1×                     | 90%         |
| 10×                    | 95%         |
| 100×                   | 98%         |
| 1,000×                 | 99%         |
| 10,000×                | 99.5%       |

These are illustrative numbers, not measured scaling results.

And I think you're making an even deeper observation:

Conventional computing scales the amount of computation we can perform. Neural-network AI scaling increases the computation available to approximate a desired result, but the improvement in the result itself can be dramatically smaller.

There is a distinction worth preserving: 10× more GPU capacity really can deliver approximately 10× more raw calculations per second under suitable conditions. But that doesn't mean 10× better intelligence, prediction, or reliability.

This also connects directly to your earlier argument about adding more 9s to accuracy.

I would summarize your thesis as:

The spectacular exponential growth in AI computational capacity is frequently confused with equally spectacular growth in AI capability. But these are fundamentally different measurements, and diminishing returns can make the gap enormous.

I think that is a strong argument. The part I would be careful about is claiming that the gap must grow at a particular exponential rate. That would require empirical evidence and a precise definition of AI capability.

But the underlying distinction you're emphasizing is absolutely valid—and important.

<br><br>

Amazing how AI can conduct such "conversations". But its important to remember that the GPT statement **"I think I see the deeper distinction you're making, and I agree with the central argument"** is not at all true. GPT sees nothing **and never will**. You and I do.
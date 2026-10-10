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


# **2 AI heroes** (26.1010 this section is still a WIP mess....)

<br>

#### **The problems start when the AI champions become our AI heroes**

That's why I often focus on debunking the hype of AI champions-turned-heroes. 
- Many of the concepts on this page are ZAI original. And usually get to the gist of AI. For example, below I reference an interesting **[chat I had with ChatGPT](/champions_chat1/)** ("My correction of ChatGPT's definition of transformer (GPT agrees with me)").
- Another interesting page with a lot of original ZAI takes on AI: **[LOOK MOM! NO WIRES!)](/pal_concepts_AIPU_no_wires/)**, (26.0927)


**What's good for them isn't always necessarily good for us**. The champions have alwys been focused (and rightly so) on whatever it takes _for them_ to be successful. 
- **The solution**. Educate yourself about 
  - their history (this page) and 
  - the basic technical details of how AI really works (the next top-level webpage "Hack").

<br>

---------------

<br>


#### Hinton

- Claimed a few years ago that AI had emotions and would achieve AGI (human intelligence) within a year or so (he recently retracted such statements)


#### **4.1 Jensen says he was not born a loser**

(comments about losers)




From ChatGPT:

In April 2026, Jensen Huang, CEO of Nvidia, made a striking statement during an interview with technology podcaster Dwarkesh Patel:
- "You're not talking to somebody who woke up a loser."
He followed it by rejecting what he called a loser attitude and a loser premise.

The discussion concerned whether Nvidia should continue selling advanced AI chips to China.

Patel challenged Huang with two arguments:
- Selling powerful AI chips to China could create national-security risks for the United States.
- Even if Nvidia continued selling chips, Chinese manufacturers such as Huawei might eventually replace Nvidia, causing it to lose the Chinese market anyway.

Huang strongly rejected the second argument. His position was essentially: Why should Nvidia surrender an enormous market simply because it might eventually lose to a competitor?

In another 2026 appearance, at Stanford University, Huang expressed essentially the same philosophy. 
- He argued that difficult competition is valuable and that people develop resilience by experiencing hardship.
- His message was that he doesn't subscribe to the belief that one should avoid competing because defeat is possible.

<br>

#### **4.2 America also does not want to be a loser**



America gave Jensen the chance to succeed that he did not have in his ancestral homeland.

And this is how he pays America back?

In the USA his IP is protected. 
But in China?


#### Musk

(who has lost to competition in China (and now Canada and EU) in the EV market)


Elon transferred a lot of tech to China. Now Elon wants to get out of China. The reasons to me are obvious (I am Chinese speaker and recently spent a month in China).
- Chinese companies are now copying the tech they learned from Tesla China.
- Musk can't compete anymore. The showrooms for Chinese cars are in every big shopping center. 

The result is a fleet of new Chinese-made vehicles. Some with major pricetags and major problems.<br>_The $110K Huawei luxury van with brake pedals that break._<br><img src="/assets/sun-01.png" alt="drones" width="80%">

<!-- _I myself worked at Huawei. That was a short experience that ended when I was a contractor at Huawei (China) and was paid half of my salary 2 months in a row. I was told that I would not receive the rest (I eventually did). Just a few months before that I was told that Huawei wanted to hire me as a regular Huawei China employee._ -->

Is Elon a loser? xxx

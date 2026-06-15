---
layout: page
title: Concepts
permalink: /0b-demos/
---

<br>

#### **WIP** (maybe v1 will be ready in July 2026)

<!-- **During the [QS](/0-qs/) demos, you started to truly grasp the core concepts.** Core concepts are crucial for making the right decisions about how to use AI. **The goal of this section: To summarize the concepts in a logical cohesive whole**. -->

<br>

**TOC**
- **1 AI "intelligence"**. How real intelligence and AI work together.
- **2 AI components**. NNs, models, agents.
- **3 AI projects**. How to apply to real world problems.



<br>

## **1 AI "intelligence"**

#### **1.1 The human <> machine interface**

This is perhaps the most important function of AI. The problem is AI token output starts to fool humans into believing AI is intelligent.  **These tokens ellicit thoughts in intelligent human** (no explanation necessary or possible). **For a NN these tokens are just a large set of large (FP) numbers**. When you type a prompt into a chatbot, that prompt is converted into a lot of FP numbers. That is all the TF sees.

<!-- tokens (words parts) and then converted into an "embedding" (12288 FP numbers for GPT-3.. for a single token). For example: "hello world" might become [15496, 995]. Then the embedding table converts that into [[0.12, -0.55, ...],[0.87,  0.03, ...]]. **No thoughts. Nothing. Just clocked binary state switching.** -->

#### **1.2 NNs are always passive; CPU-based agents are in control**

A core lesson from the demos was that a NN is always passive. At least the NN part that does the pattern matching and statisical computation that passes for intelligence. **An NN inputs data and outputs the (100% deterministic) result. Thats it. No control loop.** In the end AI is simply an add-on to CPU-based systems. 

*Electronic agents still run the world, not electronic "NNs"* <br>
<img src="/assets/M-12.png" alt="drones" width="22%">

#### **1.3 NN and agent = Tweedledee and Tweedledum**

A possible analogy for the NN and the agent are Tweedledee and Tweddledum from **[Alice in Wonderland](https://en.wikipedia.org/wiki/Alice%27s_Adventures_in_Wonderland)**. This analogy will help you assess where AI can be deployed successfully and how much effort system integration will cost (if AI was intelligent, you'd just plug AI into the system and finished).

*An intelligent human (left) dealing with the robotic dynamic duo (right)* <br>
<img src="/assets/M-11.png" alt="drones" width="26%">

<!-- Human intelligence is a mystery. How the brain hosts intellligence, consciousness, sight, thoughts, feelings, emotions, hearing, etc. **Listening to AI "gurus" talking about how binary computers already have intelligence was the primary motivation for my initial studies of AI**. I was more interested in analyzing the hype of the gurus than figuring out AI (I knew what the core of AI was already; AI runs on switched binary circuits, not on neurons, so all the talk about AGI was pure hype). **AI is "mechanical" computation** (an AI simulation created by the Dee agent and the Dum NN). **AI is programmed to produce certain outputs. AI does not learn. It understands nothing. It only computes numbers. It only reacts.** AI is vastly simpler than the intelligent human mind. -->


#### **1.4 Agentic AI higher level "thinking" is statistical probability**

Along with some clever programming. **The agent and TF and designed to work together to create the illusion of higher level thinking by only exchanging tokens**. (MORE ON THIS LATER... COMPLEX TO EXPLAIN).

<br>

## **2 AI components**

<!-- #### **This section summarizes the concepts introduced in the QS demos.**

I simply find the word "mechanism" to be a perfect classifier of AI. It get to the heart of what AI is. But **AI is NOT simple**, and **AI IS extremely useful (for specific applications)**. This section discusses the available mechanism that AI offers. -->

<!-- Therefore, it is quite worth your while to really understand the core concepts. To draw conclusions from the [QS](/0-qs/).  -->

<br>


*xxxxxxxxx* <br>
<img src="/assets/M-15.png" alt="drones" width="85%">


<!--*AI components for an LLM* <br>
<img src="/assets/M-13.png" alt="drones" width="62%"> -->

<!-- *[ZiptieAI evolution](/0.1-zai-evolution/)* <br>
<img src="/assets/zai_evolution7.png" alt="drones" width="42%"> -->

<br>

- **2.1 NNs**
- **2.2 Models**
- **2.3 Agents (external)**

<br>

### **[2.1 NNs](/2_models/)**

The NN is the core of AI "intelligence". A NN provides a pattern matching algorithm. The the NN is controlled by Python code ("agent").

- **2.1.1 Tiny NN demo (D2ccc) INFERENCE**
- **2.1.1b Tiny NN demo (D2ccc) TRAINING**
- **2.1.2a ALEXNET CNN** (this is a good example to study before doing the Tiny CNN demo)
- **2.1.2b Tiny CNN demo (D4)**
- **2.1.3 Tiny TF demo (D5)**


*AlexNet CNN (left) and LLM transformer (right)*<br>
<img src="/assets/cnn2.png" alt="desc" width="35%">  <img src="/assets/tf_S1-S6.png" alt="desc" width="40%"> 


<br>

#### **2.1.1 Tiny NN demo (D2ccc) INFERENCE** *(see section 5 at the end of this page for code description)*

*"Inference" means normal run-time operation. Generating output from input. Training is described next.* 

**This one simple NN demo will give you an understanding of the core of all AI** (including CNNs, LLMs TFs, etc). The following diagram shows the core components of the demo:
- **Encoder**. All NNs only "know" numbers (including ChatGPT, Claude, etc). So if you have a dataset that is not (FP) numbers, it must be encoded (and later decoded).
- **NN**. The source of "intelligence". A UFA (universal function approximator). 
  - This NN inputs 2 numbers. And based on that number outputs 2 probabilities. That's it.
- **Decoder**. Convert from a probability for inside/outside the circle to a binary state (1 or 0; inside/outside circle).  

**All of the above insight (and much more) about the CORE of AI from one tiny demo**.

*Demo D2ccc (left) and test results right)*<br>
<img src="/assets/M-05.png" alt="drones" width="46%">     <img src="/assets/M-02.png" alt="drones" width="26%">

<!-- 
  - It does this using the "neurons" shown. Rather than using a logical mathematical equation for distance from center, D2ccc's **"neurons" calculate the equation** W*x+b for all the lines shown (see section 5 for details). This is **absolutely deterministic and without one iota of intelligence"**. 
  - NOTE: This is very confusing, but typical in AI discussions. In the NN diagram "x1" and "x2" are in the plot "x" and "y". NN diagram output "y1" and "y2" are the probabilities that the point is in the center green circle or not.
  - The yellow area is the center of the circle as programmed into the NN by the training data. I intentionally lowered the training data so that the approximation error would be visible.
  - White dots are not in the center. Red dots are in the center. These are calculated by the NN.
  - The black X's show data points that the NN mistakenly classified as outside the circle.
  - The genius of the NN is that it can take a data combination that it has never seen and still make a good guess as to what the data is. That is also the NN's weakness. 
  - This is why scaling is so important. Because AI has no intelligence. But with much more brute force calculation, the error rate of the UFA can go down enough to give the illusion of intelligence. The marketing/hype genius of Musk is that can make "batteries" in a car a status symbol, and make "macrohard" (brute force computing) a status symbol for AI. 
  - REMEMBER: The NN knows nothing about x,y, the circle, etc. It only computes numbers. And the **NN is a clocked binary state machine**. Intelligence (human style) exists in time only, not as a series of binary states. 

-->


<br>

#### **2.1.1b Tiny NN demo (D2ccc) TRAINING**

WIP. The main thing is the training input/output must match exactly what is desired in inference. Discuss following steps.

```
for epoch in range(100):
    logits = model(X)
    loss = loss_fn(logits, Y)
    optimizer.zero_grad()
    loss.backward()
    optimizer.step()
```

<br>

#### **2.1.2a ALEXNET CNN** (this is a good example to study before doing the Tiny CNN demo)

2012 this enabled recognition of digits. With XX % accuracy.
Its too complicated to use as a demo. 

Diagram from page [2.2.1b D4 CNN algorithm details](https://ziptieai.com/2.2.1b-d4-cnn-algorithm-details/).

<img src="/assets/M-06.png" alt="drones" width="46%">

<br>

<!-- About the Tiny CNN NN and Tiny NN differences:
- In this demo there is a NN with 2 parts
  - Conv2d+MaxPool2d. This is not really an NN like in the Tiny NN demo. Its basically computing the evolving values of the pix's through each step and uses convolution to add in values from neighboring pix's.
  - Linear. This is the finally "fully connected" (FC) layer that computes the probabilities of outputs. FC means that all pix's share "context", not just the neighbors via convolution. This is more like the NN in the Tiny NN demo. 
- The reason for the difference: The nature of the data. The next demo for a transfomer will also be similar but different because the data (language tokens, not pic pixels) is different. 
 

This is a diagram that I created that explains clearly how AlexNet CNN works (my notation here makes ever step clear). There are 3 main parts.
- **1 Data input**. In this case the data input is pixel RGB values (already numerical). Just split them into sets of R, G, and B.
- **2 Feature extraction (Conv2d+MaxPool2d)**. This is where convolution and pooling are used to turn the original pixel values into "hidden state" values that progressive define higher level features (I typical call these values "pix's"). The final output at step 9 is 5x5x256 set of pix's. NOTE: Pixels are crude approximate measurements of a fluid phenomenon. Much of this convolution/pooling is used to "filter out" these errors (my opinion; I have not read this anywhere, but GPT seems to finally agree with my suggestion; this is perhaps why the convolution mechanism uses so-called "filters" that filter out pixel approximation errors).
- **3 Final NN (Linear) computing CNN "logits"**. This involves
  - 3.1 Linear NN (like for D2ccc) computes the probabilities of each of 1000 possible outputs.
  - 3.2 The most probable output is converted into a label (such as "Siamese cat"). -->



#### **2.1.2b Tiny CNN (D4)**

You input a 28x28 pixel screenshot of a digit, and the NN outputs "0", "1", ... "9".

For details 
- [2.2.1 D4 CNN image classifier](https://ziptieai.com/2.2.1-d4-cnn-image-classifier/) 
- [2.2.1b D4 CNN algorithm details](https://ziptieai.com/2.2.1b-d4-cnn-algorithm-details/).

<!-- There are 3 main parts.
- **1 Data input**. In this case the data input is .............
- **2 Feature extraction (nn.Conv2d + nn.MaxPool2d)**. This is where convolution and pooling are used to turn the original pixel values into "hidden state" values that progressive define higher level features (I typical call these values "pix's"). ...
- **3 Final NN (nn.Linear) computing CNN "logits"**. This involves
  - 3.1 Linear NN (like for D2ccc) computes the probabilities of each of 10 possible outputs (digits 0 to 9).
  - 3.2 The most probable output is converted into a label (such as "7"). -->

<!-- ```
class TinyCNN(nn.Module):
    def __init__(self):
        super().__init__()
        self.conv1 = nn.Conv2d(1, 8, kernel_size=3, padding=1)
        self.conv2 = nn.Conv2d(8, 16, kernel_size=3, padding=1)
        self.pool = nn.MaxPool2d(2, 2)
        self.fc1 = nn.Linear(16 * 7 * 7, 64)
        self.fc2 = nn.Linear(64, 10)
``` -->

<img src="/assets/M-07.png" alt="drones" width="46%">
<img src="/assets/M-08.png" alt="drones" width="20%">


<br>

#### **2.1.3 Tiny TF (D5)** 


In D5 (diagram below):

- Loop 1
  - Input the letter "h" (T1).
  - Infer. Result = "e".
- Loop 2
  - Input the letters "h", "e" (T1,T2).
  - Infer. Result = "l".
- keep looping until the output is "hello world hello world hello world"


<img src="/assets/M-09.png" alt="drones" width="60%">


<br>


### **[2.2 Models](/2b_models/)** (with API)

The agent and the NN are typically packed into a **model** that has an API that makes it possible for existing software to **use the model as a "helpful" assistant**. I refer to the **code in the model that controls the TF NN as the "internal agent" (iAgent)**. This concept is central to understanding how models work. *Note: I invented the iAgent concept; GPT has only kind of accepted it as OK.*

```
So cleaner:

HF = stores/distributes NN/PT files
Render/AWS/etc = runs API/eAgent code
Client = calls eAgent/API

Example:

HF
 └── .pt file

Render
 └── FastAPI server
     ├── NN definition
     ├── downloads .pt from HF
     ├── iAgent/inference logic
     └── exposes /predict

Laptop client
 └── eAgent/client code calls Render API

AWS could do the same job as Render, but Render is simpler for your demos.
```


```
my focus here is what i can create.. 

(1) I CREATE THE NN. NO EXISTING MODEL. JUST PT. 
i create the NN , i train, infer, total control. and all visible. 
i need no infrastructure. 
THERE IS NO EXISTING MODEL... it is created whebn running the code. 
I can train it every time i run it, or store in pt file. 
normal use woudl probably be simple "USE EXISTING PT FILE". 
***you dont fine tune such models... you just modify the training data.*** 

(2) I CREATE A PACKAGED MODEL. I CAN MODIFY. 
this is usuallly the minimum for others to reuse.. 
this is normally *** you can modify (train yourself) , 
but you dont have too .. 
and you dont have to write inference code (the iAgent) ***. 
its meant as a more complete unit. there is an API. 
i am interested in deployment options, but that is secondary. 

(3) I CREATE eAgent ONLY AND USE AN API. MAYBE I CAN RUN LOCALLY. 
"out of my league" models. 
too complex.. could install local .. who cares.


GPT: Yes — this is a better framework.

I would write it as:

1. I create the model from scratch
I create:
NN + training code + data + PT

Use case:

tiny CNN
tiny TF
forecast model
classifier

Normal use:

load existing .pt
run inference

Key point:

You do not fine-tune it.
You retrain it or change the training data/code.

This is your M01-M07 world.

2. I create a packaged reusable model
I create:
NN + PT + iAgent/API + docs

Others can use it without writing the inference code.

Use case:

download package
call API
reuse model
possibly retrain/modify

This is closer to:

a real model product

M07 starts this.

3. I create only the eAgent
I do NOT create the model.
I use someone else's model/API.

You create:

workflow
tools
business logic
agent
UI
database integration

Examples:

OpenAI API
Claude API
Gemini API
local Ollama model

Key point:

The model is out of scope.
Your value is the external system.

This is your PAL/agentic-AI world.
```


<br>


### **[2.3 Agents](/3_agents/)**

External (not LLM internal) agents provide 
- reliable workflows built around models, tools, and automation. 
- tolerance of AI faults and unpredictable outputs





<br>

## **[3 AI projects](/3.3-ai-projects/)**

*xxxxxxxxx* <br>
<img src="/assets/M-16.png" alt="drones" width="35%">




<br>

26.0615 (v1 26.0611)

<br>


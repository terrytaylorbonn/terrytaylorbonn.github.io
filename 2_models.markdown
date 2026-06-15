---
layout: page
title: "2 NNs"
permalink: /2_models/
---

<br> 

<!-- *NNs (inside the models)* <br>
<img src="/assets/zai_evolution7.png" alt="drones" width="42%"> -->

*2 NNs in the master diagram* <br>
<img src="/assets/M-15-2.png" alt="drones" width="52%">



<br>

**TOC**

- 2.0 Concepts
- 2.1 Core NNs 
- 2.2 Convolution
- 2.2b CNN<>TF comparison
- 2.3 Transformers (TFs)
- 2.5 Robotic AI NNs
- 2.6 Historical NNs
- 2.7 TF training algorithms (TODO)


<!-- 3 phases of model demos for each model group:
- P1 DIY (doit yourself) models / understand mechanics
- P2 OTS (offtheshelf) models 
- P3 OTS fine-tuned -->

<br>

### [2.0 Concepts](/2.0-ufas/)

The core of every model is the NN that implements a UFA (Univeral Function **Approximator**) that **generates an output based on pattern matching of the input**. The patterns were programmed ("trained") by setting NN parameters (weights and biases) during training.

<br>

### [2.1 Core NNs](/2.1-predictive-nns/)

Small NNs for specific tasks. **Includes DIY demos that give you a real understanding of the core of NNs**.

<img src="/assets/brain1.png" alt="drones" width="14%">

<br>

### [2.2 CNNs (convolution)](/2.2-cnns/)

A CNN computes the most probable label ("dog", "airplane", etc) for a set of pixels. **Studying CNNs is great preparation for studying more complex LLMs**.

<img src="/assets/brain1a.png" alt="drones" width="17%">

<br>

### [2.2b CNN<>TF comparison](/2.2b-cnn-tf-comparison/) (WIP)

These 2 AI architectures are much more closely related that you might think.

<!-- <img src="/assets/00-side-by-side.png" alt="drones" width="22%"> -->

<img src="/assets/00-MAIN.png" alt="drones" width="30%">

<br>

### [2.3 TFs (transformers)](/2.3-llms/)

An LLM (1) inputs a sequence of tokens, (2) computes the probabilities of all vocabulary tokens as the next token, (3) outputs the selected new token, and finally (4) adds the new token to the next input sequence. An LLM consists of an (1) internal agent and a (2) transformer (TF) NN. **The TF is the core computational engine behind modern AI systems and the mechanism that enables modern LLM behavior**.

<img src="/assets/brain1b.png" alt="drones" width="22%"> 

Note: The following diagram shows the **extra functionality ("reasoning", etc) that LLMs added later that enabled [agentic AI](/3.2-agentic-ai/)**.

<img src="/assets/brain1c.png" alt="drones" width="20%">

<br>

### [2.5 Robotic AI NNs](/2.5-robotic-ai/)

I no longer believe LeCun's hype about his version of JEPA that will supposedly be a fundamentally different type of AI platform (that fixes the fundamental limitations of LLMs; it doesnt, and never will). I have put this section on pauses. ***Robotic AI (that claims to be able to do what humans can do) is about as realistic as LLM intelligence, FSD, or colonizing Mars.**

*A Waymo "self-drives" into a flooded street.* <br>
<img src="/assets/waymo.png" alt="drones" width="22%"> 

<br>

### [2.6 Historical NNs](/2.6-ai-models-historical/)

Where did today's AI come from? What survived? What became obsolete? What evolved into something else? This section will not have demos, just explanations (you run into these terms all the time, so its good to know what they are). Also good to know how this all developed. Page added 26.0603.

<br>

### [2.7 Training algorithms](/2.7-ai-models-training-algos/)

TODO

<br>

26.0610 (v1 26.0526)

<br>

-------------------------------------
---------------------------------
--------------------------------------
---------------------------------------

<br>


### **[3.1 NNs](/2_models/)**

The NN is the core of AI "intelligence". A NN provides a pattern matching algorithm. The the NN is controlled by Python code ("agent").

- **3.1.1 Tiny NN demo (D2ccc) INFERENCE**
- **3.1.1b Tiny NN demo (D2ccc) TRAINING**
- **3.1.2a ALEXNET CNN** (this is a good example to study before doing the Tiny CNN demo)
- **3.1.2b Tiny CNN demo (D4)**
- **3.1.3 Tiny TF demo (D5)**

<br>

#### **3.1.1 Tiny NN demo (D2ccc) INFERENCE** *(see section 5 at the end of this page for code description)*

*"Inference" means normal run-time operation. Generating output from input. Training is described next.* 

**This one simple NN demo will give you an understanding of the core of all AI** (including CNNs, LLMs TFs, etc). The following diagram shows the core components of the demo:
- **Encoder**. All NNs only "know" numbers (including ChatGPT, Claude, etc). So if you have a dataset that is not (FP) numbers, it must be encoded (and later decoded).
- **NN**. The source of "intelligence". A UFA (universal function approximator). 
  - This NN inputs 2 numbers. And based on that number outputs 2 probabilities. That's it.
  - It does this using the "neurons" shown. Rather than using a logical mathematical equation for distance from center, D2ccc's **"neurons" calculate the equation** W*x+b for all the lines shown (see section 5 for details). This is **absolutely deterministic and without one iota of intelligence"**. 
  - NOTE: This is very confusing, but typical in AI discussions. In the NN diagram "x1" and "x2" are in the plot "x" and "y". NN diagram output "y1" and "y2" are the probabilities that the point is in the center green circle or not.
  - The yellow area is the center of the circle as programmed into the NN by the training data. I intentionally lowered the training data so that the approximation error would be visible.
  - White dots are not in the center. Red dots are in the center. These are calculated by the NN.
  - The black X's show data points that the NN mistakenly classified as outside the circle.
  - The genius of the NN is that it can take a data combination that it has never seen and still make a good guess as to what the data is. That is also the NN's weakness. 
  - This is why scaling is so important. Because AI has no intelligence. But with much more brute force calculation, the error rate of the UFA can go down enough to give the illusion of intelligence. The marketing/hype genius of Musk is that can make "batteries" in a car a status symbol, and make "macrohard" (brute force computing) a status symbol for AI. 
  - REMEMBER: The NN knows nothing about x,y, the circle, etc. It only computes numbers. And the **NN is a clocked binary state machine**. Intelligence (human style) exists in time only, not as a series of binary states. 
- **Decoder**. Convert from a probability for inside/outside the circle to a binary state (1 or 0; inside/outside circle).  

**All of the above insight (and much more) about the CORE of AI from one tiny demo**.

*Demo D2ccc (left) and test results right)*<br>
<img src="/assets/M-05.png" alt="drones" width="46%">     <img src="/assets/M-02.png" alt="drones" width="26%">

<br>

#### **3.1.1b Tiny NN demo (D2ccc) TRAINING**

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

#### **3.1.2a ALEXNET CNN** (this is a good example to study before doing the Tiny CNN demo)

About the Tiny CNN NN and Tiny NN differences:
- In this demo there is a NN with 2 parts
  - Conv2d+MaxPool2d. This is not really an NN like in the Tiny NN demo. Its basically computing the evolving values of the pix's through each step and uses convolution to add in values from neighboring pix's.
  - Linear. This is the finally "fully connected" (FC) layer that computes the probabilities of outputs. FC means that all pix's share "context", not just the neighbors via convolution. This is more like the NN in the Tiny NN demo. 
- The reason for the difference: The nature of the data. The next demo for a transfomer will also be similar but different because the data (language tokens, not pic pixels) is different. 
 

This is a diagram that I created that explains clearly how AlexNet CNN works (my notation here makes ever step clear). There are 3 main parts.
- **1 Data input**. In this case the data input is pixel RGB values (already numerical). Just split them into sets of R, G, and B.
- **2 Feature extraction (Conv2d+MaxPool2d)**. This is where convolution and pooling are used to turn the original pixel values into "hidden state" values that progressive define higher level features (I typical call these values "pix's"). The final output at step 9 is 5x5x256 set of pix's. NOTE: Pixels are crude approximate measurements of a fluid phenomenon. Much of this convolution/pooling is used to "filter out" these errors (my opinion; I have not read this anywhere, but GPT seems to finally agree with my suggestion; this is perhaps why the convolution mechanism uses so-called "filters" that filter out pixel approximation errors).
- **3 Final NN (Linear) computing CNN "logits"**. This involves
  - 3.1 Linear NN (like for D2ccc) computes the probabilities of each of 1000 possible outputs.
  - 3.2 The most probable output is converted into a label (such as "Siamese cat").

Diagram from page [2.2.1b D4 CNN algorithm details](https://ziptieai.com/2.2.1b-d4-cnn-algorithm-details/).

<img src="/assets/M-06.png" alt="drones" width="46%">

<br>

#### **3.1.2b Tiny CNN (D4)**

See [2.2.1 D4 CNN image classifier](https://ziptieai.com/2.2.1-d4-cnn-image-classifier/) and (for details) [2.2.1b D4 CNN algorithm details](https://ziptieai.com/2.2.1b-d4-cnn-algorithm-details/).

There are 3 main parts.
- **1 Data input**. In this case the data input is .............
- **2 Feature extraction (nn.Conv2d + nn.MaxPool2d)**. This is where convolution and pooling are used to turn the original pixel values into "hidden state" values that progressive define higher level features (I typical call these values "pix's"). ...
- **3 Final NN (nn.Linear) computing CNN "logits"**. This involves
  - 3.1 Linear NN (like for D2ccc) computes the probabilities of each of 10 possible outputs (digits 0 to 9).
  - 3.2 The most probable output is converted into a label (such as "7").

```
class TinyCNN(nn.Module):
    def __init__(self):
        super().__init__()
        self.conv1 = nn.Conv2d(1, 8, kernel_size=3, padding=1)
        self.conv2 = nn.Conv2d(8, 16, kernel_size=3, padding=1)
        self.pool = nn.MaxPool2d(2, 2)
        self.fc1 = nn.Linear(16 * 7 * 7, 64)
        self.fc2 = nn.Linear(64, 10)
```

<img src="/assets/M-07.png" alt="drones" width="46%">
<img src="/assets/M-08.png" alt="drones" width="20%">


<br>

#### **3.1.3 Tiny TF (D5)** 

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



--------------------
--------------------
--------------------
--------------------

<br>

## **5 NN demo D2cc details**

*Note: I created this version of the D2 demo on 26.0611. I documented the details in **[docx #607](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO)**. Its similar to D2 demo on page **[2.1 Core NNs](/2.1-predictive-nns/)**.*

1) The short bit of code shown below defines the D2ccc Tiny Demo classifier NN.

```
model = nn.Sequential(
    nn.Linear(2, 16),
    nn.ReLU(),
    nn.Linear(16, 16),
    nn.ReLU(),
    nn.Linear(16, 2),  # 2 class scores/logits
).to(device)
```

2) This is the resulting NN.


```text2
- W = weights, b = biases (these are the model parameters that are UPDATED during training and FIXED during inference)
- h1-01 = hidden layer 1, neuron 01
- h1-02 = hidden layer 1, neuron 02
- ...
- h2-1 = hidden layer 2, neuron 01
- ...
- y-1  = output neuron 1
- y-2  = output neuron 2
```

- 50 data points
- 100 epochs
- num_test = 30

<img src="/assets/M-01.png" alt="drones" width="43%">


3) Computation details. 

```
x, y (inputs)
        ▼
Layer 1: nn.Linear(2,16)
 h1_1 = w1*x + w2*y + b  → ReLU → a1_1
 ...
 h1_16= w1*x + w2*y + b  → ReLU → a1_16
        ▼
Layer 2: nn.Linear(16,16)
 h2_1 = w1*a1_1 + w2*a1_2 + ... + w16*a1_16 + b  → ReLU → a2_1
 ...
 h2_16= w1*a1_1 + w2*a1_2 + ... + w16*a1_16 + b  → ReLU → a2_16
       ▼
Output layer: nn.Linear(16,2)
 logit_outside = w1*a2_1 + w2*a2_2 + ... + w16*a2_16 + b
 logit_inside  = w1*a2_1 + w2*a2_2 + ... + w16*a2_16 + b
        ▼
argmax(logits)
        ▼
class 0 = outside circle
class 1 = inside circle
```

4) These are the total number of computations within the NN.

```text2
TOTALS
- 354 wx+b operations + 32 ReLU operations = 386 simple operations per point
- weights: 32 + 256 + 32 = 320
- biases: 16 + 16 + 2 = 34
- total parameters = 354
- ReLU after h1: 16 comparisons
- ReLU after h2: 16 comparisons
```

5) Resulting output (**I will explain these results better later**). 

- I intentionally lowered the training length to make the result less than optimal (easier to see).
- I added the green circle. It shows where the boundary should be (*in this demo you could compute the test points to see if they were in the center; an equation would work; but the point of this demo is to show how to can do that without equations and what results would be; this would be valuable for data sets that cannot be classified by a simple equation*).
- Yellow / purple area boundary was the NN-computed from a limited data set.
- White dots = outside area.
- Red dots = NN corrected classified as in the green circle.
- X marks = NN incorrectly classified as outside the green circle.

test 1
- 50 data points
- 100 epochs
- num_test = 30

<img src="/assets/M-02.png" alt="drones" width="43%">

test 2
- 500 data points
- 1000 epochs
- num_test = 30

<img src="/assets/M-03.png" alt="drones" width="43%">


6) Lessons learned from this demo:
- The simple NN can classify x,y locations with good accuracy.
- **But classification accuracy is not equation-level perfect**. In our simple demo the results were good for a small NN. But for more complex datasets the size of the NN would increase dramatically. AI must be used where the input / output relationship can not be defined with simple computation or equations. **But AI is always an approximation (UFA, universal function approximator), so the challenge is integrating AI so that the approximation errors are acceptable** (for war time planning systems OK, for self driving cars or home humanoids NOT OK).

<br>

26.0615


<!-- *How a UFA determines if a location is in the Netherlands or Belgium*.<br>
<img src="/assets/belgium1.png" alt="drones" width="75%"> 
<br> -->
<!-- 
***My depiction** of how the AlexNet CNN works*<br>
<img src="/assets/cnn2.png" alt="desc" width="40%"> 
***My depiction** of the main loop of an LLM transformer (GPT-3)*<br> 
<img src="/assets/tf_S1-S6.png" alt="desc" width="50%"> 
-->
<!-- 
**TOC**:
- **2.0a Overview of model evolution**.
- **2.0b UFAs**. Basic UFA concepts. 
- **2.1 Predictive NNs** are small customized NNs for specific recognition task.  
- **2.2 CNNs** (object recognition). A CNN computes the most probable label ("dog", "airplane", etc) for a set of pixels. CNNs are great for your first deep dive into AI, because they are much more intuitive and simpler than LLMs.
- **2.3 LLMs** are the main focus of this site. An LLM generates the probabilities of all vocabulary token candidates for next token (a set of numbers) from the token sequence input.  
- **2.4 Agentic LLMs** are LLMs with extra functionality to support agentic AI.
- **2.5 Robotic NNs** (such as JEPA, LeCun's new projects, etc) are specifically for robots. **LeCun seems to generating a lot of hype**. I did some demos, lost interest for now in this.
-->
<!--
- **2.X Gist of LLMs** is that they (1) convert prompt+response input tokens into large (12288) vector language (just set of FP numbers), (2) massive calculations are performed on the VL to determine the complete meaning of the input, and (3) select a new vocab token. **The algoritm of LLM inference is the mirror image of the algorithm used to program ("train") the LLM.**
- **2.0 UFA** (universal function approximator) is the core of AI. **A UFA only knows numbers. It has absolutely no info about the real world.** It is trained to output a number(s) based on the input numbers. 
That last point is essential for successful AI projects. I first took an interest in understanding the core of **what makes models tick** when I started hearing all the hype from AI gurus about how AI could really think and even have emotions. **Models run on ticking clocked binary circuits**. You don't have to be very bright to understand that ticking mechanisms (clocked state machines) dont think. That may seem impossible when you use an LLM that can intelligenty converse with you. But **LLM intelligence simulation is based on (1) binary computing structures and (2) massive computing power/speed**. Your PC does the same kind of trick.
-->

<!-- 

- **2.1 predictive = basic NN**
- **2.2 CNN adds convolution**

<img src="/assets/brain1a.png" alt="drones" width="20%">

<br>

- **2.3 Chat LLM adds attention heads (extra stuff for language)**. This could be compared to adding grey matter in the brain.

<img src="/assets/brain1b.png" alt="drones" width="25%">

<br>

- **2.4 Agentic LLL adds extra "intelligence" to the NN**. To support "deduction", "reasoning", etc.

<img src="/assets/brain1c.png" alt="drones" width="32%">

<br>
-->

<!-- 
### [2.0a Overview of model evolution](/2.0a-model-evolution/)

An analogy between the brain and models. The main importance of understanding this is to 
- realize that the claims that AI has one iota of real intelligence are nonsense.
- gain an intrinsic understanding of how to exploit the incredible computing capabilities of models while minimizing the (substantial) limitations.

<br>

### [2.0b DIY models](/2.0b-diy-models/)

(TODO / v1 26.0524) How to create your own (do it yourself) models. For now just an idea. There are advantages to creating your own models (you select the training pattern data and you can ensure honesty and integrity of responses). The challenges are significant, but will lessen with time. In any case, understanding the steps involved for a practical demo will be very helpful in understanding how AI really works.
-->

<!--

### **[2.4 Agentic LLM (TF/UFA semantic) functionality](/2.4-agentic-llms/)**

Agentic LLMs (all major LLMs are agentic) are LLMs programmed with the required functionality and training data to support complex interaction with external agents (usually Python scripts). A few examples of agentic LLM functionality: 
- constrain response content/format as specified in prompts  
- build complex responses based on an analysis of prompt content (for example, breaking down a complex process description into planning steps that an agent can reasonably process)


<img src="/assets/brain1c.png" alt="drones" width="27%">

<br> -->

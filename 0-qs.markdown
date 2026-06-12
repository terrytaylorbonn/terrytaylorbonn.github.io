---
layout: page
title: QS
permalink: /0-qs/
---

<br>

Quick start guide. 

<br>

*[ZiptieAI evolution](/0.1-zai-evolution/)* <br>
<img src="/assets/zai_evolution7.png" alt="drones" width="42%">




<br>

- **3.1 NNs**
- **3.2 Models**
- **3.3 Agents (external)**
- **5 NN demo D2cc details**

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


<br>


### **[3.2 Models](/2b_models/)** (with API)

The agent and the NN are typically packed into a **model** that has an API that makes it possible for existing software to **use the model as a "helpful" assistant**. I refer to the **code in the model that controls the TF NN as the "internal agent" (iAgent)**. This concept is central to understanding how models work. *Note: I invented the iAgent concept; GPT has only kind of accepted it as OK.*


<br>


### **[3.3 Agents](/3_agents/)**

External (not LLM internal) agents provide 
- reliable workflows built around models, tools, and automation. 
- tolerance of AI faults and unpredictable outputs


<br>

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



26.0612 (v1 26.0611)

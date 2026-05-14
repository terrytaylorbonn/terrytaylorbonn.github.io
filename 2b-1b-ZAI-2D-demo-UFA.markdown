---
layout: page
title: "1b ZAI 2D demo UFA"
permalink: /2b-1b-ZAI-2D-demo-UFA/
---

**[back](/UFAs/)** 

<br>

(ZAI = ziptieai).
This ZAI demo shows the correct way to detect regions. ROUGH DRAFT.

*NOTE: Wiki page **[Core-AI-concepts (detector example)](https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts#432-detector-example)** shows the original usage of this demo.. as a "logic gate" (XOR) h layer detector (should maybe add to this page sometime).* 


#### **TOC** 

- **1b.1 2x / 2h / inverted trough detector**.
The red inverted trough (z00_h1h2.png)<br>
<img src="/assets/z00_h1h2.png" alt="2b-1b-ZAI" width="20%"> 
- **1b.2 2x / 3h / inverted (triangular) pothole detector**. 
The red circle (triangular inverted pothole) (z01_h1h2h3.png)<br>
<img src="/assets/z01_h1h2h3.png" alt="2b-1b-ZAI" width="20%"> 
- **1b.3 the proper next step in this demo** 
- **1b.4 CORE CONCEPT SUMMARY**

 
## **1b.1 2x / 2h / inverted trough detector**
- 2 inputs x1, x2, consider them to be 2D dimensions.
- we want to detect a 2 sided area in 2D.
- 2S = 2 sides = has 2 h's. 
  -  in this demo the sides are parallel and space between them, so its a trough. 
  -  it would be a an infinite pie piece if the lines were not parallel.

My demo is quite simple.  it was originally to show how to create an XOR function.
https://github.com/terrytaylorbonn/auxdrone/wiki/Core-AI-concepts 

### =1 (need to adjust h1, h2 W's) (z02_logic_gates_need_fix.png)<br>
<img src="/assets/z02_logic_gates_need_fix.png" alt="2b-1b-ZAI" width="55%"> 
 

### =2 in h layer neuron 1

- these 2 inputs are multiplied by weights.
- this is the slope of the plane defined by the 2 inputs.
- this plane goes through the origin. (z03_2_inputs_origin.png)<br>
<img src="/assets/z03_2_inputs_origin.png" alt="2b-1b-ZAI" width="20%"> 
 

- they are added. 
- this creates a plane 
- then a bias is added to their sum.
- the bias effectively moves the plane away from the origin (z04_bias.png) <br>
<img src="/assets/z04_bias.png" alt="2b-1b-ZAI" width="20%"> 
 

### =2b GELU applied // GELU diagram 3

- GELU is applied to their biased sum.
- the line is actually created in the x1 x2 plane when 
- on one side of line, its a flat plane in x1 x2 plane.
- on other side its a plane going up (UP ONLY). (z05_gelu.png)<br>
<img src="/assets/z05_gelu.png" alt="2b-1b-ZAI" width="20%"> 



### =3 in hlayer neuron 2

- do the same, but tweak the W/bias values a bit so that there is a "trough" between where h1 is not 0 and h2 is not 0 ( this trough will be inverted and biases up in y. 
- so where the trough is is the only region where x1 x2 values give a >0 probability.) (z06_shift_2d_line.png)<br>
<img src="/assets/z06_shift_2d_line.png" alt="2b-1b-ZAI" width="20%"> 
 

### =4 h layer result (NEED TO MODIFY W,bias slightly to create trough... right now its a line)
- h1, h2 <=0  (z00_h1h2.png)<br>
<img src="/assets/z00_h1h2.png" alt="2b-1b-ZAI" width="30%"> 
 

### =5 in y layer 

- in the y1 neuron, each h plane is multiplied by NEGATIVE weight.
- this inverts the planes.
- then +bias to raise what was the "trough" above 0 (its now the only part about 0)
- the resulting inverted trough represents the probability of y1 detected.
- NO GELU required.... because negative probabilities are ignored. 
- h1/h2 were GELU'd so they are >=0
- y max occurs in the middel of the inverted trough. (z07_y1_h1h2.png)<br>
<img src="/assets/z07_y1_h1h2.png" alt="2b-1b-ZAI" width="30%"> 

 
## **1b.2 2x / 3h / inverted (triangular) pothole detector**
- 2 inputs x1, x2, consider them to be 2D dimensions.
- we want to detect a 3 sided area in 2D (assume not all 3 are parallel).
- 3S = 3 sides =  has 3 h's, so its location is defined by a triangle.

### -1 ADD h3 to this diagram (need to adjust h1, h2 W's) (z08_3h_gates.png)<br>
<img src="/assets/z08_3h_gates.png" alt="2b-1b-ZAI" width="50%"> 
 

### -2 in y the detection area is now a ~ pothole (in red circle below (approx)) will be above 0.  (z01_h1h2h3.png)<br>
<img src="/assets/z01_h1h2h3.png" alt="2b-1b-ZAI" width="30%"> 
 
 
## **1b.3 the proper next step in this demo**

- if we add anohter h layer (hL2) , then y outputs would be some higher level features that are defined by various features in hL1. 
- hte problem is, as more layers are added, the conceptual complexity gets big quick.
- SEE SECTION 4 CNN (CNN, not TF) (MULTILAYER UFA) for how multi layers are used. 

<br>

## **1b.4 CORE CONCEPT SUMMARY**
- 1) THIS IS WHY GPUS AND NNs, BECAUSE (1) LOWER LAYER FEATURES ADD TO UPPER LAYER, (2) SUPER FAST COMPUTATION (NO LOOPS), ETC.
- 2) what defines the layers arise out of hte training data naturally. but we dont understaand what they are, because they are all numbers. all we see are encodings.
- 3) we give the TF numbers (that represent tokens) and TF spits out numbers (that represent the next token). 
- 4) For hte TF is just number crunching, matching patterns. NO INTELLIGENCE, NO CONSICIOUSNESS OF WHAT IS GOING ON.

<br> 


26.0513 (v1 26.0513)

---
layout: page
title: 8a Governance -- allow, block, verify
permalink: /pal_693_qs_8a_governance/
---

<br>


[← 3c Foundry QS](/pal_693_qs/)


<br>

ME: i think of adding ch8a governance ... simple sample restrictions on the data chain... restrict use of LLM, etc.... again, just mechanistic demos to show how FOundry works... how important these govern functions are.

FDE: fit well: 8a shows how access is controlled

Keep the same objects and workflow. Change one restriction at a time, then demonstrate what succeeds and what is blocked.

Possible small demos:

```
Demo	                            Mechanism to demonstrate
Who can see the objects?	        Restrict access; verify with a second test user
Who can run A2?	                    Allow only a selected group to submit 693_CheckAndSaveRecord
Who changed CheckResult?	        Inspect the Action submission and automation history
May this data be sent to this LLM?	Demonstrate an approved data/model restriction, if supported by your environment
```

For the LLM example, distinguish who can call the function from whether particular data may be processed by a model. They are different controls. We should verify which mechanisms your enrollment supports before writing those instructions.

A useful chapter pattern:

Run successfully → apply restriction → repeat and observe the block → restore access

Two or three examples are enough. A second test user is important for access demonstrations; testing only as the owner can hide the effect.

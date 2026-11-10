---
layout: page
title: 8a (7b) Add processing of updated objects to automation
permalink: /pal_693_qs_8a_automate_updated/
---

<br>


[← 3c Foundry QS](/pal_693_qs/)

<br>

ME: i think of adding ch8b real world applications... not actually build anything in this chapter.... insstead, talk about a few real world industry apps in which even the simple demo we built could be used...

FDP: fit well: 8b shows why the mechanics matter.

Use a few short examples, each mapped to the workflow already built:

```
Industry	      Incoming object	    AI operation	                                            Saved response
Manufacturing	  Maintenance report	Identify whether its description mentions overheating    	Classification
Logistics	      Shipment exception	Interpret the description and identify a delay reason	    Delay category
Customer service	Support request	    Identify the issue described by the customer	               Routing category
Procurement	        Supplier submission	 Identify whether the text addresses a specified requirement	Finding for review
```

For each example, show:
- External source → import → object → AI operation → saved property → UI

Explicitly separate what this demo already demonstrates from what a production implementation would additionally need—such as validation, handling updated objects, monitoring, and human review.

That keeps 8b concrete without turning it into another build chapter.


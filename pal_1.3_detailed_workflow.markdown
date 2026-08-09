---
layout: page
title: 1.3 Detailed workflow chats
permalink: /pal_1.3_workflow_chats/
---

<br>

Enterprise AI dev platforms do the heavy lifting of creating an enterprise level AI app. 




<br>


<img src="/assets/777_25.png" alt="drones" width="75%" style="border: 1px solid #999;"><br> 

#### My prompt 

```
Attached is the main diagram for the 
Speedrun: Your First End-to-End Workflow
https://learn.palantir.com/speedrun-your-first-e2e-workflow/1944887 

The TOC for what i did is below. 
in TOC "[1a]" refers to "1a" in the attached diagram.
I also added the text for the steps from section 8.4. 

questions:

(1) Does the diagram match the TOC?
(2) There is no analysis, and no write back to the datasource?
(3) ontology read/write 
   (3.1) i think the pipeline output is read into the ontology objects when the ontology (object type) is created at [3] ???
   (3.2) in 8.4 step 3 the object values are read from the ontology  [3a]  ??
   (3.3) in 8.4 step 8 the new object value is written to the ontology [3b] ??

[1a] 3 Ingestion: Getting Data Into Foundry	14
3.1 Introduction	14
3.2 Manual Upload	15
3.3 [Optional] Deploy Datasets via Marketplace	18
3.4 Conclusion	22
[1b] 4 Transforming the Data (BIG)	23
4.1 Introduction	23
4.2 Create a new Pipeline and add data	24
4.3 Clean Bureau SAS	29
4.4 Clean Office Goods Corp	36
4.5 Join Clean Office Goods with Customer List	39
4.6 Join Clean Bureau with Customer List	45
4.7 Union Datasets	50
4.8 Set a Dataset Output	55
4.9 Finalize and Run Pipeline	57
4.10 Conclusion	61
[3] 5 Creating the Ontology	62
5.1 Introduction	62
5.2 Create your Object (BIG)	63
5.3 Conclusion	77
[5] 6 Building the Workshop Application (BIG)	78
6.1 Introduction	78
6.2 Create the Workshop Module	79
6.3 Add Workshop Title	82
6.4 Create an Object Table	84
6.5 Create Filter	93
6.6 Add Object Details	111
6.7 Rename the Object Table (why soooo many details! this is endless.....)	123
6.8 Configure Sections (more UI chaos!!  .... will it ever end?)	125
6.9 Create Pie Chart	129
6.10 Create Bar Chart	131
6.11 Move Charts to the Top	139
6.12 Configure Object Table	141
6.13 Saving and Viewing your Workshop Module	142
[3b] Configuring Actions	144
7.1 Introduction	144
7.2 Enabling edits to your object	145
7.3 Create the "Assign Order" Action	149
7.4 Finish configuring the Action	156
7.5 Conclusion	159
[5] 8 Making your Workshop Application Operational (TOTAL CONFUSION)	160
8.1 Introduction	160
8.2 Open your Workshop Module (what is VIEW MODE WORKSHOP????)	161
8.3 Add Actions to your Workshop	167
8.4 Test Your New Application (BINGO)	174
1.	Ensure your application is in View mode rather than Edit. If you're in Edit mode you'll see a View button in the top right corner and can click it to enter View mode. 
2.	Navigate to the Filters tool on the far right 
3.	[3a] Under Order ID, paste the following Order ID
8d64e941-799c-4e35-b913-d0e3475c307ec206b101-f8b3-4bbe-a1f4-c674dc3124c8
4.	Select the option from the drop down. This should update your table and charts to only display a singular order
5.	Click on the Order in the Object table   
6.	Click on the Assign button 
7.	In the Action form, remove Alfredo Birns from the Assignee and add Gail Weber 
8.	[3b] Click Submit 
9.	Back viewing your application, you should see a green pop-up at the top of your screen verifying that your Action was implemented. 
10.	In the Object table, also note how the name in the Assignee column has been updated. 
Congrats! You've successfully updated an Object via an Action. 
```

## **FDE RESPONSE**


## (1) Does the diagram match the TOC?

Yes — broadly it matches well.

Mapping:

```text
[1a] Section 3 Ingestion
= local files/manual upload → starting data in Foundry

[1b] Section 4 Transforming the Data
= Pipeline Builder cleans/joins/unions data → output dataset

[3] Section 5 Creating the Ontology
= output dataset becomes ontology object type

[5] Section 6 Building Workshop Application
= Workshop reads ontology objects and displays table/filters/charts/details

[3b] Section 7 Configuring Actions
= define ontology action/write capability

[5 + 3b] Section 8 Operational Workshop
= use UI to execute the action
```

So yes, the diagram matches the TOC.

---

## (2) No analysis and no writeback to datasource?

Correct.

### No separate `4 Analysis`

There are charts in Workshop, but this is mainly:

```text
5 UI / app display
```

not a separate Analysis tool like:

```text
Quiver
Contour
Code Workbook
```

So I would leave `4 Analysis` unhighlighted or “not used.”

### No writeback to original datasource

Correct.

The action updates the ontology/object state, not the original uploaded source files.

So:

```text
UI → Action → Ontology object edit
```

not:

```text
UI → Action → original CSV/source file
```

---

## (3) Ontology read/write

### (3.1) Pipeline output read into ontology when object type is created?

Yes, mostly.

More precise:

```text
Pipeline output dataset
→ object type configured/backed by that dataset
→ ontology objects become available from that dataset
```

So Section 5 creates/configures the object type over the pipeline output dataset.

That is your `3`.

---

### (3.2) Step 8.4.3 object values are read from ontology?

Yes.

In Workshop View mode, when you filter by Order ID:

```text
Workshop filter/table/charts
→ read Order objects from ontology
```

That is:

```text
3a Ontology READ → 5 UI
```

So your `[3a]` tag is correct.

---

### (3.3) Step 8.4.8 new object value written to ontology?

Yes.

When you click Submit on the Assign action:

```text
Workshop action form
→ Ontology Action
→ updates object property Assignee
```

That is:

```text
5 UI → 3b Action WRITE
```

So your `[3b]` tag is correct.

The updated value then appears because Workshop rereads the object:

```text
3b write
→ object state changes
→ 3a read
→ UI table shows updated Assignee
```

---

## Best simple flow for this demo

```text
Local files
→ manual upload
→ Foundry input datasets
→ Pipeline Builder transforms
→ output dataset
→ Ontology object type
→ Workshop app reads objects
→ user submits Assign Order action
→ ontology object is updated
→ Workshop shows updated object
```

## Diagram highlights for this demo

Highlight:

```text
1a Data source / input data
1b Pipeline Builder
3 Ontology
3a Read
3b Action write
5 UI / Workshop
```

Do not highlight:

```text
4 Analysis
2 AI
external datasource writeback
```

Security/governance is background only unless the course explicitly configures permissions/actions security.


26.0809 (v1 26.0702) 


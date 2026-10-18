---
layout: page
title: pal_ontology_management
permalink: /pal_ontology_management/
---

<br>

**[← 3c Enterprise](/pal/)**

<br>

**This page is a WIP** (currently just various thoughts (many **very original**))

(WIP: discuss here about managing ontology while doing the demos, especially object types in order to **stay under the 60 object types limit**... there are no utilities to take care of this!).


<br>

#### **TOC**
xxx


<br>

------------------


<br>


# **GPT CHAT: DELETE non-WWW D2 OBJECT TYPES 26.1017**

### **ME1:  In Foundry demo D02 has ony 1 version now (PIC1)**

_xxx_<br><img src="/assets/sun-33.png" alt="drones" width="46%" style="border: 1px solid #999;">


PIC2 shows the object types from previous versions to delete (in red squares).

_xxx_<br><img src="/assets/sun-34.png" alt="drones" width="46%" style="border: 1px solid #999;">
 

PIC3 shows the link types to delete (in read squares). (1) Link types i believe must be deleted first.

_xxx_<br><img src="/assets/sun-35.png" alt="drones" width="46%" style="border: 1px solid #999;">
 

PIC4 shows the action types to delete (in red squares). (2) After link type delete, then delete action types.

_xxx_<br><img src="/assets/sun-36.png" alt="drones" width="46%" style="border: 1px solid #999;">


(3) Finally delete the object types (my real goal, because I must stay below 60 total for my free trial). 

does this make sense?

GPT1: YES, BUT.....
Yes. Your plan makes sense, and your screenshots show a reasonable cleanup strategy for removing obsolete D02 Ontology resources.
I would make one adjustment to the deletion order.
Recommended order
1.	Delete obsolete Action Types (PIC4). Actions can depend on Object Types and Link Types. Remove those dependencies first.
2.	Delete obsolete Link Types (PIC3). Links depend on the Object Types they connect.
3.	Delete obsolete Object Types (PIC2). This is your actual goal, to reduce the total number of Object Types below your free-trial limit.
In other words:
Action Types → Link Types → Object Types
This is the reverse of the usual dependency direction.
Two things to check
1. Your current D02 resources
PIC1 shows the datasets, pipeline, AIP Logic resources, and other files you want to retain. However, Ontology resources are managed separately and might still be referenced by these files.
Before deleting anything, make sure the old Object Types are not referenced by your current D02 pipeline, AIP Logic, Workshop module, or other resources.
2. The red boxes
Your selections appear internally consistent: the Action Types and Link Types highlighted in red correspond to the obsolete Object Types.
However, I notice that TT2 Chunk and TT2 Chunk WW are different Object Types, so check the exact names and their associated Links and Actions before deleting.
One practical recommendation
Try deleting one obsolete group first:
•	Its Action Types
•	Its Link Type
•	Its two Object Types
Then verify that the Object Type count decreases and your current D02 demo still works.
If Foundry reports a dependency, inspect it before proceeding rather than forcing the deletion.
Bottom line: Your cleanup strategy is sound. I would simply reverse your first two steps: Actions first, Links second, Objects last.

### **ME2: More png's to verify**

 
_xxx_<br><img src="/assets/sun-37.png" alt="drones" width="30%" style="border: 1px solid #999;">

_xxx_<br><img src="/assets/sun-38.png" alt="drones" width="46%" style="border: 1px solid #999;">


_xxx_<br><img src="/assets/sun-39.png" alt="drones" width="46%" style="border: 1px solid #999;">
 
_xxx_<br><img src="/assets/sun-40.png" alt="drones" width="46%" style="border: 1px solid #999;">

 

GPT2: These additional screenshots help. They confirm which Ontology resources

your current D02 demo uses, and they reveal one naming detail worth checking before deletion.
1. Current D02 resources to retain
Resource	Type	Objects
Chunks WWW	Object Type	578
Entities WWW	Object Type	1,012
Entities WWWS ↔ Chunks WWWS	Link Type	—
Create Chunks WWW	Action Type	—
Create Entities WWW	Action Type	—
Delete Entities WWW	Action Type	—
The first screenshot confirms that your current Workshop UI uses Chunks WWW, linked to Entities WWW.
The second and third screenshots confirm the associated Actions and Links.
2. One naming detail
The fourth screenshot shows the Link Type named:
Entities WWWS ↔ Chunks WWWS
But its configuration identifies the underlying Object Types as:
Entities WWW ↔ Chunks WWW
This appears to be the correct link for your current D02 demo, despite the additional S in the Link Type names.
Do not delete this Link Type.
3. Your cleanup plan
I would retain these resources and delete the obsolete versions highlighted in your earlier screenshots.
The deletion order remains:
1.	Obsolete Action Types
2.	Obsolete Link Types
3.	Obsolete Object Types
The screenshots provide good evidence for identifying the current resources, although they don't establish whether other applications depend on the obsolete ones.
4. One additional observation
Your current Link Type uses a dataset-based join, configured as many-to-many.
That is a useful example of your earlier REST/database analogy: Foundry is exposing a relationship between business objects, but the underlying implementation uses dataset columns and object primary keys.
Bottom line: Your current D02 appears to use two Object Types, one Link Type, and three Action Types. The new screenshots support keeping those while cleaning up the older versions.


Step 1: DELETE Obsolete Action Types
Step 2: DELETE Obsolete Link Types
Step 3: DELETE Obsolete Object Types




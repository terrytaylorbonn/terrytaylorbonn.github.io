---
layout: page
title: 1 Fetch MockAPI records and display in UI ("Workshop")
permalink: /pal_693_qs_1_mockapi/
---

<br>


[← 0 First steps](/pal_693_qs_0b_first_steps/)  / [↑ 3c Foundry QS](/pal_693_qs/) / [→ 2 Create AIPLF and UI](/pal_693_qs_2_ailpf/)

_26.1111 16:21 (converted from docx source file to markdown+PNGs by ChatGPT)_

<br>


**TOC**

- **[1.0 What we will build](#section-1-0-what-we-will-build)**
- **[1.1 Create MockAPI records](#section-1-1-create-mockapi-records)**
- **[1.2 Configure the data connection to MockAPI](#section-1-2-configure-the-data-connection-to-mockapi)**
- **[1.3 Fetch MockAPI records through the data connection and store them in a dataset using Python (837)](#section-1-3-fetch-mockapi-records-through-the-data-connection-and-store-them-in-a-dataset-using-python-837)**
- **[1.4 Create ObjectTypes/Objects from the dataset (841)](#section-1-4-create-objecttypes-objects-from-the-dataset-841)**
- **[1.5 Display ObjectType records in a UI (Workshop) table](#section-1-5-display-objecttype-records-in-a-ui-workshop-table)**

<br>

<a id="section-1-0-what-we-will-build"></a>

### **1.0 What we will build**

**Summary**. Bring in a few records from MockAPI and display the record text and numbers in a table. No AI.


<img src="/assets/qs/1_01.png" alt="Chapter 1 screenshot 1" width="88%" style="border: 1px solid #999;">

**Configuration (numbered steps in diagram above)**


- 1.1 MockAPI — three source records
- 1.2 Connection allowing Foundry to read MockAPI (1.2 is connection configuration, not another set of data records. The import uses that connection to fetch the records.)
- 1.3a PY script for importing to the dataset.
- 1.3b Stored dataset (693_MockAPI_Items).
- 1.4 Create object types (ontology) from the dataset.
- 1.5 UI table displays those objects. UI Column-to-property mappings + automatic indexing (Capstone2Record: three objects)
<br>

<a id="section-1-1-create-mockapi-records"></a>

### **1.1 Create MockAPI records**

Keep only the synthetic records needed for this demo: an ID, text, and an integer.


```
[
  {
    "id": "1",
    "text": "text1",
    "integer": 111
  },
  {
    "id": "2",
    "text": "text2",
    "integer": 222
  },
  {
    "id": "3",
    "text": "text3",
    "integer": 333
  }
]
```


<img src="/assets/qs/1_02.png" alt="Chapter 1 screenshot 2" width="50%" style="border: 1px solid #999;">

<br>

<a id="section-1-2-configure-the-data-connection-to-mockapi"></a>

### **1.2 Configure the data connection to MockAPI**

Configure the external connection and explain what access we are allowing. Reuse the existing connection if suitable.


<img src="/assets/qs/1_03.png" alt="Chapter 1 screenshot 3" width="91%" style="border: 1px solid #999;">


<img src="/assets/qs/1_04.png" alt="Chapter 1 screenshot 4" width="98%" style="border: 1px solid #999;">


<img src="/assets/qs/1_05.png" alt="Chapter 1 screenshot 5" width="93%" style="border: 1px solid #999;">

<br>

<a id="section-1-3-fetch-mockapi-records-through-the-data-connection-and-store-them-in-a-dataset-using-python-837"></a>

### **1.3 Fetch MockAPI records through the data connection and store them in a dataset using Python (837)**

Run a small import manually. Check the returned records and column types. Leave recurring fetches off.


<img src="/assets/qs/1_06.png" alt="Chapter 1 screenshot 6" width="69%" style="border: 1px solid #999;">

**Confirmed: the old import reads name and quantity.** We’ll leave it unchanged and create a new import for 693.


<img src="/assets/qs/1_07.png" alt="Chapter 1 screenshot 7" width="87%" style="border: 1px solid #999;">


<img src="/assets/qs/1_08.png" alt="Chapter 1 screenshot 8" width="18%" style="border: 1px solid #999;">


<img src="/assets/qs/1_09.png" alt="Chapter 1 screenshot 9" width="44%" style="border: 1px solid #999;">

Preview.


<img src="/assets/qs/1_10.png" alt="Chapter 1 screenshot 10" width="84%" style="border: 1px solid #999;">


<img src="/assets/qs/1_11.png" alt="Chapter 1 screenshot 11" width="82%" style="border: 1px solid #999;">


<img src="/assets/qs/1_12.png" alt="Chapter 1 screenshot 12" width="17%" style="border: 1px solid #999;">


<img src="/assets/qs/1_13.png" alt="Chapter 1 screenshot 13" width="48%" style="border: 1px solid #999;">


<img src="/assets/qs/1_14.png" alt="Chapter 1 screenshot 14" width="92%" style="border: 1px solid #999;">


<img src="/assets/qs/1_15.png" alt="Chapter 1 screenshot 15" width="69%" style="border: 1px solid #999;">

<br>

<a id="section-1-4-create-objecttypes-objects-from-the-dataset-841"></a>

### **1.4 Create ObjectTypes/Objects from the dataset (841)**

(was "Make the records available as objects")  Yes—**“1.4 Create objects from the dataset”** is better. It says plainly what the reader will do, rather than describing the outcome indirectly.

Connect the imported columns to an object’s ID, text, and integer properties. Keep this backing-data path throughout the demo.

We’ll create **one new object type** for 693, backed directly by this dataset—no CSV combination or datasource replacement.

Proposed configuration:


- **Object type:** Capstone2Record
- **ID:** id
- **Displayed title:** text
- **Numeric property:** integer

<img src="/assets/qs/1_16.png" alt="Chapter 1 screenshot 16" width="45%" style="border: 1px solid #999;">


<img src="/assets/qs/1_17.png" alt="Chapter 1 screenshot 17" width="61%" style="border: 1px solid #999;">


<img src="/assets/qs/1_18.png" alt="Chapter 1 screenshot 18" width="61%" style="border: 1px solid #999;">


<img src="/assets/qs/1_19.png" alt="Chapter 1 screenshot 19" width="61%" style="border: 1px solid #999;">


<img src="/assets/qs/1_20.png" alt="Chapter 1 screenshot 20" width="32%" style="border: 1px solid #999;">

**Leave all three checkboxes unchecked.** We do not need controls to create, modify, or delete records inside Foundry for this first step. Our records will come from **MockAPI**, and the table will display them. We’ll add a specific result-saving operation later when needed. The **who can submit** options are disabled because no Actions are selected—that is expected.


<img src="/assets/qs/1_21.png" alt="Chapter 1 screenshot 21" width="25%" style="border: 1px solid #999;">


<img src="/assets/qs/1_22.png" alt="Chapter 1 screenshot 22" width="95%" style="border: 1px solid #999;">


<img src="/assets/qs/1_23.png" alt="Chapter 1 screenshot 23" width="37%" style="border: 1px solid #999;">


<img src="/assets/qs/1_24.png" alt="Chapter 1 screenshot 24" width="16%" style="border: 1px solid #999;">


<img src="/assets/qs/1_25.png" alt="Chapter 1 screenshot 25" width="93%" style="border: 1px solid #999;">


<img src="/assets/qs/1_26.png" alt="Chapter 1 screenshot 26" width="96%" style="border: 1px solid #999;">

Verified: Capstone2Record now has 3 objects, and all three columns are mapped correctly:


- **Id ← id** — unique identifier
- **Text ← text** — displayed title
- **Integer ← integer** — numeric value

There are **no generated Actions**, and edits are disabled. That is appropriate for our current read-only display.

<br>

<a id="section-1-5-display-objecttype-records-in-a-ui-workshop-table"></a>

### **1.5 Display ObjectType records in a UI (Workshop) table**

Create a minimal application with one table. Verify that the displayed values match MockAPI. **Chapter 1 ends with:** MockAPI records visible in the application—**no AI, buttons, result storage, or automation yet**.


<img src="/assets/qs/1_27.png" alt="Chapter 1 screenshot 27" width="94%" style="border: 1px solid #999;">


<img src="/assets/qs/1_28.png" alt="Chapter 1 screenshot 28" width="32%" style="border: 1px solid #999;">


<img src="/assets/qs/1_29.png" alt="Chapter 1 screenshot 29" width="27%" style="border: 1px solid #999;">


<img src="/assets/qs/1_30.png" alt="Chapter 1 screenshot 30" width="77%" style="border: 1px solid #999;">


<img src="/assets/qs/1_31.png" alt="Chapter 1 screenshot 31" width="84%" style="border: 1px solid #999;">


<img src="/assets/qs/1_32.png" alt="Chapter 1 screenshot 32" width="69%" style="border: 1px solid #999;">


<img src="/assets/qs/1_33.png" alt="Chapter 1 screenshot 33" width="81%" style="border: 1px solid #999;">


<img src="/assets/qs/1_34.png" alt="Chapter 1 screenshot 34" width="51%" style="border: 1px solid #999;">


<img src="/assets/qs/1_35.png" alt="Chapter 1 screenshot 35" width="28%" style="border: 1px solid #999;">


<img src="/assets/qs/1_36.png" alt="Chapter 1 screenshot 36" width="88%" style="border: 1px solid #999;">


<img src="/assets/qs/1_37.png" alt="Chapter 1 screenshot 37" width="36%" style="border: 1px solid #999;">

**Publishing makes the application configuration available; it does not fetch MockAPI again.**

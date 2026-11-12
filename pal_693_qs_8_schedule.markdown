---
layout: page
title: 8 Schedule (Data Lineage) 
permalink: /pal_693_qs_8_schedule/
---

<br>




[← 7 Add automation](/pal_693_qs_7_automation/) / [↑ 3c Foundry QS](/pal_693_qs/) / [→ 8a Add processing of updated objects](/pal_693_qs_8a_automate_updated/)


_26.1110 16:53 (converted from docx source file to markdown+PNGs by ChatGPT)_

<br>

## **8 Schedule (Data Lineage)**

**TOC**

- **[8.0 What we will build](#section-8-0)**
- **[8.0b Accessing applications](#section-8-0b)**
  - **[Build schedules / data lineage](#section-build-schedules-data-lineage)**
  - **[Dataset (not shown in list of applications)](#section-dataset-not-shown-in-list-of-applications)**
- **[8.1 Pause / Delete any existing old schedule](#section-8-1)**
  - **[8.1.1 Pause schedule (pause any schedule you are not using)](#section-8-1-1)**
  - **[8.1.2 Delete schedule](#section-8-1-2)**
- **[8.2 Create new schedule](#section-8-2)**
  - **[1 The schedule builds 693_MockAPI_Items (dataset) every two minutes.](#section-1)**
  - **[2 Each build runs capstone2_items.py (Python script) from 015_MockAPI_Import (repository).](#section-2)**
  - **[3 The script fetches records from MockAPI and writes them into the dataset.](#section-3)**
- **[8.3 Add a MockAPI item with a new (unused) ID](#section-8-3)**
- **[8.4 Trace the result (then pause the schedule)](#section-8-4)**
  - **[8.4.1a Dataset](#section-8-4-1a)**
  - **[8.4.1b Dataset Metrics / Schedule](#section-8-4-1b)**
  - **[8.4.2 Insight](#section-8-4-2)**
  - **[8.4.3 Automation](#section-8-4-3)**
  - **[8.4.4 UI](#section-8-4-4)**
- **[8.5 Test CheckRecord in UI (this is not automation)](#section-8-5)**


<br>

<a id="section-8-0"></a>

### **8.0 What we will build**

<img src="/assets/qs/8_01.png" alt="8 Schedule illustration 1" width="72%" style="border: 1px solid #999;">

Schedule the Python import to fetch MockAPI records into **693_MockAPI_Items every two minutes**.

**The complete flow is:**

- **Scheduled Python import → **
- **dataset update → **
- **new Capstone2Record object → **
- **Chapter 7 automation → **
- **A2 → **
- **AIPLF → **
- **LLM response saved in CheckResult**

**We will:**

- Delete the old build schedule (if exists) and create a new one.
- Add a MockAPI item with a **new, unused Id**.
- Wait for the scheduled import—**without manually clicking Build or running an Action**.
- Verify the new object and its saved **CheckResult** in **Insight**, then verify the successful execution in **Automate**.
- Verify that the new object appears in **693_RecordViewer**.
- Pause the build schedule after testing.

**Note:**

- **Limitation:** the import fetches new and updated records, but the Chapter 7 automation processes **only newly added objects**. Updating an existing object does not trigger another AI operation.
- The separate **8.5 CheckRecord button test** runs the earlier response-only AIPLF from the UI. It does **not** save the response in CheckResult.

**Note: My tabs for this ch8 (all Foundry apps except for MockAPI.io)**

<img src="/assets/qs/8_02.png" alt="8 Schedule illustration 2" width="100%" style="border: 1px solid #999;">

- MockAPI.io
- Data connection
- VS code
- Dataset
- Dataset metrics / schedule
- Data Lineage
- Build Schedules
- Insight
- AIP Logic (AIPL)
- Automation
- Ontology Manager
- Workshop (UI)


<br>

<a id="section-8-0b"></a>

### **8.0b Accessing applications**


<br>

<a id="section-build-schedules-data-lineage"></a>

#### **Build schedules / data lineage**

<img src="/assets/qs/8_03.png" alt="8 Schedule illustration 3" width="52%" style="border: 1px solid #999;">

<img src="/assets/qs/8_04.png" alt="8 Schedule illustration 4" width="73%" style="border: 1px solid #999;">

<img src="/assets/qs/8_05.png" alt="8 Schedule illustration 5" width="68%" style="border: 1px solid #999;">


<br>

<a id="section-dataset-not-shown-in-list-of-applications"></a>

#### **Dataset (not shown in list of applications)**

This section addresses an important gap. 

<img src="/assets/qs/8_06.png" alt="8 Schedule illustration 6" width="52%" style="border: 1px solid #999;">

For the dataset entry, use:

**Open the existing dataset:** In the **OntologyDemo001** project, find and open **693_MockAPI_Items**. Then select **Preview → Schedules**.

<img src="/assets/qs/8_07.png" alt="8 Schedule illustration 7" width="100%" style="border: 1px solid #999;">

  
**Do not use New → Dataset**—that creates another dataset.

<img src="/assets/qs/8_08.png" alt="8 Schedule illustration 8" width="51%" style="border: 1px solid #999;">


<br>

<a id="section-8-1"></a>

### **8.1 Pause / Delete any existing old schedule**


<br>

<a id="section-8-1-1"></a>

#### **8.1.1 Pause schedule (pause any schedule you are not using)**

- In **Data Lineage → Schedules**, open **Schedule d077a76b98**.
- Click **Pause**.
- Verify the schedule shows **Paused**.

Leave **693_AIPL_CR_Automation** active.

<img src="/assets/qs/8_09.png" alt="8 Schedule illustration 9" width="77%" style="border: 1px solid #999;">

<img src="/assets/qs/8_10.png" alt="8 Schedule illustration 10" width="48%" style="border: 1px solid #999;">

<img src="/assets/qs/8_11.png" alt="8 Schedule illustration 11" width="44%" style="border: 1px solid #999;">


<br>

<a id="section-8-1-2"></a>

#### **8.1.2 Delete schedule**

In **Data Lineage**, click **Back to schedules list** at the top of the right-hand panel.

Show that list so we can locate the delete control for **Schedule afe13ab56b**. Leave it paused.

<img src="/assets/qs/8_12.png" alt="8 Schedule illustration 12" width="45%" style="border: 1px solid #999;">

click Edit.

<img src="/assets/qs/8_13.png" alt="8 Schedule illustration 13" width="46%" style="border: 1px solid #999;">

<img src="/assets/qs/8_14.png" alt="8 Schedule illustration 14" width="41%" style="border: 1px solid #999;">

<img src="/assets/qs/8_15.png" alt="8 Schedule illustration 15" width="75%" style="border: 1px solid #999;">

The delete control appearing only after **Edit** certainly made that harder to find.

**The old schedule is deleted:** the panel shows **0 schedules** for **693_MockAPI_Items**.

ME: no UI warning about the delete... only a browser popup.

Correct—the deletion confirmation was a **browser popup**, not a Foundry dialog.


<br>

<a id="section-8-2"></a>

### **8.2 Create new schedule**


<br>

<a id="section-1"></a>

#### **1 The schedule builds 693_MockAPI_Items (dataset) every two minutes.**


<br>

<a id="section-2"></a>

#### **2 Each build runs capstone2_items.py (Python script) from 015_MockAPI_Import (repository).**


<br>

<a id="section-3"></a>

#### **3 The script fetches records from MockAPI and writes them into the dataset.**

*015_MockAPI_Import (repository), showing capstone2_items.py (Python script).*

<img src="/assets/qs/8_16.png" alt="8 Schedule illustration 16" width="82%" style="border: 1px solid #999;">

<img src="/assets/qs/8_17.png" alt="8 Schedule illustration 17" width="55%" style="border: 1px solid #999;">

1 For this new schedule:

- **Schedule description:** Build 693_MockAPI_Items (dataset) every two minutes
- Keep **Targets-only** selected.
- Keep **693_MockAPI_Items (dataset)** as the target resource.
- Under **When to build**, select **At a specific time**.
- Set **Run every → 2 Minutes** and **Starting at → 1 minute past the hour**.

*The screenshot uses the older description “Fetch MockAPI every 2 minutes”; the description is only a label.*

<img src="/assets/qs/8_18.png" alt="8 Schedule illustration 18" width="44%" style="border: 1px solid #999;">

2 Expand **Advanced options** → enable **Force build** and acknowledge its warning.

<img src="/assets/qs/8_19.png" alt="8 Schedule illustration 19" width="44%" style="border: 1px solid #999;">

<img src="/assets/qs/8_20.png" alt="8 Schedule illustration 20" width="44%" style="border: 1px solid #999;">

3 Click **Save** at the top of the above panel. This returns to Data Lineage dialog.

<img src="/assets/qs/8_21.png" alt="8 Schedule illustration 21" width="100%" style="border: 1px solid #999;">

**The new schedule is saved and enabled.**

- **Schedule d077a76b98**
- Force builds **693_MockAPI_Items**
- Every **2 minutes**, at minutes **01, 03, 05, …**
- Timezone: **America/Indianapolis**


<br>

<a id="section-8-3"></a>

### **8.3 Add a MockAPI item with a new (unused) ID**

To test:

1 Add a MockAPI item with a **new, unused Id**, preserving existing items.

<img src="/assets/qs/8_22.png" alt="8 Schedule illustration 22" width="30%" style="border: 1px solid #999;">

<img src="/assets/qs/8_23.png" alt="8 Schedule illustration 23" width="33%" style="border: 1px solid #999;">

**Id 7 is new**, and the existing six items are preserved.

2 Save the MockAPI update, then wait for the scheduled import and automation. 

3 In **Ontology Manager → Capstone2Record**, look for **Id 7**. We expect **Integer = 777** and **CheckResult = FOUND**, using the automation’s criterion **“integer is greater than 100.”**

<img src="/assets/qs/8_24.png" alt="8 Schedule illustration 24" width="16%" style="border: 1px solid #999;">


<br>

<a id="section-8-4"></a>

### **8.4 Trace the result (then pause the schedule)**


<br>

<a id="section-8-4-1a"></a>

#### **8.4.1a Dataset**

**Correction:** I called it **Dataset Preview**, but it is **not listed as a standalone application in your app launcher**.

It is the **dataset viewer**, opened by opening **693_MockAPI_Items** from its project or folder. 

**Open 693_MockAPI_Items → Preview → Schedules.**

<img src="/assets/qs/8_25.png" alt="8 Schedule illustration 25" width="100%" style="border: 1px solid #999;">

<img src="/assets/qs/8_26.png" alt="8 Schedule illustration 26" width="100%" style="border: 1px solid #999;">


<br>

<a id="section-8-4-1b"></a>

#### **8.4.1b Dataset Metrics / Schedule**

<img src="/assets/qs/8_27.png" alt="8 Schedule illustration 27" width="26%" style="border: 1px solid #999;">

<img src="/assets/qs/8_28.png" alt="8 Schedule illustration 28" width="51%" style="border: 1px solid #999;">

<img src="/assets/qs/8_29.png" alt="8 Schedule illustration 29" width="100%" style="border: 1px solid #999;">


<br>

<a id="section-8-4-2"></a>

#### **8.4.2 Insight**

<img src="/assets/qs/8_30.png" alt="8 Schedule illustration 30" width="100%" style="border: 1px solid #999;">


<br>

<a id="section-8-4-3"></a>

#### **8.4.3 Automation**

<img src="/assets/qs/8_31.png" alt="8 Schedule illustration 31" width="100%" style="border: 1px solid #999;">


<br>

<a id="section-8-4-4"></a>

#### **8.4.4 UI**

<img src="/assets/qs/8_32.png" alt="8 Schedule illustration 32" width="35%" style="border: 1px solid #999;">


<br>

<a id="section-8-5"></a>

### **8.5 Test CheckRecord in UI (this is not automation)**

<img src="/assets/qs/8_33.png" alt="8 Schedule illustration 33" width="31%" style="border: 1px solid #999;">

<img src="/assets/qs/8_34.png" alt="8 Schedule illustration 34" width="11%" style="border: 1px solid #999;">

<img src="/assets/qs/8_35.png" alt="8 Schedule illustration 35" width="29%" style="border: 1px solid #999;">

<img src="/assets/qs/8_36.png" alt="8 Schedule illustration 36" width="28%" style="border: 1px solid #999;">

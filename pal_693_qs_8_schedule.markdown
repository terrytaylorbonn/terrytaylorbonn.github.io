---
layout: page
title: 8 Schedule (Data Lineage) 
permalink: /pal_693_qs_8_schedule/
---

<br>

[← 7 Add automation](/pal_693_qs_7_automation/) / [↑ 3c Foundry QS](/pal_693_qs/) / [→ 8a Add processing of updated objects](/pal_693_qs_8a_automate_updated/)

_26.1112 17:32 (converted from docx source file to markdown+PNGs by ChatGPT)_

<br>

<a id="section-8-schedule-data-lineage"></a>


**TOC**

- **[8.0 What we will build](#section-8-0-what-we-will-build)**
- **[8.0b Accessing applications](#section-8-0b-accessing-applications)**
  - **[Build schedules / data lineage](#section-build-schedules-data-lineage)**
  - **[Dataset (not shown in list of applications)](#section-dataset-not-shown-in-list-of-applications)**
- **[8.1 Pause / Delete any existing old schedule](#section-8-1-pause-delete-any-existing-old-schedule)**
  - **[8.1.1 Pause schedule (pause any schedule you are not using)](#section-8-1-1-pause-schedule-pause-any-schedule-you-are-not-using)**
  - **[8.1.2 Delete schedule](#section-8-1-2-delete-schedule)**
- **[8.2 Create new schedule](#section-8-2-create-new-schedule)**
- **[8.3 Add a MockAPI item with a new (unused) ID](#section-8-3-add-a-mockapi-item-with-a-new-unused-id)**
- **[8.4 Trace the result (then pause the schedule)](#section-8-4-trace-the-result-then-pause-the-schedule)**
  - **[8.4.1a Dataset](#section-8-4-1a-dataset)**
  - **[8.4.1b Dataset Metrics / Schedule](#section-8-4-1b-dataset-metrics-schedule)**
  - **[8.4.2 Insight](#section-8-4-2-insight)**
  - **[8.4.3 Automation](#section-8-4-3-automation)**
  - **[8.4.4 UI](#section-8-4-4-ui)**
- **[8.5 Test CheckRecord in UI (this is not automation)](#section-8-5-test-checkrecord-in-ui-this-is-not-automation)**

<br>

<a id="section-8-0-what-we-will-build"></a>

### **8.0 What we will build**

**Summary.** Schedule the Python import to fetch MockAPI records into **693_MockAPI_Items (dataset) every two minutes**. **NOTE: Limitation:** the import fetches new and updated records, but the Chapter 7 automation processes **only newly added objects**. Updating an existing object does not trigger another AI operation.

<img src="/assets/qs/8_01.png" alt="Chapter 8 screenshot 8_01.png" width="72%" style="border: 1px solid #999;">

**Configuration**

1\. Delete the old build schedule, **if one exists**.

2\. Create a new build schedule.

**Workflow**

1\. In **MockAPI**, add an item with a **new, unused Id**, preserving the existing items.

2\. Wait for the scheduled import. **Do not manually click Build or run an Action.**

3\. Trace the result:

  3.1 **Dataset viewer → 693_MockAPI_Items (dataset):** verify the new row.

  3.2 **Data Lineage → build schedule → Metrics & History:** verify a successful scheduled build.

  3.3 **Insight → Capstone2Record objects:** verify the new object and its saved **CheckResult**.

  3.4 **Automate → 693_AIPL_CR_Automation (automation) → history:** verify successful execution for the 3.5 new object.

  3.5 **Workshop → 693_RecordViewer (your UI):** verify the new object appears in the table.

4 In **Data Lineage**, **pause the build schedule** after testing.

<br>

<a id="section-8-0b-accessing-applications"></a>

### **8.0b Accessing applications**

<br>

<a id="section-build-schedules-data-lineage"></a>

#### **Build schedules / data lineage**

<img src="/assets/qs/8_02.png" alt="Chapter 8 screenshot 8_02.png" width="52%" style="border: 1px solid #999;">

<img src="/assets/qs/8_03.png" alt="Chapter 8 screenshot 8_03.png" width="73%" style="border: 1px solid #999;">

<img src="/assets/qs/8_04.png" alt="Chapter 8 screenshot 8_04.png" width="68%" style="border: 1px solid #999;">

<br>

<a id="section-dataset-not-shown-in-list-of-applications"></a>

#### **Dataset (not shown in list of applications)**

This section addresses an important gap.

<img src="/assets/qs/8_05.png" alt="Chapter 8 screenshot 8_05.png" width="52%" style="border: 1px solid #999;">

For the dataset entry, use:  **Open the existing dataset:** In the **OntologyDemo001** project, find and open **693_MockAPI_Items**. Then select **Preview → Schedules**.

<img src="/assets/qs/8_06.png" alt="Chapter 8 screenshot 8_06.png" width="100%" style="border: 1px solid #999;">

**Do not use New → Dataset**—that creates another dataset.

<img src="/assets/qs/8_07.png" alt="Chapter 8 screenshot 8_07.png" width="51%" style="border: 1px solid #999;">

<br>

<a id="section-8-1-pause-delete-any-existing-old-schedule"></a>

### **8.1 Pause / Delete any existing old schedule**

<br>

<a id="section-8-1-1-pause-schedule-pause-any-schedule-you-are-not-using"></a>

#### **8.1.1 Pause schedule (pause any schedule you are not using)**

1\. In **Data Lineage → Schedules**, open **Schedule d077a76b98**.

2\. Click **Pause**.

3\. Verify the schedule shows **Paused**.

Leave **693_AIPL_CR_Automation** active.

<img src="/assets/qs/8_08.png" alt="Chapter 8 screenshot 8_08.png" width="77%" style="border: 1px solid #999;">

<img src="/assets/qs/8_09.png" alt="Chapter 8 screenshot 8_09.png" width="48%" style="border: 1px solid #999;">

<img src="/assets/qs/8_10.png" alt="Chapter 8 screenshot 8_10.png" width="44%" style="border: 1px solid #999;">

<br>

<a id="section-8-1-2-delete-schedule"></a>

#### **8.1.2 Delete schedule**

In **Data Lineage**, click **Back to schedules list** at the top of the right-hand panel.

Show that list so we can locate the delete control for **Schedule afe13ab56b**. Leave it paused.

<img src="/assets/qs/8_11.png" alt="Chapter 8 screenshot 8_11.png" width="45%" style="border: 1px solid #999;">

Click Edit.

<img src="/assets/qs/8_12.png" alt="Chapter 8 screenshot 8_12.png" width="46%" style="border: 1px solid #999;">

<img src="/assets/qs/8_13.png" alt="Chapter 8 screenshot 8_13.png" width="41%" style="border: 1px solid #999;">

<img src="/assets/qs/8_14.png" alt="Chapter 8 screenshot 8_14.png" width="75%" style="border: 1px solid #999;">

The delete control appearing only after **Edit** certainly made that harder to find. **The old schedule is deleted:** the panel shows **0 schedules** for **693_MockAPI_Items**.

<br>

<a id="section-8-2-create-new-schedule"></a>

### **8.2 Create new schedule**

1\. The schedule builds 693_MockAPI_Items (dataset) every two minutes.

2\. Each build runs capstone2_items.py (Python script) from 015_MockAPI_Import (repository).

3\. The script fetches records from MockAPI and writes them into the dataset.

*015_MockAPI_Import (repository), showing capstone2_items.py (Python script).*

<img src="/assets/qs/8_15.png" alt="Chapter 8 screenshot 8_15.png" width="82%" style="border: 1px solid #999;">

<img src="/assets/qs/8_16.png" alt="Chapter 8 screenshot 8_16.png" width="55%" style="border: 1px solid #999;">

4\. For this new schedule:

**- Schedule description:** Build 693_MockAPI_Items (dataset) every two minutes

- Keep **Targets-only** selected.
- Keep **693_MockAPI_Items (dataset)** as the target resource.
- Under **When to build**, select **At a specific time**.
- Set **Run every → 2 Minutes** and **Starting at → 1 minute past the hour**.

*The screenshot uses the older description “Fetch MockAPI every 2 minutes”; the description is only a label.*

<img src="/assets/qs/8_17.png" alt="Chapter 8 screenshot 8_17.png" width="44%" style="border: 1px solid #999;">

2 Expand **Advanced options** → enable **Force build** and acknowledge its warning.

<img src="/assets/qs/8_18.png" alt="Chapter 8 screenshot 8_18.png" width="44%" style="border: 1px solid #999;">

<img src="/assets/qs/8_19.png" alt="Chapter 8 screenshot 8_19.png" width="44%" style="border: 1px solid #999;">

3 Click **Save** at the top of the above panel. This returns to Data Lineage dialog.

<img src="/assets/qs/8_20.png" alt="Chapter 8 screenshot 8_20.png" width="44%" style="border: 1px solid #999;">

**The new schedule is saved and enabled.**

**- Schedule d077a76b98**

- Force builds **693_MockAPI_Items**
- Every **2 minutes**, at minutes **01, 03, 05, …**
- Timezone: **America/Indianapolis**
<br>

<a id="section-8-3-add-a-mockapi-item-with-a-new-unused-id"></a>

### **8.3 Add a MockAPI item with a new (unused) ID**

To test:

1\. Add a MockAPI item with a **new, unused Id**, preserving existing items.

<img src="/assets/qs/8_21.png" alt="Chapter 8 screenshot 8_21.png" width="30%" style="border: 1px solid #999;">

<img src="/assets/qs/8_22.png" alt="Chapter 8 screenshot 8_22.png" width="33%" style="border: 1px solid #999;">

**Id 7 is new**, and the existing six items are preserved.

2\.  Save the MockAPI update, then wait for the scheduled import and automation.

3\. In **Ontology Manager → Capstone2Record**, look for **Id 7**. We expect **Integer = 777** and **CheckResult = FOUND**, using the automation’s criterion **“integer is greater than 100.”**

<img src="/assets/qs/8_23.png" alt="Chapter 8 screenshot 8_23.png" width="16%" style="border: 1px solid #999;">

<br>

<a id="section-8-4-trace-the-result-then-pause-the-schedule"></a>

### **8.4 Trace the result (then pause the schedule)**

<br>

<a id="section-8-4-1a-dataset"></a>

#### **8.4.1a Dataset**

**Dataset viewer**, opened by opening **693_MockAPI_Items** from its project or folder.  **Open 693_MockAPI_Items → Preview → Schedules.**

<img src="/assets/qs/8_24.png" alt="Chapter 8 screenshot 8_24.png" width="100%" style="border: 1px solid #999;">

<img src="/assets/qs/8_25.png" alt="Chapter 8 screenshot 8_25.png" width="100%" style="border: 1px solid #999;">

<br>

<a id="section-8-4-1b-dataset-metrics-schedule"></a>

#### **8.4.1b Dataset Metrics / Schedule**

<img src="/assets/qs/8_26.png" alt="Chapter 8 screenshot 8_26.png" width="26%" style="border: 1px solid #999;">

<img src="/assets/qs/8_27.png" alt="Chapter 8 screenshot 8_27.png" width="51%" style="border: 1px solid #999;">

<img src="/assets/qs/8_28.png" alt="Chapter 8 screenshot 8_28.png" width="100%" style="border: 1px solid #999;">

<br>

<a id="section-8-4-2-insight"></a>

#### **8.4.2 Insight**

<img src="/assets/qs/8_29.png" alt="Chapter 8 screenshot 8_29.png" width="100%" style="border: 1px solid #999;">

<br>

<a id="section-8-4-3-automation"></a>

#### **8.4.3 Automation**

<img src="/assets/qs/8_30.png" alt="Chapter 8 screenshot 8_30.png" width="100%" style="border: 1px solid #999;">

<br>

<a id="section-8-4-4-ui"></a>

#### **8.4.4 UI**

<img src="/assets/qs/8_31.png" alt="Chapter 8 screenshot 8_31.png" width="35%" style="border: 1px solid #999;">

<br>

<a id="section-8-5-test-checkrecord-in-ui-this-is-not-automation"></a>

### **8.5 Test CheckRecord in UI (this is not automation)**

<img src="/assets/qs/8_32.png" alt="Chapter 8 screenshot 8_32.png" width="31%" style="border: 1px solid #999;">

<img src="/assets/qs/8_33.png" alt="Chapter 8 screenshot 8_33.png" width="11%" style="border: 1px solid #999;">

<img src="/assets/qs/8_34.png" alt="Chapter 8 screenshot 8_34.png" width="29%" style="border: 1px solid #999;">

<img src="/assets/qs/8_35.png" alt="Chapter 8 screenshot 8_35.png" width="28%" style="border: 1px solid #999;">

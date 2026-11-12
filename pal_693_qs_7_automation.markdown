---
layout: page
title: 7 Add automation -- "(new) object added to set" inits automation 
permalink: /pal_693_qs_7_automation/
---

<br>

[← 6 Add A1/A2 Actions](/pal_693_qs_6_a1_a2/) / [↑ 3c Foundry QS](/pal_693_qs/) / [→ 8 Schedule (Data Lineage)](/pal_693_qs_8_schedule/)

_26.1112 13:37 (converted from docx source file to markdown+PNGs by ChatGPT)_

<br>

<a id="section-7-add-automation-new-object-added-to-set-inits-automation"></a>

Add a record in MockAPI and manually fetch the latest data. Verify that the new record is checked and its answer saved without pressing the checking button.

**TOC**

- **[7.0 What we will build](#section-7-0-what-we-will-build)**
- **[7.1 View AIPL / Usage (from this dialog create AIPLF automation)](#section-7-1-view-aipl-usage-from-this-dialog-create-aiplf-automation)**
- **[7.2 Create the automation 693_AIPL_CR_Automation (auto-activated)](#section-7-2-create-the-automation-693-aipl-cr-automation-auto-activated)**
  - **[7.2.1 Overview / Summary / AIPLF and A2](#section-7-2-1-overview-summary-aiplf-and-a2)**
  - **[7.2.2 Overview / Effects / A2 / Criteria static value](#section-7-2-2-overview-effects-a2-criteria-static-value)**
  - **[7.2.3 Overview / Condition / Objects added (to set) / OT = Capstone2Record](#section-7-2-3-overview-condition-objects-added-to-set-ot-capstone2record)**
  - **[7.2.4 Expand Advanced settings](#section-7-2-4-expand-advanced-settings)**
  - **[7.2.5 Click Summary in the left sidebar.](#section-7-2-5-click-summary-in-the-left-sidebar)**
  - **[7.2.6 Create automation](#section-7-2-6-create-automation)**
- **[7.3 Test](#section-7-3-test)**
  - **[7.3.1 Add MockAPI record](#section-7-3-1-add-mockapi-record)**
  - **[7.3.2 Build dataset 693_MockAPI_Items](#section-7-3-2-build-dataset-693-mockapi-items)**
  - **[7.3.3 Refresh the Capstone2Records table in Object Explorer](#section-7-3-3-refresh-the-capstone2records-table-in-object-explorer)**
  - **[7.3.4 Open 693_AIPL_CR_Automation / execution history.](#section-7-3-4-open-693-aipl-cr-automation-execution-history)**

<br>

<a id="section-7-0-what-we-will-build"></a>

### **7.0 What we will build**

**Summary.** In Ch6, you selected a record (in Insight) and clicked Submit.  This ran** 693_CheckAndSaveRecord** manually. Now We’ll use** Automate** to run that Action when a** new Capstone2Record appears**.

For this chapter, use fixed checking instructions:

```
Match if the integer is greater than 100.
```

We’ll still fetch MockAPI records **manually**. Scheduling the fetch comes in Chapter 8.

<img src="/assets/qs/7_01.png" alt="Chapter 7 screenshot 1" width="77%" style="border: 1px solid #999;">

**Configuration**

7.2 Automation represents the Automate configuration screen (North).

**Workflow**

- Add a record in MockAPI and manually fetch the latest data (with manual dataset build). **Manual fetch → new object → automatic AI check → saved CheckResult**
- Verify that the new record is checked and its answer saved without pressing the checking button. You manually fetched the records, but did **not** manually run the check.

<br>

<a id="section-7-1-view-aipl-usage-from-this-dialog-create-aiplf-automation"></a>

### **7.1 View AIPL / Usage (from this dialog create AIPLF automation)**

Return to **693_AIPL_CheckRecord** in AIP Logic and open** Usage** on the right-hand toolbar. We need the automation controls for the published function and its Action.

<img src="/assets/qs/7_02.png" alt="Chapter 7 screenshot 2" width="50%" style="border: 1px solid #999;">

The panel confirms action **693_CheckAndSaveRecord** uses function** 3.0.0**.

<br>

<a id="section-7-2-create-the-automation-693-aipl-cr-automation-auto-activated"></a>

### **7.2 Create the automation 693_AIPL_CR_Automation (auto-activated)**

Click **Create new automation** under** Create deployment**. We’ll configure it for** new records only**, so updating** CheckResult** does not repeatedly trigger the same check.

<br>

<a id="section-7-2-1-overview-summary-aiplf-and-a2"></a>

#### **7.2.1 Overview / Summary / AIPLF and A2**

<img src="/assets/qs/7_03.png" alt="Chapter 7 screenshot 3" width="32%" style="border: 1px solid #999;">

<img src="/assets/qs/7_04.png" alt="Chapter 7 screenshot 4" width="53%" style="border: 1px solid #999;">

<img src="/assets/qs/7_05.png" alt="Chapter 7 screenshot 5" width="89%" style="border: 1px solid #999;">

The automation already has the right structure:
- **Condition:** a Capstone2Record is added.
- **Effect:** run **A2 693_CheckAndSaveRecord** once for each new record.

The red error says the required **criteria** input is missing. Click** 693_CheckAndSaveRecord** under** Effects** in the left sidebar. We’ll supply:

```
Match if the integer is greater than 100.
```

Leave the security settings alone for now—the screen says configuration errors must be resolved before those settings can be determined.

<br>

<a id="section-7-2-2-overview-effects-a2-criteria-static-value"></a>

#### **7.2.2 Overview / Effects / A2 / Criteria static value**

<img src="/assets/qs/7_06.png" alt="Chapter 7 screenshot 6" width="94%" style="border: 1px solid #999;">

**The effect is configured correctly:**
- **Record:** the newly added Capstone2Record. 
- **Criteria:** fixed text, Match if the integer is greater than 100.
- **Execution:** once for each new record.

Leave parallelization and retries unchanged for this demo.

<br>

<a id="section-7-2-3-overview-condition-objects-added-to-set-ot-capstone2record"></a>

#### **7.2.3 Overview / Condition / Objects added (to set) / OT = Capstone2Record**

Next, click **Objects added** under** Condition** in the left sidebar. We’ll verify which object set is monitored before enabling the automation.

<img src="/assets/qs/7_07.png" alt="Chapter 7 screenshot 7" width="90%" style="border: 1px solid #999;">

**The condition is correct:**
- **Objects added to set**
- Object type: **Capstone2Record**
- **No filters**—monitors the whole type.
- **Live monitoring** — the notice says evaluation begins within a minute of an object change, with processing time afterward.

Because **CheckResult** is not used in a filter, saving an answer won’t make the record leave and re-enter this set.

<br>

<a id="section-7-2-4-expand-advanced-settings"></a>

#### **7.2.4 Expand Advanced settings**

We can check whether existing objects are included when the automation starts.

<img src="/assets/qs/7_08.png" alt="Chapter 7 screenshot 8" width="70%" style="border: 1px solid #999;">

Keep these defaults. Two are especially important:
- Disable automation if cycles are detected — ON: keeps loop protection enabled.
- Ignore changes from backing datasets — OFF: necessary so newly imported MockAPI records can trigger the automation.

There’s no existing-object startup option shown here.

<br>

<a id="section-7-2-5-click-summary-in-the-left-sidebar"></a>

#### **7.2.5 Click Summary in the left sidebar.**

We’ll name the automation and review its security settings before creating it. Enter this **Description**:

```
When a new Capstone2Record appears, run 693_CheckAndSaveRecord with the criteria “Match if the integer is greater than 100.” and save the AI answer in CheckResult.
```

Keep **User scoped security** selected and** Generate shared history events** off for this demo. The summary shows** No action required**, and the effect has a green check.

<img src="/assets/qs/7_09.png" alt="Chapter 7 screenshot 9" width="70%" style="border: 1px solid #999;">

<br>

<a id="section-7-2-6-create-automation"></a>

#### **7.2.6 Create automation**

If a confirmation or activation screen appears, show it before continuing.

<img src="/assets/qs/7_10.png" alt="Chapter 7 screenshot 10" width="40%" style="border: 1px solid #999;">

<img src="/assets/qs/7_11.png" alt="Chapter 7 screenshot 11" width="87%" style="border: 1px solid #999;">

**The automation is created and Active.** It has not triggered yet (**Last triggered: Never**).

<br>

<a id="section-7-3-test"></a>

### **7.3 Test**

<br>

<a id="section-7-3-1-add-mockapi-record"></a>

#### **7.3.1 Add MockAPI record**

In MockAPI, add this record **while preserving the existing three**:

```
{"id":"4","text":"automation test","integer":444}
```

<img src="/assets/qs/7_12.png" alt="Chapter 7 screenshot 12" width="33%" style="border: 1px solid #999;">

**Remember:** MockAPI’s** Data → Update** replaces the entire collection, so don’t paste only this record there.

<br>

<a id="section-7-3-2-build-dataset-693-mockapi-items"></a>

#### **7.3.2 Build dataset 693_MockAPI_Items**

Then manually build the import that produces **693_MockAPI_Items**, as in Chapter 1. Once the new object is indexed, the automation should check it and save** FOUND** because 444 > 100. We’ll verify both the automation’s execution history and record** Id 4**—do not run the check Action manually.

<img src="/assets/qs/7_13.png" alt="Chapter 7 screenshot 13" width="95%" style="border: 1px solid #999;">

**This is where you run the import to fetch the MockAPI records into the dataset.** After adding record **Id 4** in MockAPI:
- Keep **Only this dataset** selected.
- Enable **Force** so the import runs again even if Foundry sees no input changes—the external MockAPI change may not be detected.

<img src="/assets/qs/7_14.png" alt="Chapter 7 screenshot 14" width="21%" style="border: 1px solid #999;">

Click **Build**. Check the dataset preview for **Id 4**. Indexing and the automation run follow afterward.

<img src="/assets/qs/7_15.png" alt="Chapter 7 screenshot 15" width="95%" style="border: 1px solid #999;">

<img src="/assets/qs/7_16.png" alt="Chapter 7 screenshot 16" width="13%" style="border: 1px solid #999;">

<img src="/assets/qs/7_17.png" alt="Chapter 7 screenshot 17" width="55%" style="border: 1px solid #999;">

**The import succeeded:** the stored dataset now includes** Id 4**, automation test, integer** 444**.

<br>

<a id="section-7-3-3-refresh-the-capstone2records-table-in-object-explorer"></a>

#### **7.3.3 Refresh the Capstone2Records table in Object Explorer**

Allow time for indexing and live monitoring, then check whether **Id 4 → CheckResult** becomes** FOUND**.

Do **not** run either Action manually—we’re testing the automation.

<img src="/assets/qs/7_18.png" alt="Chapter 7 screenshot 18" width="95%" style="border: 1px solid #999;">

The new object has the expected saved answer:
- **Id:** 4
- **Text:** automation test
- **Integer:** 444
- **CheckResult:** FOUND

Since you did not run the Action manually, this is evidence that the automation checked the new record.

<br>

<a id="section-7-3-4-open-693-aipl-cr-automation-execution-history"></a>

#### **7.3.4 Open 693_AIPL_CR_Automation / execution history.**

We’ll confirm the Action succeeded for this record before closing Chapter 7.

<img src="/assets/qs/7_19.png" alt="Chapter 7 screenshot 19" width="95%" style="border: 1px solid #999;">

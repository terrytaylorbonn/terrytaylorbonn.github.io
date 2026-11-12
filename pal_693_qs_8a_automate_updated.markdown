---
layout: page
title: 8a (7b) Add processing of updated objects to automation
permalink: /pal_693_qs_8a_automate_updated/
---

<br>



[← 8 Schedule (Data Lineage)](/pal_693_qs_8_schedule/) / [↑ 3c Foundry QS](/pal_693_qs/) / [→ 8b Governance](/pal_693_qs_8b_governance/)

_26.1112 17:00 (converted from docx source file to markdown+PNGs by ChatGPT)_

<br>

<a id="section-8a-7b-add-processing-of-updated-objects-to-automation"></a>


This chapter should have been after ch7. But in this QS version it was done after ch8. A future QS version will fix the order.

**TOC**

- **[8a.0 What we will build](#section-8a-0-what-we-will-build)**
- **[8a.1 Inspect the automation’s trigger options](#section-8a-1-inspect-the-automation-s-trigger-options)**
- **[8a.2 Create a second automation so that the Ch7 automation continues handling new objects](#section-8a-2-create-a-second-automation-so-that-the-ch7-automation-continues-handling-new-objects)**
- **[8a.3 Test an update to an existing object](#section-8a-3-test-an-update-to-an-existing-object)**
- **[8a.4 End to end (add DS build scheduling)](#section-8a-4-end-to-end-add-ds-build-scheduling)**

<br>

<a id="section-8a-0-what-we-will-build"></a>

### **8a.0 What we will build**

The Chapter 7 automation processes **only newly added objects**. Updating an existing object does not trigger another AI operation. Modify in this chapter so that automation processes updated objects.

<img src="/assets/qs/8a_01.png" alt="Chapter 8a screenshot 1" width="77%" style="border: 1px solid #999;">

- **8a is a logical extension of Chapter 7. Run the AI operation again when an object’s Text or Integer changes.** The Chapter 7 automation processes only newly added objects. In this chapter, extend the automation setup to also process existing objects when their **Text or Integer** properties change.
- **Do not trigger on CheckResult changes**, because the AI operation writes that property and could trigger itself repeatedly.
- **Test:** change an existing object’s Integer from **55 to 555**, import the update, and verify that **CheckResult changes from NOT FOUND to FOUND** without manually running an Action.
- Once implemented, update Chapter 8’s limitation note to reflect the added behavior.

<br>

<a id="section-8a-1-inspect-the-automation-s-trigger-options"></a>

### **8a.1 Inspect the automation’s trigger options**

Check the available update triggers before changing the existing automation.

1\. Open **Automate**.

2\. Open **693_AIPL_CR_Automation (automation)**.

3\. Click **Edit**.

<img src="/assets/qs/8a_02.png" alt="Chapter 8a screenshot 2" width="81%" style="border: 1px solid #999;">

4\. Select **Objects added** under **Condition**.

5\. Open the **Objects added to set ▾** dropdown at the top.  Objects modified in a set is the trigger we need.

<img src="/assets/qs/8a_03.png" alt="Chapter 8a screenshot 3" width="82%" style="border: 1px solid #999;">

<br>

<a id="section-8a-2-create-a-second-automation-so-that-the-ch7-automation-continues-handling-new-objects"></a>

### **8a.2 Create a second automation so that the Ch7 automation continues handling new objects**

1\. Close the dropdown.

2\. Leave the editor **without saving changes**.

3\. Return to the automation’s overview and open **Actions**. That menu shows the duplicate/copy options.

<img src="/assets/qs/8a_04.png" alt="Chapter 8a screenshot 4" width="83%" style="border: 1px solid #999;">

4\.  Click **Duplicate**.

5\.  Name the copy **693_AIPL_CR_Updated_Automation (automation)** if prompted. Keep **OntologyDemo001** as its location.

6\.  View the next screen **before activating the copy** so we can change its trigger and select which properties to monitor.

<img src="/assets/qs/8a_05.png" alt="Chapter 8a screenshot 5" width="90%" style="border: 1px solid #999;">

7\. Set **File name** to:693_AIPL_CR_Updated_Automation

8\. Replace **Description** with:

```

When an existing Capstone2Record object's Text or Integer changes, run 693_CheckAndSaveRecord to update CheckResult.

```

9\. Click the pen for  **Object set condition**.

10\. In the dropdown shown, click **Objects modified in a set** at the bottom.

<img src="/assets/qs/8a_06.png" alt="Chapter 8a screenshot 6" width="89%" style="border: 1px solid #999;">

11\. Under **Specify properties to monitor** Select **Only trigger on selected properties**.

12\. Use **Search…** to select **Text** and **Integer** only. **Do not select CheckResult.**

13\. Under **Also trigger when**, uncheck **Objects added to set**—the original automation already handles new objects.

14\. Leave **Objects removed from set** unchecked. View the selected properties before continuing.

<img src="/assets/qs/8a_07.png" alt="Chapter 8a screenshot 7" width="60%" style="border: 1px solid #999;">

15\. **Correct:** only changes to **Integer** or **Text** will trigger this automation. Added and removed objects are unchecked. Next, open **693_CheckAndSaveRecord (A2 Action)** under **Effects**—use its pencil if needed. Verify that **Record** refers to the **modified object**, rather than the previously configured “new object added.”

<img src="/assets/qs/8a_08.png" alt="Chapter 8a screenshot 8" width="90%" style="border: 1px solid #999;">

**The inputs are correct:**

- **- Record:** Capstone2Record modified
- **- Criteria:** Match if the integer is greater than 100.

16\. There is a **Possible cycles** warning. Click or hover over that warning and show its explanation. **Do not create the automation yet**—we should inspect the warning even though we excluded CheckResult from the monitored properties.

<img src="/assets/qs/8a_09.png" alt="Chapter 8a screenshot 9" width="75%" style="border: 1px solid #999;">

The warning says the Action modifies objects in the monitored set. **Our configuration monitors only Text and Integer; A2 writes only CheckResult**, so that write should not retrigger this automation.

17\. **Keep cycle detection enabled.**

18\. Next, open **Condition → Objects modified → Advanced settings** and verify:

- **- Disable automation if cycles are detected:** ON
- **- Ignore changes from backing datasets:** OFF

<img src="/assets/qs/8a_10.png" alt="Chapter 8a screenshot 10" width="65%" style="border: 1px solid #999;">

19\. Then return to **Summary** and show it before creating the automation.

<img src="/assets/qs/8a_11.png" alt="Chapter 8a screenshot 11" width="85%" style="border: 1px solid #999;">

**The configuration is ready:**

- **693_AIPL_CR_Updated_Automation (automation)** monitors changes to **Text and Integer**.
- **693_CheckAndSaveRecord (A2 Action)** receives the modified object.
- Cycle detection is **ON**.
- **- Ignore changes from backing datasets** is **OFF**.
- Summary shows **No action required**.

20\. Click **Create automation** at the bottom right.

21\. Then confirm its status is **Active** before we modify a test record.

<img src="/assets/qs/8a_12.png" alt="Chapter 8a screenshot 12" width="50%" style="border: 1px solid #999;">

<img src="/assets/qs/8a_13.png" alt="Chapter 8a screenshot 13" width="70%" style="border: 1px solid #999;">

**693_AIPL_CR_Updated_Automation (automation) is Active. No events have run yet.**

<br>

<a id="section-8a-3-test-an-update-to-an-existing-object"></a>

### **8a.3 Test an update to an existing object**

1\. In **MockAPI**, change only the integer of existing item **Id 7** from **777 to 77**. Preserve its Id, text, and all other items.

<img src="/assets/qs/8a_14.png" alt="Chapter 8a screenshot 14" width="41%" style="border: 1px solid #999;">

2\. Build **693_MockAPI_Items (dataset)** once, with **Force** enabled, to import the change.

<img src="/assets/qs/8a_15.png" alt="Chapter 8a screenshot 15" width="91%" style="border: 1px solid #999;">

<img src="/assets/qs/8a_16.png" alt="Chapter 8a screenshot 16" width="91%" style="border: 1px solid #999;">

<img src="/assets/qs/8a_17.png" alt="Chapter 8a screenshot 17" width="55%" style="border: 1px solid #999;">

3\. In **Insight**, refresh the **Capstone2Record objects** table. Expected for **Id 7**:

- **- Integer:** 77
- **- CheckResult:** changes from FOUND to NOT FOUND

**4. Do not manually run A2.** We’re testing whether the updated-object automation runs it.

<img src="/assets/qs/8a_18.png" alt="Chapter 8a screenshot 18" width="98%" style="border: 1px solid #999;">

**The update test passed.** In **Insight**, existing object **Id 7** now shows:

- **- Integer:** 77
- **- CheckResult:** NOT FOUND—previously FOUND
- **- Text:** unchanged

5\. Next, open **Automate → 693_AIPL_CR_Updated_Automation (automation) → clock/history icon**.

6\. Select the newest event and verify that **Id 7** triggered it and **693_CheckAndSaveRecord (A2 Action)** completed successfully.

<img src="/assets/qs/8a_19.png" alt="Chapter 8a screenshot 19" width="97%" style="border: 1px solid #999;">

<br>

<a id="section-8a-4-end-to-end-add-ds-build-scheduling"></a>

### **8a.4 End to end (add DS build scheduling)**

The AI operation was automatic, but fetching the changed MockAPI data was manual.  To make the whole flow automatic, resume the **Chapter 8 build schedule for 693_MockAPI_Items (dataset)**:

- **Scheduled dataset build → Python script fetches MockAPI records → object properties update → updated-object automation runs A2 → CheckResult is committed**

The schedule targets the **dataset**, not the data connection.

1\. In **Data Lineage**, open the build schedule for **693_MockAPI_Items (dataset)** and click **Unpause** if paused.

<img src="/assets/qs/8a_20.png" alt="Chapter 8a screenshot 20" width="82%" style="border: 1px solid #999;">

<img src="/assets/qs/8a_21.png" alt="Chapter 8a screenshot 21" width="50%" style="border: 1px solid #999;">

<img src="/assets/qs/8a_22.png" alt="Chapter 8a screenshot 22" width="49%" style="border: 1px solid #999;">

2\. In **MockAPI**, change existing **Id 7** from integer **77 back to 777**.

<img src="/assets/qs/8a_23.png" alt="Chapter 8a screenshot 23" width="36%" style="border: 1px solid #999;">

3\. Wait—**do not manually build or run an Action**.

4\. Verify in **Insight** that Id 7 shows **Integer = 777** and **CheckResult = FOUND**.

<img src="/assets/qs/8a_24.png" alt="Chapter 8a screenshot 24" width="82%" style="border: 1px solid #999;">

<img src="/assets/qs/8a_25.png" alt="Chapter 8a screenshot 25" width="84%" style="border: 1px solid #999;">

5\. Pause the build schedule afterward.

<img src="/assets/qs/8a_26.png" alt="Chapter 8a screenshot 26" width="55%" style="border: 1px solid #999;">

<img src="/assets/qs/8a_27.png" alt="Chapter 8a screenshot 27" width="49%" style="border: 1px solid #999;">

<img src="/assets/qs/8a_28.png" alt="Chapter 8a screenshot 28" width="49%" style="border: 1px solid #999;">

The end-to-end update test passed

- Existing object **Id 7** now has **Integer = 777**.
- **- CheckResult** changed back to **FOUND**.
- The build schedule is now **paused**, as confirmed by the banner.

**Chapter 8a is complete:** new objects are handled by the original automation; changes to existing objects’ **Text or Integer** are handled by the updated-object automation.

---
layout: page
title: 8 Schedule MockAPI DATASET import / Add new Capstone2Record / Trace automation 
permalink: /pal_693_qs_8_schedule/
---

<br>


[← 3c Foundry QS](/pal_693_qs/)

<br>

26.1106 09:33 (converted from docx source file to markdown+PNGs by ChatGPT)


<br>

### **8.0 What we will build**


<img src="/assets/qs/8_01.png" alt="8_schedule illustration 1" width="75%" style="border: 1px solid #999;">

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


<img src="/assets/qs/8_02.png" alt="8_schedule illustration 2" width="75%" style="border: 1px solid #999;">

- MockAPI.io
- Data connection
- VS code
- Dataset
- Data Lineage
- Build Schedules
- Insight
- AIP Logic (AIPL)
- Automation
- Ontology Manager
- Workshop (UI)

<br>

### **8.0b Accessing applications**


<br>

#### **Build schedules / data lineage**


<img src="/assets/qs/8_03.png" alt="8_schedule illustration 3" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8_04.png" alt="8_schedule illustration 4" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8_05.png" alt="8_schedule illustration 5" width="75%" style="border: 1px solid #999;">


<br>

#### **Dataset (not shown in list of applications)**

This section addresses an important gap.


<img src="/assets/qs/8_06.png" alt="8_schedule illustration 6" width="75%" style="border: 1px solid #999;">

For the dataset entry, use:

**Open the existing dataset:** In the **OntologyDemo001** project, find and open **693_MockAPI_Items**. Then select **Preview → Schedules**.


```text
Do not use New → Dataset—that creates another dataset.
```


<img src="/assets/qs/8_07.png" alt="8_schedule illustration 7" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8_08.png" alt="8_schedule illustration 8" width="75%" style="border: 1px solid #999;">


<br>

### **8.1 Pause / Delete any existing old schedule**


<br>

#### **8.1.1 Pause schedule (pause any schedule you are not using)**

- In **Data Lineage → Schedules**, open **Schedule d077a76b98**.
- Click **Pause**.
- Verify the schedule shows **Paused**.
Leave **693_AIPL_CR_Automation** active.


<img src="/assets/qs/8_09.png" alt="8_schedule illustration 9" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8_10.png" alt="8_schedule illustration 10" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8_11.png" alt="8_schedule illustration 11" width="75%" style="border: 1px solid #999;">


<br>

#### **8.1.2 Delete schedule**

In **Data Lineage**, click **Back to schedules list** at the top of the right-hand panel.

Show that list so we can locate the delete control for **Schedule afe13ab56b**. Leave it paused.


<img src="/assets/qs/8_12.png" alt="8_schedule illustration 12" width="75%" style="border: 1px solid #999;">

click Edit.


<img src="/assets/qs/8_13.png" alt="8_schedule illustration 13" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8_14.png" alt="8_schedule illustration 14" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8_15.png" alt="8_schedule illustration 15" width="75%" style="border: 1px solid #999;">

The delete control appearing only after **Edit** certainly made that harder to find.

**The old schedule is deleted:** the panel shows **0 schedules** for **693_MockAPI_Items**.

ME: no UI warning about the delete... only a browser popup.

Correct—the deletion confirmation was a **browser popup**, not a Foundry dialog.


<br>

### **8.2 Click Create new schedule to start fresh.**


<img src="/assets/qs/8_16.png" alt="8_schedule illustration 16" width="40%" style="border: 1px solid #999;">

For this new schedule:

- **Schedule description:** Fetch MockAPI every 2 minutes
- Keep **Targets-only** and **693_MockAPI_Items**.
- Select **At a specific time** → **every 2 minutes**.

<img src="/assets/qs/8_17.png" alt="8_schedule illustration 17" width="40%" style="border: 1px solid #999;">

- Expand **Advanced options** → enable **Force build** and acknowledge its warning.

<img src="/assets/qs/8_18.png" alt="8_schedule illustration 18" width="60%" style="border: 1px solid #999;">


<img src="/assets/qs/8_19.png" alt="8_schedule illustration 19" width="50%" style="border: 1px solid #999;">

- Click **Save** at the top of this panel.

<img src="/assets/qs/8_20.png" alt="8_schedule illustration 20" width="75%" style="border: 1px solid #999;">

**The new schedule is saved and enabled.**

- **Schedule d077a76b98**
- Force builds **693_MockAPI_Items**
- Every **2 minutes**, at minutes **01, 03, 05, …**
- Timezone: **America/Indianapolis**

<br>

### **8.3 Add a MockAPI item with a new, unused Id**

To test it, add a MockAPI item with a **new, unused Id**, preserving existing items. Then wait—**do not click Build or Run Now**.


<img src="/assets/qs/8_21.png" alt="8_schedule illustration 21" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8_22.png" alt="8_schedule illustration 22" width="40%" style="border: 1px solid #999;">

Yes—**Id 7 is new**, and the existing six items are preserved.

Save the MockAPI update, then wait for the scheduled import and automation. **Do not manually build or run an Action.**

In **Ontology Manager → Capstone2Record**, look for **Id 7**. We expect **Integer = 777** and **CheckResult = FOUND**, using the automation’s criterion **“integer is greater than 100.”**


<img src="/assets/qs/8_23.png" alt="8_schedule illustration 23" width="75%" style="border: 1px solid #999;">


<br>

### **8.4 Trace the result (then pause the schedule)**


<br>

#### **8.4.1a Dataset**

**Correction:** I called it **Dataset Preview**, but it is **not listed as a standalone application in your app launcher**.

It is the **dataset viewer**, opened by opening **693_MockAPI_Items** from its project or folder. You don’t need to find a separate app first.

For your directions:

**Open 693_MockAPI_Items → Preview → Schedules.**


<img src="/assets/qs/8_24.png" alt="8_schedule illustration 24" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8_25.png" alt="8_schedule illustration 25" width="75%" style="border: 1px solid #999;">


<br>

#### **8.4.1b Dataset Metrics / Schedule**


<img src="/assets/qs/8_26.png" alt="8_schedule illustration 26" width="50%" style="border: 1px solid #999;">


<img src="/assets/qs/8_27.png" alt="8_schedule illustration 27" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8_28.png" alt="8_schedule illustration 28" width="60%" style="border: 1px solid #999;">


<br>

#### **8.4.2 Insight**


<img src="/assets/qs/8_29.png" alt="8_schedule illustration 29" width="75%" style="border: 1px solid #999;">


<br>

#### **8.4.3 Automation**


<img src="/assets/qs/8_30.png" alt="8_schedule illustration 30" width="50%" style="border: 1px solid #999;">


<br>

#### **8.4.4 UI**


<img src="/assets/qs/8_31.png" alt="8_schedule illustration 31" width="40%" style="border: 1px solid #999;">


<br>

### **8.5 Test CheckRecord in UI (this is not automation)**


<img src="/assets/qs/8_32.png" alt="8_schedule illustration 32" width="60%" style="border: 1px solid #999;">


<img src="/assets/qs/8_33.png" alt="8_schedule illustration 33" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8_34.png" alt="8_schedule illustration 34" width="60%" style="border: 1px solid #999;">


<img src="/assets/qs/8_35.png" alt="8_schedule illustration 35" width="60%" style="border: 1px solid #999;">


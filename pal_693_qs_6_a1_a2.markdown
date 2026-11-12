---
layout: page
title: 6 Add an AIPL call to text-save action (A1 / Ch5) / create AIPLF / create action (A2) to call AIPLF (use in Ch7) 
permalink: /pal_693_qs_6_a1_a2/
---

<br>

[← 5 Add object property and Action](/pal_693_qs_5_property_action/) / [↑ 3c Foundry QS](/pal_693_qs/) / [→ 7 Add automation](/pal_693_qs_7_automation/)

_26.1112 13:37 (converted from docx source file to markdown+PNGs by ChatGPT)_

<br>

<a id="section-6-add-an-aipl-call-to-text-save-action-a1-ch5-create-aiplf-create-action-a2-to-call-aiplf-use-in-ch7"></a>


**TOC**

- **[6.0 What we will build](#section-6-0-what-we-will-build)**
- **[6.1 Add text save action 693_SaveCheckResult (A1) to AIPL (no publish (create AIPLF) yet)](#section-6-1-add-text-save-action-693-savecheckresult-a1-to-aipl-no-publish-create-aiplf-yet)**
  - **[One correction to our Chapter 6 plan: this version returns edits, not a String answer.](#section-one-correction-to-our-chapter-6-plan-this-version-returns-edits-not-a-string-answer)**
- **[6.2 Test AIPL text save (PREVIEW)](#section-6-2-test-aipl-text-save-preview)**
- **[6.3 Publish AIPL (create function (AIPLF))](#section-6-3-publish-aipl-create-function-aiplf)**
- **[6.4 Create 693_CheckAndSaveRecord (A2) (runs AIPLF)](#section-6-4-create-693-checkandsaverecord-a2-runs-aiplf)**
  - **[To apply the function’s proposed edits, it must be called through an Action.](#section-to-apply-the-function-s-proposed-edits-it-must-be-called-through-an-action)**
  - **[Leave Auto upgrade to compatible versions off so the tutorial uses a fixed version.](#section-leave-auto-upgrade-to-compatible-versions-off-so-the-tutorial-uses-a-fixed-version)**
- **[6.5 Test action 693_CheckAndSaveRecord (A2) in Insight](#section-6-5-test-action-693-checkandsaverecord-a2-in-insight)**
- **[6.6 What we built](#section-6-6-what-we-built)**

<br>

<a id="section-6-0-what-we-will-build"></a>

### **6.0 What we will build**

**Summary.**

- Add text save action 693_SaveCheckResult (A1) to AIPL.

- Test AIPL.
- Create function AIPLF.
- Create the AIPLF "wrapper" action 693_CheckAndSaveRecord (A2) (call to run AIPLF).
- Test action A2 (in Insight).

For a chat about the details of why you need to do this, see https://ziptieai.com/pal_693_qs_0a2bbb_a2_aiplf_a1/ .

Configuration diagram (shows the MockAPI to UI chain... UI not shown).

<img src="/assets/qs/6_01.png" alt="Chapter 6 screenshot 1" width="77%" style="border: 1px solid #999;">

Here is a different perspective thats shows the ontology flow clearly. Note the duplicate naming for AIPL and AIPLF (AIPLF is auto-named). *This and the diagram above (like all diagrams in this section) were verified in chats with FDE; FDE pays great attention to details, even if it struggles with big picture concepts).*

<img src="/assets/qs/6_02.png" alt="Chapter 6 screenshot 2" width="84%" style="border: 1px solid #999;">

**Configuration (numbered steps in diagram above)**

- 6.1 Add a call to the text-save action 693_SaveCheckResult (A1) (**green below**) to AIPL 693_AIPL_CheckRecord (no publish (create AIPLF) yet).

    <img src="/assets/qs/6_03.png" alt="Chapter 6 screenshot 3" width="67%" style="border: 1px solid #999;">

- 6.2 Test AIPL (preview) text save.
- 6.3 Publish AIPL (create function AIPLF).
- 6.4 Create 693_CheckAndSaveRecord (A2) (runs AIPLF).
- 6.5 Test action 693_CheckAndSaveRecord (A2) in Insight

**Workflow**. Press one button to perform both steps. Verify the saved answer.
- The AI checks the selected record using the user’s instructions.
- It saves its answer into that record’s **CheckResult** using** 693_SaveCheckResult**.

The application still displays the answer.

<br>

<a id="section-6-1-add-text-save-action-693-savecheckresult-a1-to-aipl-no-publish-create-aiplf-yet"></a>

### **6.1 Add text save action 693_SaveCheckResult (A1) to AIPL (no publish (create AIPLF) yet)**

Open **693_AIPL_CheckRecord** in AIP Logic and show its current workflow. We’ll extend it without changing the published** 2.0.0** version currently used by the application.

We’ll add a **separate saving step after the AI check**, so the AI produces the answer and the workflow passes it to the Action. Keep the prompt—including** “Do not call tools or Actions”**—unchanged. That restriction applies to the AI check, not the separate saving step.

Click the **Ontology ▾** menu under** Add a block** and show the available options.

<img src="/assets/qs/6_04.png" alt="Chapter 6 screenshot 4" width="90%" style="border: 1px solid #999;">

<img src="/assets/qs/6_05.png" alt="Chapter 6 screenshot 5" width="82%" style="border: 1px solid #999;">

Choose **Action**—the first option.

In the new block, select **693_SaveCheckResult**.

<img src="/assets/qs/6_06.png" alt="Chapter 6 screenshot 6" width="83%" style="border: 1px solid #999;">

We’ll then connect its two inputs:

**Capstone2Record** → the record input.** CheckResult** → the** Use LLM** answer.

This adds the saving step; it does not yet apply any changes to records.

<img src="/assets/qs/6_07.png" alt="Chapter 6 screenshot 7" width="29%" style="border: 1px solid #999;">

**Yes—both connections are correct:**

**Capstone2Record → record** selects the record to update.** CheckResult → Use LLM** supplies the AI’s answer to save.

Click outside the dropdown to close it. Then scroll to the bottom **Output** block and show its configuration. We need to configure the workflow to return the proposed** Ontology edits**, rather than only the answer text.

<img src="/assets/qs/6_08.png" alt="Chapter 6 screenshot 8" width="23%" style="border: 1px solid #999;">

**Correct.** The Action block returns** Ontology edits**, so no separate selector is needed here.

<br>

<a id="section-one-correction-to-our-chapter-6-plan-this-version-returns-edits-not-a-string-answer"></a>

#### **One correction to our Chapter 6 plan: this version returns edits, not a String answer.**

We’ll display the saved **CheckResult** in the application instead of binding this version to the existing Markdown answer variable.

<br>

<a id="section-6-2-test-aipl-text-save-preview"></a>

### **6.2 Test AIPL text save (PREVIEW)**

Open the Logic preview and supply:

**record:** Id 1 — one hundred and eleven** criteria:** Match if the integer is greater than 100.

Run the preview and show the result. We expect a proposed change setting **CheckResult** to FOUND; previewing does not itself prove that the value was permanently saved.

<img src="/assets/qs/6_09.png" alt="Chapter 6 screenshot 9" width="83%" style="border: 1px solid #999;">

**The preview passed.**

- The AI returned **FOUND**.
- The saving step proposed changing **CheckResult** from MANUAL TEST → FOUND.
- These edits were **not applied**, as the preview notice confirms.

<br>

<a id="section-6-3-publish-aipl-create-function-aiplf"></a>

### **6.3 Publish AIPL (create function (AIPLF))**

Click **Publish** at the top of AIP Logic. Because the output changed from a String to Ontology edits, use** 3.0.0** if prompted for a version. Show the publishing dialog before confirming so we can check its settings.

Leave **Automatic** selected and** Function visibility** set to** Visible**.

Enter this changelog:

```
Evaluate the record against the supplied criteria and propose saving the AI answer in CheckResult using 693_SaveCheckResult.
```

<img src="/assets/qs/6_10.png" alt="Chapter 6 screenshot 10" width="55%" style="border: 1px solid #999;">

Then click **Publish**. Publishing makes the function available; it** does not apply edits to any records**.

Show the resulting version number once publishing finishes.

<img src="/assets/qs/6_11.png" alt="Chapter 6 screenshot 11" width="55%" style="border: 1px solid #999;">

**Version 3.0.0 is published.**

<br>

<a id="section-6-4-create-693-checkandsaverecord-a2-runs-aiplf"></a>

### **6.4 Create 693_CheckAndSaveRecord (A2) (runs AIPLF)**


<a id="section-to-apply-the-function-s-proposed-edits-it-must-be-called-through-an-action"></a>

#### **To apply the function’s proposed edits, it must be called through an Action.**

Click **Create action**. We’ll name the new Action **693_CheckAndSaveRecord**. This is separate from **693_SaveCheckResult**:
- **SaveCheckResult** saves supplied text.
- **CheckAndSaveRecord** runs the AI check and saves its answer.

Show the creation screen so we can configure it.

<img src="/assets/qs/6_12.png" alt="Chapter 6 screenshot 12" width="52%" style="border: 1px solid #999;">

<img src="/assets/qs/6_13.png" alt="Chapter 6 screenshot 13" width="54%" style="border: 1px solid #999;">

**This configuration is correct:**

- Function: **693_AIPL_CheckRecord**
- Version: **3.0.0**
- record → **Record** Action input
- criteria → **Criteria** Action input

<br>

<a id="section-leave-auto-upgrade-to-compatible-versions-off-so-the-tutorial-uses-a-fixed-version"></a>

#### **Leave Auto upgrade to compatible versions off so the tutorial uses a fixed version.**

Scroll down to the next step to enter the Action’s name and details.

Enter:

```
Action type name
693_CheckAndSaveRecord
```

```
Description
Check the selected Capstone2Record against the supplied criteria using AI, then save the answer in CheckResult. Leave imported properties unchanged.
```

Keep the default icon, then scroll down to the next step.

<img src="/assets/qs/6_14.png" alt="Chapter 6 screenshot 14" width="50%" style="border: 1px solid #999;">

<img src="/assets/qs/6_15.png" alt="Chapter 6 screenshot 15" width="32%" style="border: 1px solid #999;">

<img src="/assets/qs/6_16.png" alt="Chapter 6 screenshot 16" width="29%" style="border: 1px solid #999;">

For this demo, keep:
- **Step 3 — Organization:** allows everyone in this organization to submit the Action, subject to their data permissions.
- **Step 4 — OntologyDemo001:** saves it alongside your existing Action.

Proceed with creation. If an API-name validation error appears, use c2-693-check-and-save-record. This creates the Action definition; it does **not** run the AI or change any records yet.

<img src="/assets/qs/6_17.png" alt="Chapter 6 screenshot 17" width="97%" style="border: 1px solid #999;">

<img src="/assets/qs/6_18.png" alt="Chapter 6 screenshot 18" width="39%" style="border: 1px solid #999;">

<img src="/assets/qs/6_19.png" alt="Chapter 6 screenshot 19" width="43%" style="border: 1px solid #999;">

<img src="/assets/qs/6_20.png" alt="Chapter 6 screenshot 20" width="58%" style="border: 1px solid #999;">

<img src="/assets/qs/6_21.png" alt="Chapter 6 screenshot 21" width="70%" style="border: 1px solid #999;">

**693_CheckAndSaveRecord is saved.** Its overview shows the two inputs—**Record** and** Criteria**—feeding the AI function.

<br>

<a id="section-6-5-test-action-693-checkandsaverecord-a2-in-insight"></a>

### **6.5 Test action 693_CheckAndSaveRecord (A2) in Insight**

Return to the **Capstone2Records table in Object Explorer**, where you ran the manual saving Action.

<img src="/assets/qs/6_22.png" alt="Chapter 6 screenshot 22" width="99%" style="border: 1px solid #999;">

Select **Id 1**.

Open **Actions** and choose** 693_CheckAndSaveRecord**.

<img src="/assets/qs/6_23.png" alt="Chapter 6 screenshot 23" width="42%" style="border: 1px solid #999;">

Enter:

Match if the integer is greater than 100.

Submit. **This runs the AI and writes its answer to CheckResult.**

Refresh the table afterward. We expect **CheckResult** to change from MANUAL TEST to FOUND, with** Text** and** Integer** unchanged.

<img src="/assets/qs/6_24.png" alt="Chapter 6 screenshot 24" width="31%" style="border: 1px solid #999;">

<img src="/assets/qs/6_25.png" alt="Chapter 6 screenshot 25" width="90%" style="border: 1px solid #999;">

**The check-and-save workflow worked.** Record** Id 1** now stores** FOUND** in** CheckResult**, while** Text** and** Integer (111)** remain unchanged. The other records were not modified.

For a second test, run **693_CheckAndSaveRecord** on** Id 1** with:

```
Match if the integer is greater than 200.
```

After submitting, verify that **CheckResult** changes to** NOT FOUND**. This confirms the workflow saves a newly calculated answer rather than always writing FOUND.

<img src="/assets/qs/6_26.png" alt="Chapter 6 screenshot 26" width="99%" style="border: 1px solid #999;">

**The second test passed.** Record** Id 1** now stores NOT FOUND;** Text** and** Integer (111)** remain unchanged. The earlier error was a missing record selection, not a broken workflow.

<br>

<a id="section-6-6-what-we-built"></a>

### **6.6 What we built**

One Action now performs the complete operation:
- **Selected record + checking instructions → AI answer → saved CheckResult**

We verified both outcomes:
- Greater than **100** → FOUND
- Greater than **200** → NOT FOUND** Chapter 6 is complete**, with execution verified in Object Explorer. The existing Workshop button still uses the earlier check-only function.

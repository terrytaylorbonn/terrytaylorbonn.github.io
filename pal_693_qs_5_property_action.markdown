---
layout: page
title: 5 Add an object property and text-save action (A1) to save the LLM response (used in Chapter 6)
permalink: /pal_693_qs_5_property_action/
---

<br>




[← 4 Enter AI matching criteria](/pal_693_qs_4_criteria/) / [↑ 3c Foundry QS](/pal_693_qs/) / [→ 6 Add A1/A2 Actions](/pal_693_qs_6_a1_a2/)


_26.1112 09:08 (converted from docx source file to markdown+PNGs by ChatGPT)_


<br>

<a id="section-5-add-an-object-property-and-text-save-action-a1-to-save-the-llm-response-used-in-chapter-6"></a>

**TOC**

- **[5.0 What we will build](#section-5-0)**
- **[5.1 Add OT Capstone2Record PT CheckResult (to save text)](#section-5-1)**
  - **[5.1.1 Create property CheckResult](#section-5-1-1)**
  - **[5.1.2 Allow edits (saving values) for the ObjectType](#section-5-1-2)**
  - **[5.1.3 Save the OT changes](#section-5-1-3)**
- **[5.2 Create the 693_SaveCheckResult Action to save a String in CheckResult](#section-5-2)**
  - **[5.2.1 Create an Action](#section-5-2-1)**
  - **[5.2.2 Correct the API name](#section-5-2-2)**
  - **[5.2.3 Verify Required ON](#section-5-2-3)**
  - **[5.2.4 Save](#section-5-2-4)**
- **[5.3 Test the Action (using action preview / insight (actual save))](#section-5-3)**
  - **[5.3.1 Action preview (no save to object)](#section-5-3-1)**
  - **[5.3.2 Insight test (actual save to object)](#section-5-3-2)**

<br>

<a id="section-5-0"></a>

### **5.0 What we will build**

**Summary.** Configure and test the saving operation.

<img src="/assets/qs/5_01.png" alt="Chapter 5 screenshot 1" width="75%" style="border: 1px solid #999;">

**Configuration (numbered steps in diagram above)**

- 5.1 Add the CheckResult property to the Capstone2Record object type.
- 5.2 Create the 693_SaveCheckResult Action to save a String in CheckResult.
-5.3 Test the Action using manually entered test text.

**Workflow**

- Select an object + enter test text.
- AI checks a selected **Capstone2Record object** using the supplied criteria.
- The **LLM text response** (FOUND, NOT FOUND, etc.) is saved in that object’s **CheckResult** property using **693_SaveCheckResult**.

<br>

<a id="section-5-1"></a>

### **5.1 Add OT Capstone2Record PT CheckResult (to save text)**

Add an edit-only String property named **CheckResult** to **Capstone2Record**.

<br>

<a id="section-5-1-1"></a>

#### **5.1.1 Create property CheckResult**

We’ll configure **CheckResult** as a single String supplied through edits—not as another column imported from MockAPI.

- Open **Ontology Manager → Capstone2Record → Properties**.

Click Create property.

<img src="/assets/qs/5_02.png" alt="Chapter 5 screenshot 2" width="94%" style="border: 1px solid #999;">

- Set:
- **Name:** CheckResult
- **Description:
- **Base type:** String
- **Allow multiple:** OFF

Values required: OFF—unchecked records can have no answer.

<img src="/assets/qs/5_03.png" alt="Chapter 5 screenshot 3" width="34%" style="border: 1px solid #999;">

<br>

<a id="section-5-1-2"></a>

#### **5.1.2 Allow edits (saving values) for the ObjectType**

- Click **Datasources** in ObjectType1’s left navigation—here, the object type is **Capstone2Record**.
- Find **Edits → Allow edits**.

Turn Allow edits ON. This permits Actions to write object values. It does not change any record or enable inline editing in the UI.

<img src="/assets/qs/5_04.png" alt="Chapter 5 screenshot 4" width="94%" style="border: 1px solid #999;">

<br>

<a id="section-5-1-3"></a>

#### **5.1.3 Save the OT changes**

- Click **Save** in the top toolbar.

Review the changes (add CheckResult and enable edits on Capstone2Record).

<img src="/assets/qs/5_05.png" alt="Chapter 5 screenshot 5" width="89%" style="border: 1px solid #999;">

If no errors appear, click Save to ontology….

<img src="/assets/qs/5_06.png" alt="Chapter 5 screenshot 6" width="33%" style="border: 1px solid #999;">

<img src="/assets/qs/5_07.png" alt="Chapter 5 screenshot 7" width="88%" style="border: 1px solid #999;">

<br>

<a id="section-5-2"></a>

### **5.2 Create the 693_SaveCheckResult Action to save a String in CheckResult**

<br>

<a id="section-5-2-1"></a>

#### **5.2.1 Create an Action**

The action receives one record and answer text, then writes that text into **CheckResult**.

Click + New → Action type.

<img src="/assets/qs/5_08.png" alt="Chapter 5 screenshot 8" width="75%" style="border: 1px solid #999;">

- On the **Object** tab:
  - **Object type:** Capstone2Record

Operation: Modify object(s)

<img src="/assets/qs/5_09.png" alt="Chapter 5 screenshot 9" width="51%" style="border: 1px solid #999;">

- Click **Next**.
- Under **Mapping**, click **Add property → CheckResult**.
- **Left CheckResult:** the stored property.

Right CheckResult: the input text to write into it (Left CheckResult).

<img src="/assets/qs/5_10.png" alt="Chapter 5 screenshot 10" width="52%" style="border: 1px solid #999;">

Click **Next** and enter:

- **Name:** 693_SaveCheckResult

Description: Store supplied answer text in CheckResult on the supplied Capstone2Record. Leave imported properties unchanged.

<img src="/assets/qs/5_11.png" alt="Chapter 5 screenshot 11" width="51%" style="border: 1px solid #999;">

Continue with:

- **Who can submit:** Organization → ziptieai
- **Save location:** OntologyDemo001

Finish the wizard, but **do not finalize the Ontology save yet**. Open **Parameters → CheckResult** and send its settings. We’ll make the answer input required before saving.

<img src="/assets/qs/5_12.png" alt="Chapter 5 screenshot 12" width="39%" style="border: 1px solid #999;">

<img src="/assets/qs/5_13.png" alt="Chapter 5 screenshot 13" width="41%" style="border: 1px solid #999;">

<br>

<a id="section-5-2-2"></a>

#### **5.2.2 Correct the API name**

**The Action’s generated API name is invalid.** Its displayed name can keep the 693_ prefix, but use a letter-first, lower-kebab-case API name.

- Dismiss the warning popup.

On Overview, find API name and click its pencil.

<img src="/assets/qs/5_14.png" alt="Chapter 5 screenshot 14" width="55%" style="border: 1px solid #999;">

Replace 693-save-check-result with:
capstone2-save-check-result
c2-693-save-check-result

<img src="/assets/qs/5_15.png" alt="Chapter 5 screenshot 15" width="44%" style="border: 1px solid #999;">

<img src="/assets/qs/5_16.png" alt="Chapter 5 screenshot 16" width="54%" style="border: 1px solid #999;">

<br>

<a id="section-5-2-3"></a>

#### **5.2.3 Verify Required ON**

Then open **Parameters → CheckResult**:

- **Required:** ON
- **Visible:** ON

Disabled: OFF

<img src="/assets/qs/5_17.png" alt="Chapter 5 screenshot 17" width="99%" style="border: 1px solid #999;">

<br>

<a id="section-5-2-4"></a>

#### **5.2.4 Save**

<img src="/assets/qs/5_18.png" alt="Chapter 5 screenshot 18" width="96%" style="border: 1px solid #999;">

<br>

<a id="section-5-3"></a>

### **5.3 Test the Action (using action preview / insight (actual save))**

<br>

<a id="section-5-3-1"></a>

#### **5.3.1 Action preview (no save to object)**

Run it manually and inspect the stored value. Confirm the original record values remain unchanged. Click **User Interface** in the left sidebar. We’ll use its **Test run** tab to supply record **Id 1** and MANUAL TEST, run the Action, and then verify the stored value.

<img src="/assets/qs/5_19.png" alt="Chapter 5 screenshot 19" width="97%" style="border: 1px solid #999;">

The **Test run** tab displays test results; the form is under **Preview**.

- Select the record with **Id 1**.

Enter MANUAL TEST in CheckResult.

<img src="/assets/qs/5_20.png" alt="Chapter 5 screenshot 20" width="41%" style="border: 1px solid #999;">

Click Submit, then inspect Test run. We’ll check the result before treating this as proof that the value was permanently stored.

<img src="/assets/qs/5_21.png" alt="Chapter 5 screenshot 21" width="43%" style="border: 1px solid #999;">

**The test passed—but nothing was saved.** The notice explicitly says these changes are **not applied** to the Ontology. The proposed result is correct:

- **CheckResult:** MANUAL TEST
- **Text:** one hundred and eleven (unchanged)
- **Integer:** 111 (unchanged)

<br>

<a id="section-5-3-2"></a>

#### **5.3.2 Insight test (actual save to object)**

To finish **5.3**, we still need to run the Action on the actual object and verify storage. Return to **Capstone2Record** using the upper-left back link, then open its **Open in** menu so we can access the objects.

<img src="/assets/qs/5_22.png" alt="Chapter 5 screenshot 22" width="27%" style="border: 1px solid #999;">

<img src="/assets/qs/5_23.png" alt="Chapter 5 screenshot 23" width="99%" style="border: 1px solid #999;">

<img src="/assets/qs/5_24.png" alt="Chapter 5 screenshot 24" width="95%" style="border: 1px solid #999;">

<img src="/assets/qs/5_25.png" alt="Chapter 5 screenshot 25" width="44%" style="border: 1px solid #999;">

<img src="/assets/qs/5_26.png" alt="Chapter 5 screenshot 26" width="94%" style="border: 1px solid #999;">

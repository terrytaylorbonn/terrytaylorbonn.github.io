---
layout: page
title: 8b (8a) Governance (allow, block, verify)
permalink: /pal_693_qs_8b_governance/
---

<br>



[← 8a Add processing of updated objects](/pal_693_qs_8a_automate_updated/) / [↑ 3c Foundry QS](/pal_693_qs/) / [→ 9 Continuing your Foundry education](/pal_693_qs_9_where_next/)

<br>

_26.1110 17:04 (converted from docx source file to markdown+PNGs by ChatGPT)_

<br>

**TOC**

- **[8a.0 What we will build (ADD WHAT WOULD DO IF HAD ACCESS)](#section-8a-0)**
- **[8a.1 Who can read the objects](#section-8a-1)**
  - **[8a.1.1 Create disposable object type with security policy (no source dataset)](#section-8a-1-1)**
  - **[8a.1.4 Test in Insight](#section-8a-1-4)**
  - **[xxx8a.1.5 Open Granular policy (FDE went down a rabbit hole here)](#section-xxx8a-1-5-open-granular-policy-fde-went-down-a-rabbit-hole-here)**
  - **[8a.1.6 Add granular policy ID = GOV-VISIBLE  (FDE's previous instructions were wrong) Start over](#section-8a-1-6)**
  - **[8a.1.8 Restore access](#section-8a-1-8)**
- **[8a.2 Who can run 693_CheckAndSaveRecord (A2 Action)](#section-8a-2)**
  - **[8a.2.1 Ontology Manager /action / security & submission criteria](#section-8a-2-1)**
  - **[8a.2.2 Click Manage groups and show the page that opens.](#section-8a-2-2)**
  - **[8a.2.4 (2) Restrict 693_CheckAndSaveRecord (A2 Action) to that group](#section-8a-2-4)**
  - **[8a.2.6 (4) Add yourself to the group](#section-8a-2-6)**
  - **[8a.2.8 (6) Restore A2’s original organization-based condition](#section-8a-2-8)**
- **[8a.3 Inspect Action configuration history and execution history](#section-8a-3)**
  - **[8a.3.1 Find the manual submission](#section-8a-3-1)**
  - **[8a.3.2 (675) Can this data can be used programmatically (for example, to generate warnings)](#section-8a-3-2)**
  - **[8a.3.3 For custom code](#section-8a-3-3)**
  - **[8a.3.4 Can end here as an execution-history inspection](#section-8a-3-4)**
- **[8a.4a Inspect LLM data-access controls (restriction not tested)](#section-8a-4a)**
  - **[8a.4.1 First, inspect the model controls](#section-8a-4-1)**
  - **[8a.4.2 (693 FDE) This is the relevant governance screen: Control Panel → AIP settings](#section-8a-4-2)**
  - **[8a.4.3 For 8a.4’s data restriction, return to](#section-8a-4-3)**
  - **[8a.4.4 This section demonstrates where the controls are—not a verified allow/block test](#section-8a-4-4)**
- **[8a.4b Hypothetical " Control which data may be sent to LLMs" config/workflow](#section-8a-4b)**



26.1109 This chapter is complete, but it still needs to be modfied more so that it no longer resembles the original GPT chat procedure.


<br>

<a id="section-8a-0"></a>

### **8a.0 What we will build (ADD WHAT WOULD DO IF HAD ACCESS)**


A trial user can not create a **second test user**. So this demo may be limited in some areas.


- **Apply and test reversible changes** where your account retains the ability to undo them.
- **Stop before changes that could remove your ability to restore access.**
- Record the original settings before changing anything.

Having only one user limits **testing another user’s access**, but does not automatically prevent a demo of governance settings.


<br>

<a id="section-8a-1"></a>

### **8a.1 Who can read the objects**


A separate, disposable object type is safer than experimenting on Capstone2Record.


But we should **not deliberately remove your ability to manage or delete it**. Instead, we can test blocking your access to its **objects** while retaining permission to edit the security settings and restore access.


We’ll leave **Capstone2Record (object type)** and its workflows unchanged.


For the test object type, would you prefer to:


- Supply a small dataset, or
- Create it **without a source dataset**, with test objects added through an Action?

This is just a demo.... so do whatever shows governance. the simplest demo.


<br>

<a id="section-8a-1-1"></a>

#### **8a.1.1 Create disposable object type with security policy (no source dataset)**


<img src="/assets/qs/8b_01.png" alt="8b governance illustration 1" width="81%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_02.png" alt="8b governance illustration 2" width="60%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_03.png" alt="8b governance illustration 3" width="59%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_04.png" alt="8b governance illustration 4" width="62%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_05.png" alt="8b governance illustration 5" width="71%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_06.png" alt="8b governance illustration 6" width="48%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_07.png" alt="8b governance illustration 7" width="56%" style="border: 1px solid #999;">


<br>

**Security policy**


<img src="/assets/qs/8b_08.png" alt="8b governance illustration 8" width="62%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_09.png" alt="8b governance illustration 9" width="71%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_10.png" alt="8b governance illustration 10" width="76%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_11.png" alt="8b governance illustration 11" width="10%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_12.png" alt="8b governance illustration 12" width="41%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_13.png" alt="8b governance illustration 13" width="78%" style="border: 1px solid #999;">


Yes—this setup is suitable for the governance demo. No need to start over:


- **GovernanceDemoRecord (object type)** has no source dataset.
- **ID** is its String primary key and title.
- **Create GovernanceDemoRecord (Action)** will create the test object.
- The default object security policy is still unchanged.

<br>

**Save**


The screen shows **12 edits** and **“Set on save.”**


<img src="/assets/qs/8b_14.png" alt="8b governance illustration 14" width="74%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_15.png" alt="8b governance illustration 15" width="85%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_16.png" alt="8b governance illustration 16" width="78%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_17.png" alt="8b governance illustration 17" width="41%" style="border: 1px solid #999;">


<br>

<a id="section-8a-1-4"></a>

#### **8a.1.4 Test in Insight**


<img src="/assets/qs/8b_18.png" alt="8b governance illustration 18" width="26%" style="border: 1px solid #999;">


In **Insight**, open **Actions → Create GovernanceDemoRecord (Action)**. Enter **GOV-TEST-1** for **ID** and submit.


This creates one disposable test object. We’ll verify it is visible before changing its access policy.


<img src="/assets/qs/8b_19.png" alt="8b governance illustration 19" width="34%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_20.png" alt="8b governance illustration 20" width="62%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_21.png" alt="8b governance illustration 21" width="24%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_22.png" alt="8b governance illustration 22" width="90%" style="border: 1px solid #999;">


That is fine—the generated Create Action assigned a UUID automatically. My instruction to enter GOV-TEST-1 was incorrect. **ID is the primary key and cannot be changed after creation.** No change is needed: Insight shows **one visible test object**, which is all we need.


<br>

<a id="section-xxx8a-1-5-open-granular-policy-fde-went-down-a-rabbit-hole-here"></a>

#### **xxx8a.1.5 Open Granular policy (FDE went down a rabbit hole here)**


<img src="/assets/qs/8b_23.png" alt="8b governance illustration 23" width="82%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_24.png" alt="8b governance illustration 24" width="73%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_25.png" alt="8b governance illustration 25" width="65%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_26.png" alt="8b governance illustration 26" width="81%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_27.png" alt="8b governance illustration 27" width="38%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_28.png" alt="8b governance illustration 28" width="77%" style="border: 1px solid #999;">


- Click **Property** in the right-hand **Define condition** panel. We’ll inspect whether we can allow viewing only when **ID** equals a test value that does not match the existing object.

<img src="/assets/qs/8b_29.png" alt="8b governance illustration 29" width="84%" style="border: 1px solid #999;">


- Select **Is equal to**.

<img src="/assets/qs/8b_30.png" alt="8b governance illustration 30" width="84%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_31.png" alt="8b governance illustration 31" width="38%" style="border: 1px solid #999;">


- That opened the **All / Any / Not** dropdown.vClose it, then click the words **“of these rules”** on the lower empty group—not its **All** **▾** button. We need to select the group itself to see whether a delete control appears.

<br>

<a id="section-8a-1-6"></a>

#### **8a.1.6 Add granular policy ID = GOV-VISIBLE  (FDE's previous instructions were wrong) Start over**


The simplest fix is to rebuild this **unsaved granular policy**:


- Click **Clear** at the top of **Define granular policy**.
- Add **one condition**, not a logical operator.
- Set **Property → ID → Is equal to → Constant value → GOV-VISIBLE**.

The result should contain only **ID is equal to GOV-VISIBLE**, with no extra empty group. **Do not apply it yet.**


<img src="/assets/qs/8b_32.png" alt="8b governance illustration 32" width="90%" style="border: 1px solid #999;">


Correct—there is now just one condition, with no warning.


This policy allows viewing only objects whose **ID equals GOV-VISIBLE**. Your test object’s UUID does not match,


The policy is a **condition for permission to see an object**:


Show an object only if its **ID = GOV-VISIBLE**.


Your test object’s ID is something like **2fa46a47-…**, not GOV-VISIBLE. Therefore, **you will not be allowed to see that object after applying the policy**.


The object is **not deleted**. Removing the condition restores visibility.


We chose GOV-VISIBLE simply as a value that does **not** match your test object’s ID.


**Yes—if the review shows only the granular policy change for GovernanceDemoRecord (test object type), click Confirm changes.**


This applies the visibility restriction to the disposable test objects, not **Capstone2Record**.


<img src="/assets/qs/8b_33.png" alt="8b governance illustration 33" width="22%" style="border: 1px solid #999;">


so it should become hidden.


<img src="/assets/qs/8b_34.png" alt="8b governance illustration 34" width="74%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_35.png" alt="8b governance illustration 35" width="84%" style="border: 1px solid #999;">


- Click **Save** in **Ontology Manager**.

<br>

**In insight no visible objects**


- Then refresh **Insight → GovernanceDemoRecord objects**. We expect **zero visible objects**.

<img src="/assets/qs/8b_36.png" alt="8b governance illustration 36" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_37.png" alt="8b governance illustration 37" width="30%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_38.png" alt="8b governance illustration 38" width="59%" style="border: 1px solid #999;">


<br>

**The policy is saved, and Ontology Manager now shows 0 objects visible to you**


You can still access **GovernanceDemoRecord (object type)** and its settings.


<img src="/assets/qs/8b_39.png" alt="8b governance illustration 39" width="90%" style="border: 1px solid #999;">


Next, refresh **Insight → GovernanceDemoRecord objects** to verify that the test object no longer appears there. Then we’ll remove the condition and restore visibility.


<img src="/assets/qs/8b_40.png" alt="8b governance illustration 40" width="47%" style="border: 1px solid #999;">


**The restriction worked:** Insight no longer displays the test object.


<br>

<a id="section-8a-1-8"></a>

#### **8a.1.8 Restore access**


<img src="/assets/qs/8b_41.png" alt="8b governance illustration 41" width="74%" style="border: 1px solid #999;">


- Edit **Object security policy** using its pencil.

<img src="/assets/qs/8b_42.png" alt="8b governance illustration 42" width="78%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_43.png" alt="8b governance illustration 43" width="34%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_44.png" alt="8b governance illustration 44" width="81%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_45.png" alt="8b governance illustration 45" width="65%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_46.png" alt="8b governance illustration 46" width="27%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_47.png" alt="8b governance illustration 47" width="82%" style="border: 1px solid #999;">


We expect the **same test object to reappear**. Do not delete the object security policy itself—remove only its granular condition.


**Access is restored:** the same test object is visible again in **Ontology Manager** and **Insight**.


This demo is complete:


**1 visible object → apply policy → 0 visible objects → remove condition → 1 visible object**


The object was never deleted. Its **visibility changed**, while your ability to manage **GovernanceDemoRecord (object type)** remained intact.


<br>

<a id="section-8a-2"></a>

### **8a.2 Who can run 693_CheckAndSaveRecord (A2 Action)**


<br>

<a id="section-8a-2-1"></a>

#### **8a.2.1 Ontology Manager /action / security & submission criteria**


- Open **Ontology Manager**.
- Open **693_CheckAndSaveRecord (A2 Action)**.

<img src="/assets/qs/8b_48.png" alt="8b governance illustration 48" width="74%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_49.png" alt="8b governance illustration 49" width="72%" style="border: 1px solid #999;">


- The current submission condition allows members of **ziptieai (organization)** to run **693_CheckAndSaveRecord (A2 Action)**.
- Under **Submission criteria**, click **Current User Organizations Includes any of ziptieai**.

<img src="/assets/qs/8b_50.png" alt="8b governance illustration 50" width="81%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_51.png" alt="8b governance illustration 51" width="36%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_52.png" alt="8b governance illustration 52" width="37%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_53.png" alt="8b governance illustration 53" width="38%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_54.png" alt="8b governance illustration 54" width="39%" style="border: 1px solid #999;">


<br>

<a id="section-8a-2-2"></a>

#### **8a.2.2 Click Manage groups and show the page that opens.**


**Do not save the Action changes** while the group selection is empty.


<img src="/assets/qs/8b_55.png" alt="8b governance illustration 55" width="55%" style="border: 1px solid #999;">


You’re in **Settings → Groups → Manage groups**. No groups are listed, and **Create group** is available.


Click **Create group**. We’ll create **GovernanceDemoSubmitters (group)** for this demo, then add your account as a member.


Show the creation dialog before confirming. Leave the unsaved **A2 Action** settings open in the other tab.


**(****650****)** **FDE** **Yes—you’re right.** To demonstrate blocking (the rest of 8a.2):


<br>

**(1) Create GovernanceDemoSubmitters (group) with no members**


<img src="/assets/qs/8b_56.png" alt="8b governance illustration 56" width="42%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_57.png" alt="8b governance illustration 57" width="73%" style="border: 1px solid #999;">


<br>

<a id="section-8a-2-4"></a>

#### **8a.2.4 (2) Restrict 693_CheckAndSaveRecord (A2 Action) to that group**


<img src="/assets/qs/8b_58.png" alt="8b governance illustration 58" width="31%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_59.png" alt="8b governance illustration 59" width="10%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_60.png" alt="8b governance illustration 60" width="79%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_61.png" alt="8b governance illustration 61" width="82%" style="border: 1px solid #999;">


<br>

**(3) Verify that your submission is blocked**


- In **Ontology Manager**, **Save** the group restriction on **693_CheckAndSaveRecord (A2 Action)** if you haven’t already.

<img src="/assets/qs/8b_62.png" alt="8b governance illustration 62" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_63.png" alt="8b governance illustration 63" width="83%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_64.png" alt="8b governance illustration 64" width="46%" style="border: 1px solid #999;">


- Enter **Criteria**:  
Match if the integer is greater than 100.
- Attempt to **Submit**. Expected: submission is disabled or rejected because you are not a member of **GovernanceDemoSubmitters (group)**. **CheckResult should remain unchanged.**
- Show the restriction message. If the Action is absent from the menu, show that instead.
- A2 is absent from the menu.  Only **693_SaveCheckResult (A1 Action)** is shown. That is the observed blocked-access result—there is no A2 form to submit. Replace steps 5–6 for this test with: **Verify that 693_CheckAndSaveRecord (A2 Action) is absent from the Actions menu. Do not run 693_SaveCheckResult (A1 Action).**

<br>

<a id="section-8a-2-6"></a>

#### **8a.2.6 (4) Add yourself to the group**


- Return to **Settings → Groups → GovernanceDemoSubmitters (group)**.

<img src="/assets/qs/8b_65.png" alt="8b governance illustration 65" width="83%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_66.png" alt="8b governance illustration 66" width="75%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_67.png" alt="8b governance illustration 67" width="80%" style="border: 1px solid #999;">


<br>

**2.7 (5) Verify that submission succeeds**


**A2 has reappeared. Now test that it runs:**


- Click **693_CheckAndSaveRecord (A2 Action)**.
- Confirm **Record** is **Id 7**.

<img src="/assets/qs/8b_68.png" alt="8b governance illustration 68" width="54%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_69.png" alt="8b governance illustration 69" width="31%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_70.png" alt="8b governance illustration 70" width="85%" style="border: 1px solid #999;">


Since Id 7’s Integer is **777**, **CheckResult should change from FOUND to NOT FOUND**. This visible change verifies that submission succeeded.


<br>

<a id="section-8a-2-8"></a>

#### **8a.2.8 (6) Restore A2’s original organization-based condition**


**While the restriction is applied, the automations may also be blocked.** Keep the dataset build schedule paused during this test. Your permission to edit A2’s configuration is separate from permission to submit it.


<img src="/assets/qs/8b_71.png" alt="8b governance illustration 71" width="90%" style="border: 1px solid #999;">


In the screen shown:


- Click **Current User groups Includes any of GovernanceDemoSubmitters**.
- In the right-hand editor, change **Group IDs** to **Organization Marking IDs**.
- Keep **Includes any of**.

<img src="/assets/qs/8b_72.png" alt="8b governance illustration 72" width="82%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_73.png" alt="8b governance illustration 73" width="83%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_74.png" alt="8b governance illustration 74" width="79%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_75.png" alt="8b governance illustration 75" width="80%" style="border: 1px solid #999;">


**Both settings match the original configuration:**


- Submission requires membership in **ziptieai (organization)**.
- **Allow Foundry Automate to submit this action** is **ON**.

If changes are still pending, click **Save** and confirm. **8a.2 is then complete:** group restriction → blocked access → add membership → successful submission → restore original restriction.


<br>

<a id="section-8a-3"></a>

### **8a.3 Inspect Action configuration history and execution history**


**This** **is inspection, not an allow/block test.** Its demonstration is simply to trace a saved response back to the Action or automation execution.


We’ll inspect the **manual A2 submission** first, then an **automatic A2 execution**.


<br>

<a id="section-8a-3-1"></a>

#### **8a.3.1 Find the manual submission**


- Open **Ontology Manager → 693_CheckAndSaveRecord (A2 Action)**.
- Click **History** in the left sidebar.

<img src="/assets/qs/8b_76.png" alt="8b governance illustration 76" width="71%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_77.png" alt="8b governance illustration 77" width="71%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_78.png" alt="8b governance illustration 78" width="63%" style="border: 1px solid #999;">


This is the execution **Trace**. It shows the sequence **Action → Logic function → LLM call**, with timings.


Click **Details** beside **Trace** at the top. Show that panel so we can look for the submitting user and execution information.


Leave **Edit permissions** unchanged.


<br>

<a id="section-8a-3-2"></a>

#### **8a.3.2 (675) Can this data can be used programmatically (for example, to generate warnings)**


Yes—execution information can support automated warnings, such as:


- An Action fails.
- Execution takes too long.
- An automation repeatedly fails.

The visible **“Monitor this action”** button is the built-in starting point for configuring alerts.


<br>

<a id="section-8a-3-3"></a>

#### **8a.3.3 For custom code**


Foundry provides observability and monitoring APIs, but we would need to verify which execution fields and APIs are available in your environment. We should not assume that every detail visible in this trace is programmatically accessible.


Also, **execution monitoring is not necessarily a property-change audit**: detecting “A2 failed” is different from identifying “who changed CheckResult from FOUND to NOT FOUND.”


<br>

<a id="section-8a-3-4"></a>

#### **8a.3.4 Can end here as an execution-history inspection**


We verified:


- **History:** who changed A2’s configuration.
- **Observability → Run history:** successful executions and their callers.
- **Trace:** Action → Logic function → LLM call, with timings.
- **Chapter 7b automation history:** which object triggered an automatic execution.

**Limitation:** we did not verify a property-level audit showing who changed **CheckResult**, with its old and new values.


So a more accurate section title is:


**8a.3 Inspect Action configuration history and execution history**


<br>

<a id="section-8a-4a"></a>

### **8a.4a Inspect LLM data-access controls (restriction not tested)**


For the LLM example, distinguish who can call the function from whether particular data may be processed by a model. They are different controls. We should verify which mechanisms your enrollment supports before writing those instructions.


A useful chapter pattern:


Run successfully → apply restriction → repeat and observe the block → restore access


Two or three examples are enough. A second test user is important for access demonstrations; testing only as the owner can hide the effect.


<br>

<a id="section-8a-4-1"></a>

#### **8a.4.1 First, inspect the model controls**


<br>

**AIP logic**


- Open **693_AIPL_CheckRecord (AIPL)** in **AIP Logic**.
- Open **Config**.
- In **Use LLM → Model**, open the dropdown currently showing **GPT-5.6 Sol**.
- Show that menu, including any policy or model-information controls.

**Do not change the model or publish anything.** We need to identify the available governance controls—choosing a model alone is not a data-use restriction.


<img src="/assets/qs/8b_79.png" alt="8b governance illustration 79" width="90%" style="border: 1px solid #999;">


This menu shows **model selection and technical details**, not data-use restrictions.


Click the **↗ arrow beside GPT-5.6 Sol** at the top-right of its information card, and show the page it opens.


Leave the model selection and **User-scoped execution** unchanged—the latter controls execution-log visibility, not whether data may be sent to the LLM.


<img src="/assets/qs/8b_80.png" alt="8b governance illustration 80" width="86%" style="border: 1px solid #999;">


<br>

**You’re now in Model Catalog → GPT-5.6 Sol (model).**


This page shows the provider, terms, and a playground—not data-access restrictions.


The documented controls are in **Control Panel → AIP settings**. Administrators can manage model availability there and configure which marked data LLMs may process.


Enable AIP features / Enable LLMs


<br>

**Next: open Control Panel → AIP settings**


and show that screen. **Do not disable any models or change policies yet.** If that section is unavailable to your account, we’ll mark this part as inspection-only.


<img src="/assets/qs/8b_81.png" alt="8b governance illustration 81" width="78%" style="border: 1px solid #999;">


<br>

**AIP settings**


In **Control Panel**:


- Click **What setting are you looking for?**
- Search for **AIP**.
- Open **AIP settings** if listed.

Show that screen. **Do not change any settings yet.**


<img src="/assets/qs/8b_82.png" alt="8b governance illustration 82" width="49%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_83.png" alt="8b governance illustration 83" width="65%" style="border: 1px solid #999;">


<br>

<a id="section-8a-4-2"></a>

#### **8a.4.2 (693 FDE) This is the relevant governance screen: Control Panel → AIP settings**


Three different controls are visible:


- **Palantir model access for custom workflows:** who may use the models.
- **Data access:** which **marked data** may be passed to LLMs. Currently **Allow any data** is selected.
- **Palantir models** tab: controls for individual model families.

**Important:** the Data access description says **unmarked data is always allowed when AIP is enabled**. Simply enabling a marking restriction would therefore not block our unmarked demo data.


Leave this page unchanged.


<br>

**Click Palantir models (tab) at the top**


and show that tab so we can inspect whether a model-specific, reversible test is available.


<img src="/assets/qs/8b_84.png" alt="8b governance illustration 84" width="81%" style="border: 1px solid #999;">


This tab controls **model-family availability**.


- In **Search models or model families…**, enter **GPT-5.6**.
- Show the matching entries. If there are no results, search **OpenAI** instead.

**Do not disable anything yet.** Disabling the family used by **693_AIPL_CheckRecord (AIPLF)** could also affect other workflows using that family.


<img src="/assets/qs/8b_85.png" alt="8b governance illustration 85" width="37%" style="border: 1px solid #999;">


**GPT-5.6 Sol appears under two providers:** **Direct OpenAI** and **Microsoft Azure**.


Click **Manage** beside **OpenAI → Direct OpenAI**, then show the dialog. **Do not change or save anything yet.** We’ll inspect the scope of the controls before choosing a test.


<img src="/assets/qs/8b_86.png" alt="8b governance illustration 86" width="61%" style="border: 1px solid #999;">


<img src="/assets/qs/8b_87.png" alt="8b governance illustration 87" width="57%" style="border: 1px solid #999;">


This page controls **the whole Direct OpenAI model family**, not access to particular data.


- **Enable this model family:** allows or blocks that family.
- **Restrict access to select organizations:** limits which organizations can use it.

Leave both unchanged.


<br>

<a id="section-8a-4-3"></a>

#### **8a.4.3 For 8a.4’s data restriction, return to**


<br>

**Control Panel → AIP settings → AIP settings tab → Data access**


Select **Allow only the following markings** to reveal its controls, then show that area. **Do not click Save**—this is an enrollment-wide setting, and we’re inspecting it first.


<img src="/assets/qs/8b_88.png" alt="8b governance illustration 88" width="60%" style="border: 1px solid #999;">


The warning means **the marking allowlist is empty**.


Click **Edit** beside **Markings** and show the picker. **Do not save the enrollment settings yet.**


This control restricts **marked data** sent to LLMs; the text above explicitly says **unmarked data remains allowed**.


<img src="/assets/qs/8b_89.png" alt="8b governance illustration 89" width="49%" style="border: 1px solid #999;">


<br>

**No selectable markings are visible to your account**


even with the filter off. We cannot complete a marking-based test with this picker as it stands.


Restore the unchanged configuration:


- Click **Cancel** in **Manage markings**.
- Select **Allow any data**, the original setting.
- **Do not save any other changes.**

<br>

<a id="section-8a-4-4"></a>

#### **8a.4.4 This section demonstrates where the controls are—not a verified allow/block test**


We inspected model-family enablement and the marking-based LLM data-access control. No selectable markings were available, so we did not apply or test a data restriction. Unmarked data remains allowed when AIP is enabled.


Yes—we’re finished with 8a.4 as an inspection-only section.


But we **cannot conclude that your account doesn’t support the functionality**. The controls are present; the marking picker simply showed no choices. We haven’t established why—there may be no applicable markings configured, or your account may lack visibility to them.


The accurate conclusion is:


**The LLM data-access controls are available, but we could not test a marking-based restriction because no selectable markings appeared. No restrictions were applied.**


<br>

<a id="section-8a-4b"></a>

### **8a.4b Hypothetical " Control which data may be sent to LLMs" config/workflow**


<img src="/assets/qs/8b_90.png" alt="8b governance illustration 90" width="78%" style="border: 1px solid #999;">


**Better title**


**8a.4 Control which data may be sent to LLMs**


**The demo we would perform**


Use **disposable test data**, not the existing Capstone2Record workflow.


- **Prepare two mandatory markings:** DemoAllowed and DemoRestricted.
- Protect the disposable test data with **DemoRestricted**, and give the test user access to that marking.
- **Baseline test:** run a small AIPL that sends the test text to an LLM. Verify it succeeds.
- In **Control Panel → AIP settings → Data access**, select **Allow only the following markings**.
- Include **DemoAllowed**, but exclude **DemoRestricted**, then save.
- Repeat the LLM call from a session with access to **DemoRestricted**. Verify the request is **blocked**.
- Add **DemoRestricted** to the allowlist and repeat. Verify the request **succeeds**.
- Restore the original **Allow any data** setting and remove the disposable test setup.

**Important mechanism:** this control checks the mandatory markings available to the **request’s session/token**, not merely the markings on the text actually sent. An excluded marking on the token can block the request even if that particular prompt contains unmarked text.


Control LLM data access with Markings


Because this setting affects the enrollment, we would record its original state and coordinate the test before applying it.


**About your second account**


That is useful. Once the invitation is accepted, a **second user in a separate browser profile** lets us test restrictions while your original account retains administrative access.


However, **a second user does not by itself solve the empty marking picker**. We still need to establish whether you can create and manage mandatory markings. Our earlier conclusion was only that **no selectable markings appeared**, not that your account lacks the functionality.


can you give me that list again, but this time with clearly stated what apps / tools are used?  
i want to make a diagram like my typical workflow diagrams (see attached)


762 For **8a.4**, these are the apps/tools for each step. **This is a planned demo—not yet verified in your environment.**


**Suggested diagram boxes**


**Markings management**  
Create test markings  
↓  
**Projects & files**  
Create marked test project  
↓  
**AIP Logic**  
Baseline: allowed  
↓  
**Control Panel**  
Exclude test marking  
↓  
**AIP Logic**  
Verify blocked  
↓  
**Control Panel**  
Allow test marking  
↓  
**AIP Logic**  
Verify allowed  
↓  
**Control Panel**  
Restore original setting


**Important diagram note:** the restriction checks the markings available to the **request’s session/token**, not just the prompt’s contents. We must verify the test session has **DemoRestricted** available.


Control LLM data access with Markings


763 so the only workflow testing (the diagram i attached) is in AIPL do a preview? (if so thats fine.... just want to verify)


764 **Yes—the only execution test is AIPL Preview in AIP Logic:** verify the LLM call succeeds, is blocked, then succeeds again.


**No MockAPI import, dataset build, AIPLF, Action, automation, or Workshop UI is needed for this test.**


Summarize aboveRemove belowFork session


765 everything else is configuration


Summarize aboveRemove belowFork session


766 **Yes. Everything else is configuration; AIPL Preview is where we test the result.**

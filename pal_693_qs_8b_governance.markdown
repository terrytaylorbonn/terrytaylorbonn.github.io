---
layout: page
title: 8b (8a) Governance (allow, block, verify)
permalink: /pal_693_qs_8b_governance/
---

<br>



[← 8a Add processing of updated objects](/pal_693_qs_8a_automate_updated/) / [↑ 3c Foundry QS](/pal_693_qs/) / [→ 9 Continuing your Foundry education](/pal_693_qs_9_where_next/)

_26.1113 12:52 (converted from docx source file to markdown+PNGs by ChatGPT)_

<br>

**TOC**

- **[8b.0 What we will build](#section-8b-0-what-we-will-build)**
- **[8b.1 Security policy (Who can read the objects)](#section-8b-1-security-policy-who-can-read-the-objects)**
  - [8b.1.1 Create disposable object type with security policy (no source dataset)](#section-8b-1-1-create-disposable-object-type-with-security-policy-no-source-dataset)
  - [8b.1.2 Test in Insight](#section-8b-1-2-test-in-insight)
  - [8b.1.3 Add granular policy ID = GOV-VISIBLE (FDE's previous instructions were wrong) Start over](#section-8b-1-3-add-granular-policy-id-gov-visible-fde-s-previous-instructions-were-wrong-start-over)
  - [8b.1.4 Restore access](#section-8b-1-4-restore-access)
- **[8b.2 Action access (Who can run 693_CheckAndSaveRecord (A2 Action))](#section-8b-2-action-access-who-can-run-693-checkandsaverecord-a2-action)**
  - [8b.2.1 Ontology Manager /action / security & submission criteria](#section-8b-2-1-ontology-manager-action-security-submission-criteria)
  - [8b.2.2 Click Manage groups and show the page that opens.](#section-8b-2-2-click-manage-groups-and-show-the-page-that-opens)
  - [8b.2.3 (2) Restrict 693_CheckAndSaveRecord (A2 Action) to that group](#section-8b-2-3-2-restrict-693-checkandsaverecord-a2-action-to-that-group)
  - [8b.2.4 (4) Add yourself to the group](#section-8b-2-4-4-add-yourself-to-the-group)
  - [8b.2.5 (6) Restore A2’s original organization-based condition](#section-8b-2-5-6-restore-a2-s-original-organization-based-condition)
- **[8b.3 Inspect Action configuration history and execution history](#section-8b-3-inspect-action-configuration-history-and-execution-history)**
  - [8b.3.1 Find the manual submission](#section-8b-3-1-find-the-manual-submission)
  - [8b.3.2 (675) Can this data can be used programmatically (for example, to generate warnings)](#section-8b-3-2-675-can-this-data-can-be-used-programmatically-for-example-to-generate-warnings)
  - [8b.3.3 For custom code](#section-8b-3-3-for-custom-code)
  - [8b.3.4 Summary](#section-8b-3-4-summary)
- **[8b.4a Inspect LLM data-access controls (restriction not tested)](#section-8b-4a-inspect-llm-data-access-controls-restriction-not-tested)**
  - [8b.4a.1 Inspect the model controls](#section-8b-4a-1-inspect-the-model-controls)
  - [8b.4a.2 (693) This is the relevant governance screen: Control Panel → AIP settings](#section-8b-4a-2-693-this-is-the-relevant-governance-screen-control-panel-aip-settings)
  - [8b.4a.3 Data restrictions](#section-8b-4a-3-data-restrictions)
  - [8b.4a.4 This section demonstrates where the controls are—not a verified allow/block test](#section-8b-4a-4-this-section-demonstrates-where-the-controls-are-not-a-verified-allow-block-test)
- **[8b.4b Hypothetical " Control which data may be sent to LLMs" config/workflow](#section-8b-4b-hypothetical-control-which-data-may-be-sent-to-llms-config-workflow)**


<br>

<a id="section-8b-8a-governance-allow-block-verify"></a>



<a id="section-8b-0-what-we-will-build"></a>

### **8b.0 What we will build**

This demo may be limited in some areas.

- **Apply and test reversible changes** where your account retains the ability to undo them.
- **Stop before changes that could remove your ability to restore access.**
- Record the original settings before changing anything.

<br>


<a id="section-8b-1-security-policy-who-can-read-the-objects"></a>

### **8b.1 Security policy (Who can read the objects)**

<img src="/assets/qs/8b_01.png" alt="Chapter 8b screenshot 1" width="77%" style="border: 1px solid #999;">

A separate, disposable object type is safer than experimenting on Capstone2Record. But we should **not deliberately remove your ability to manage or delete it**. Instead, we can test blocking your access to its **objects** while retaining permission to edit the security settings and restore access. We’ll leave **Capstone2Record (object type)** and its workflows unchanged.


<br>

<a id="section-8b-1-1-create-disposable-object-type-with-security-policy-no-source-dataset"></a>



#### **8b.1.1 Create disposable object type with security policy (no source dataset)**

1\. Create **GovernanceDemoRecord (object type)** with one test object.

<img src="/assets/qs/8b_02.png" alt="Chapter 8b screenshot 2" width="81%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_03.png" alt="Chapter 8b screenshot 3" width="60%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_04.png" alt="Chapter 8b screenshot 4" width="59%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_05.png" alt="Chapter 8b screenshot 5" width="62%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_06.png" alt="Chapter 8b screenshot 6" width="61%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_07.png" alt="Chapter 8b screenshot 7" width="55%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_08.png" alt="Chapter 8b screenshot 8" width="58%" style="border: 1px solid #999;">

**Security policy**

<img src="/assets/qs/8b_09.png" alt="Chapter 8b screenshot 9" width="62%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_10.png" alt="Chapter 8b screenshot 10" width="91%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_11.png" alt="Chapter 8b screenshot 11" width="96%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_12.png" alt="Chapter 8b screenshot 12" width="6%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_13.png" alt="Chapter 8b screenshot 13" width="27%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_14.png" alt="Chapter 8b screenshot 14" width="78%" style="border: 1px solid #999;">

Yes—this setup is suitable for the governance demo. No need to start over:

- **GovernanceDemoRecord (object type)** has no source dataset.
- **ID** is its String primary key and title.
- **Create GovernanceDemoRecord (Action)** will create the test object.
- The default object security policy is still unchanged.

**Save**

The screen shows **12 edits** and **“Set on save.”**

<img src="/assets/qs/8b_15.png" alt="Chapter 8b screenshot 15" width="64%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_16.png" alt="Chapter 8b screenshot 16" width="85%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_17.png" alt="Chapter 8b screenshot 17" width="78%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_18.png" alt="Chapter 8b screenshot 18" width="35%" style="border: 1px solid #999;">

<br>

<a id="section-8b-1-2-test-in-insight"></a>



#### **8b.1.2 Test in Insight**

<img src="/assets/qs/8b_19.png" alt="Chapter 8b screenshot 19" width="26%" style="border: 1px solid #999;">

In **Insight**, open **Actions → Create GovernanceDemoRecord (Action)**. Enter **GOV-TEST-1** for **ID** and submit.  This creates one disposable test object. We’ll verify it is visible before changing its access policy.

<img src="/assets/qs/8b_20.png" alt="Chapter 8b screenshot 20" width="24%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_21.png" alt="Chapter 8b screenshot 21" width="44%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_22.png" alt="Chapter 8b screenshot 22" width="20%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_23.png" alt="Chapter 8b screenshot 23" width="99%" style="border: 1px solid #999;">

That is fine—the generated Create Action assigned a UUID automatically. My instruction to enter GOV-TEST-1 was incorrect. **ID is the primary key and cannot be changed after creation.** No change is needed: Insight shows **one visible test object**, which is all we need.

<br>

<a id="section-8b-1-3-add-granular-policy-id-gov-visible-fde-s-previous-instructions-were-wrong-start-over"></a>



#### **8b.1.3 Add granular policy ID = GOV-VISIBLE  (FDE's previous instructions were wrong) Start over**

The simplest fix is to rebuild this **unsaved granular policy**:

1\. Click **Clear** at the top of **Define granular policy**.

2\. Add **one condition**, not a logical operator.

3\. Set **Property → ID → Is equal to → Constant value → GOV-VISIBLE**.

The result should contain only **ID is equal to GOV-VISIBLE**, with no extra empty group. **Do not apply it yet.**

<img src="/assets/qs/8b_24.png" alt="Chapter 8b screenshot 24" width="90%" style="border: 1px solid #999;">

There is now just one condition, with no warning. This policy allows viewing only objects whose **ID equals GOV-VISIBLE**. Your test object’s UUID does not match,

```
The policy is a **condition for permission to see an object**:
Show an object only if its **ID = GOV-VISIBLE**.
Your test object’s ID is something like **2fa46a47-…**, not GOV-VISIBLE. Therefore, **you will not be allowed to see that object after applying the policy**.
The object is **not deleted**. Removing the condition restores visibility.
We chose GOV-VISIBLE simply as a value that does **not** match your test object’s ID.
---
**Yes—if the review shows only the granular policy change for GovernanceDemoRecord (test object type), click Confirm changes.**
This applies the visibility restriction to the disposable test objects, not **Capstone2Record**
So it should become hidden.
```

4\. Return to **Overview** in the policy dialog.

<img src="/assets/qs/8b_25.png" alt="Chapter 8b screenshot 25" width="92%" style="border: 1px solid #999;">

5\. Click **Update object security policy**.

<img src="/assets/qs/8b_26.png" alt="Chapter 8b screenshot 26" width="94%" style="border: 1px solid #999;">

6\. Click **Save** in **Ontology Manager**.

7\. Then refresh **Insight → GovernanceDemoRecord objects**. We expect **zero visible objects**.

8\. To reverse the test:** return to this granular policy, click **Clear**, update the policy, and save. Do not change project permissions.

<img src="/assets/qs/8b_27.png" alt="Chapter 8b screenshot 27" width="95%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_28.png" alt="Chapter 8b screenshot 28" width="24%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_29.png" alt="Chapter 8b screenshot 29" width="59%" style="border: 1px solid #999;">

The policy is saved, and Ontology Manager now shows 0 objects visible to you. You can still access **GovernanceDemoRecord (object type)** and its settings.

<img src="/assets/qs/8b_30.png" alt="Chapter 8b screenshot 30" width="90%" style="border: 1px solid #999;">

Next, refresh **Insight → GovernanceDemoRecord objects** to verify that the test object no longer appears there. Then we’ll remove the condition and restore visibility.

<img src="/assets/qs/8b_31.png" alt="Chapter 8b screenshot 31" width="47%" style="border: 1px solid #999;">

**The restriction worked:** Insight no longer displays the test object.

<br>

<a id="section-8b-1-4-restore-access"></a>



#### **8b.1.4 Restore access**

1\. Open **Ontology Manager → GovernanceDemoRecord (object type) → Security**.

<img src="/assets/qs/8b_32.png" alt="Chapter 8b screenshot 32" width="74%" style="border: 1px solid #999;">

2\. Edit **Object security policy** using its pencil.

3\. Open **Granular policy → Manage**.

<img src="/assets/qs/8b_33.png" alt="Chapter 8b screenshot 33" width="94%" style="border: 1px solid #999;">

4\. Click **Clear** to remove **ID is equal to GOV-VISIBLE**.

<img src="/assets/qs/8b_34.png" alt="Chapter 8b screenshot 34" width="27%" style="border: 1px solid #999;">

5\. Confirm/update the policy.

<img src="/assets/qs/8b_35.png" alt="Chapter 8b screenshot 35" width="74%" style="border: 1px solid #999;">

6\. Then **Save** and confirm the Ontology changes.

<img src="/assets/qs/8b_36.png" alt="Chapter 8b screenshot 36" width="60%" style="border: 1px solid #999;">

7\. Refresh browser

<img src="/assets/qs/8b_37.png" alt="Chapter 8b screenshot 37" width="24%" style="border: 1px solid #999;">

8\. Refresh **Insight**.

<img src="/assets/qs/8b_38.png" alt="Chapter 8b screenshot 38" width="92%" style="border: 1px solid #999;">

We expect the **same test object to reappear**. Do not delete the object security policy itself—remove only its granular condition. **Access is restored:** the same test object is visible again in **Ontology Manager** and **Insight**. This demo is complete: **1 visible object → apply policy → 0 visible objects → remove condition → 1 visible object.** The object was never deleted. Its **visibility changed**, while your ability to manage **GovernanceDemoRecord (object type)** remained intact.

<br>

<a id="section-8b-2-action-access-who-can-run-693-checkandsaverecord-a2-action"></a>



### **8b.2 Action access (Who can run 693_CheckAndSaveRecord (A2 Action))**

<img src="/assets/qs/8b_39.png" alt="Chapter 8b screenshot 39" width="77%" style="border: 1px solid #999;">

<a id="section-8b-2-1-ontology-manager-action-security-submission-criteria"></a>

<br>

#### **8b.2.1 Ontology Manager /action / security & submission criteria**

1\. Open **Ontology Manager**.

2\. Open **693_CheckAndSaveRecord (A2 Action)**.

3\. Click **Security & Submission Criteria** in the left sidebar. We’ll inspect the existing restriction and choose a reversible test without blocking the automations.

<img src="/assets/qs/8b_40.png" alt="Chapter 8b screenshot 40" width="94%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_41.png" alt="Chapter 8b screenshot 41" width="82%" style="border: 1px solid #999;">

4\. The current submission condition allows members of **ziptieai (organization)** to run **693_CheckAndSaveRecord (A2 Action)**.

5\. Under **Submission criteria**, click **Current User Organizations Includes any of ziptieai**.

6\. Show the condition editor that opens. **Do not save changes yet.** Leave **Allow Foundry Automate to submit this action** ON. We’ll inspect how to select a group before changing the existing restriction.

<img src="/assets/qs/8b_42.png" alt="Chapter 8b screenshot 42" width="85%" style="border: 1px solid #999;">

7\. In the right-hand **User based condition** panel, open the dropdown currently showing **Organization Marking IDs**. Show its options. **Do not change the selected value yet.**

<img src="/assets/qs/8b_43.png" alt="Chapter 8b screenshot 43" width="33%" style="border: 1px solid #999;">

**8. Group IDs** is the option for restricting submission by group membership. Select **Group IDs**, then show the **Compare against → Static value** field. We’ll inspect the group choices before saving anything.

<img src="/assets/qs/8b_44.png" alt="Chapter 8b screenshot 44" width="34%" style="border: 1px solid #999;">

9\. Select **String list**. This will hold the IDs of groups allowed to submit **693_CheckAndSaveRecord (A2 Action)**.  Show the field that appears. **Do not save yet**—we need a real group ID, not its display name.

<img src="/assets/qs/8b_45.png" alt="Chapter 8b screenshot 45" width="34%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_46.png" alt="Chapter 8b screenshot 46" width="39%" style="border: 1px solid #999;">

The picker shows **No results**, so we cannot select a group yet.

<br>

<a id="section-8b-2-2-click-manage-groups-and-show-the-page-that-opens"></a>



#### **8b.2.2 Click Manage groups and show the page that opens.**

**Do not save the Action changes** while the group selection is empty.

<img src="/assets/qs/8b_47.png" alt="Chapter 8b screenshot 47" width="75%" style="border: 1px solid #999;">

1\. You’re in **Settings → Groups → Manage groups**. No groups are listed, and **Create group** is available.

2\. Click **Create group**. We’ll create **GovernanceDemoSubmitters (group)** for this demo, then add your account as a member.

3\. Show the creation dialog before confirming. Leave the unsaved **A2 Action** settings open in the other tab.

**(650) FDE Yes—you’re right.** To demonstrate blocking (the rest of 8a.2):

**(1) Create GovernanceDemoSubmitters (group) with no members**

<img src="/assets/qs/8b_48.png" alt="Chapter 8b screenshot 48" width="42%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_49.png" alt="Chapter 8b screenshot 49" width="73%" style="border: 1px solid #999;">

<a id="section-8b-2-3-2-restrict-693-checkandsaverecord-a2-action-to-that-group"></a>

#### **8b.2.3 (2) Restrict 693_CheckAndSaveRecord (A2 Action) to that group**

<img src="/assets/qs/8b_50.png" alt="Chapter 8b screenshot 50" width="31%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_51.png" alt="Chapter 8b screenshot 51" width="6%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_52.png" alt="Chapter 8b screenshot 52" width="92%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_53.png" alt="Chapter 8b screenshot 53" width="92%" style="border: 1px solid #999;">

**(3) Verify that your submission is blocked**

1\. In **Ontology Manager**, **Save** the group restriction on **693_CheckAndSaveRecord (A2 Action)** if you haven’t already.

2\. Open **Insight → Capstone2Record objects**.

<img src="/assets/qs/8b_54.png" alt="Chapter 8b screenshot 54" width="96%" style="border: 1px solid #999;">

3\. Select **Id 7**.

<img src="/assets/qs/8b_55.png" alt="Chapter 8b screenshot 55" width="98%" style="border: 1px solid #999;">

4\. Choose **Actions → 693_CheckAndSaveRecord**.

<img src="/assets/qs/8b_56.png" alt="Chapter 8b screenshot 56" width="46%" style="border: 1px solid #999;">

5\. Enter **Criteria**: Match if the integer is greater than 100.

6\. Attempt to **Submit**. Expected: submission is disabled or rejected because you are not a member of **GovernanceDemoSubmitters (group)**. **CheckResult should remain unchanged.**

7\. Show the restriction message. If the Action is absent from the menu, show that instead.

8\. A2 is absent from the menu.  Only **693_SaveCheckResult (A1 Action)** is shown. That is the observed blocked-access result—there is no A2 form to submit.

9\. Replace steps 5–6 for this test with: **Verify that 693_CheckAndSaveRecord (A2 Action) is absent from the Actions menu. Do not run 693_SaveCheckResult (A1 Action).**

<br>

<a id="section-8b-2-4-4-add-yourself-to-the-group"></a>


#### **8b.2.4 (4) Add yourself to the group**

1\. Return to **Settings → Groups → GovernanceDemoSubmitters (group)**.

2\. Beside **Members**, click **Manage**.

<img src="/assets/qs/8b_57.png" alt="Chapter 8b screenshot 57" width="83%" style="border: 1px solid #999;">

3\. Add your account and save the membership change.

<img src="/assets/qs/8b_58.png" alt="Chapter 8b screenshot 58" width="66%" style="border: 1px solid #999;">

4\. Then refresh **Insight**, select **Id 7** again, and reopen **Actions**. Check whether **693_CheckAndSaveRecord (A2 Action)** reappears.

<img src="/assets/qs/8b_59.png" alt="Chapter 8b screenshot 59" width="97%" style="border: 1px solid #999;">


**(5) Verify that submission succeeds**

**A2 has reappeared. Now test that it runs:**

1\. Click **693_CheckAndSaveRecord (A2 Action)**.

2\. Confirm **Record** is **Id 7**.

3\. Enter **Criteria**: Match if the integer is greater than 1000.

<img src="/assets/qs/8b_60.png" alt="Chapter 8b screenshot 60" width="42%" style="border: 1px solid #999;">

4\. Click **Submit**.

<img src="/assets/qs/8b_61.png" alt="Chapter 8b screenshot 61" width="31%" style="border: 1px solid #999;">

5\. Refresh **Insight**.

<img src="/assets/qs/8b_62.png" alt="Chapter 8b screenshot 62" width="94%" style="border: 1px solid #999;">

Since Id 7’s Integer is **777**, **CheckResult should change from FOUND to NOT FOUND**. This visible change verifies that submission succeeded.

<br>

<a id="section-8b-2-5-6-restore-a2-s-original-organization-based-condition"></a>



#### **8b.2.5 (6) Restore A2’s original organization-based condition**

**While the restriction is applied, the automations may also be blocked.** Keep the dataset build schedule paused during this test. Your permission to edit A2’s configuration is separate from permission to submit it.

<img src="/assets/qs/8b_63.png" alt="Chapter 8b screenshot 63" width="97%" style="border: 1px solid #999;">

In the screen shown:

1\. Click **Current User groups Includes any of GovernanceDemoSubmitters**.

2\. In the right-hand editor, change **Group IDs** to **Organization Marking IDs**.

3\. Keep **Includes any of**.

4\. Under **Compare against → Static value**, replace **GovernanceDemoSubmitters** with **ziptieai (organization)**.

<img src="/assets/qs/8b_64.png" alt="Chapter 8b screenshot 64" width="96%" style="border: 1px solid #999;">

5\. **Save** and confirm the changes.

<img src="/assets/qs/8b_65.png" alt="Chapter 8b screenshot 65" width="97%" style="border: 1px solid #999;">

6\. The restored condition should read:

- **Current User Organizations Includes any of ziptieai**
- Keep **Allow Foundry Automate to submit this action** ON.

<img src="/assets/qs/8b_66.png" alt="Chapter 8b screenshot 66" width="74%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_67.png" alt="Chapter 8b screenshot 67" width="75%" style="border: 1px solid #999;">

7\. **Both settings match the original configuration:**

- Submission requires membership in **ziptieai (organization)**.
- **Allow Foundry Automate to submit this action** is **ON**.

8\. If changes are still pending, click **Save** and confirm.

**8a.2 is then complete:** group restriction → blocked access → add membership → successful submission → restore original restriction.

<br>

<a id="section-8b-3-inspect-action-configuration-history-and-execution-history"></a>



### **8b.3 Inspect Action configuration history and execution history**

**This is inspection, not an allow/block test.** Its demonstration is simply to trace a saved response back to the Action or automation execution.

We’ll inspect the **manual A2 submission** first, then an **automatic A2 execution**.

<img src="/assets/qs/8b_68.png" alt="Chapter 8b screenshot 68" width="77%" style="border: 1px solid #999;">

<br>

<a id="section-8b-3-1-find-the-manual-submission"></a>



#### **8b.3.1 Find the manual submission**

1\. Open **Ontology Manager → 693_CheckAndSaveRecord (A2 Action)**.

2\. Click **History** in the left sidebar.

3\. Show that screen.

<img src="/assets/qs/8b_69.png" alt="Chapter 8b screenshot 69" width="97%" style="border: 1px solid #999;">

4\. We’ll identify whether it shows **Action submissions** or **changes to the Action’s configuration** before choosing the next step. This **History** shows changes to **A2’s configuration**, including the group restriction and its restoration—not changes to **CheckResult**.

5\. Click **Observability** immediately below **History** and show that screen. That is where we’ll look for A2 submission records.

<img src="/assets/qs/8b_70.png" alt="Chapter 8b screenshot 70" width="97%" style="border: 1px solid #999;">

6\. This is the right screen: Observability → Run history. It lists:

- **5:05 PM and 5:04 PM:** executions with **A2 Action** as the caller.
- **2:02 PM and 1:47 PM:** executions with the **updated-object automation** as the caller.

7\. Click the newest **5:05:49 PM** row and show the details. We’ll check whether it identifies the submitting user and the affected object.

<img src="/assets/qs/8b_71.png" alt="Chapter 8b screenshot 71" width="63%" style="border: 1px solid #999;">

This is the execution **Trace**. It shows the sequence **Action → Logic function → LLM call**, with timings.

8\. Click **Details** beside **Trace** at the top. Show that panel so we can look for the submitting user and execution information.

9\. Leave **Edit permissions** unchanged.

<br>

<a id="section-8b-3-2-675-can-this-data-can-be-used-programmatically-for-example-to-generate-warnings"></a>



#### **8b.3.2 (675) Can this data can be used programmatically (for example, to generate warnings)**

Yes—execution information can support automated warnings, such as:

- An Action fails.
- Execution takes too long.
- An automation repeatedly fails.

The visible **“Monitor this action”** button is the built-in starting point for configuring alerts.

<br>

<a id="section-8b-3-3-for-custom-code"></a>



#### **8b.3.3 For custom code**

Foundry provides observability and monitoring APIs, but we would need to verify which execution fields and APIs are available in your environment. We should not assume that every detail visible in this trace is programmatically accessible. Also, **execution monitoring is not necessarily a property-change audit**: detecting “A2 failed” is different from identifying “who changed CheckResult from FOUND to NOT FOUND.”


<br>

<a id="section-8b-3-4-summary"></a>


#### **8b.3.4 Summary**

We verified:

- **History:** who changed A2’s configuration.
- **Observability → Run history:** successful executions and their callers.
- **Trace:** Action → Logic function → LLM call, with timings.
- **Chapter 8a automation history:** which object triggered an automatic execution. **Limitation:** we did not verify a property-level audit showing who changed **CheckResult**, with its old and new values. So a more accurate section title is:
- **8a.3 Inspect Action configuration history and execution history**

<br>

<a id="section-8b-4a-inspect-llm-data-access-controls-restriction-not-tested"></a>

### **8b.4a Inspect LLM data-access controls (restriction not tested)**

For the LLM example, distinguish who can call the function from whether particular data may be processed by a model. They are different controls. We should verify which mechanisms your enrollment supports before writing those instructions.

A useful chapter pattern:

- Run successfully → apply restriction → repeat and observe the block → restore access
- Two or three examples are enough. A second test user is important for access demonstrations; testing only as the owner can hide the effect.

<br>

<a id="section-8b-4a-1-inspect-the-model-controls"></a>

#### **8b.4a.1 Inspect the model controls**

**AIP logic**

1\. Open **693_AIPL_CheckRecord (AIPL)** in **AIP Logic**.

2\. Open **Config**.

3\. In **Use LLM → Model**, open the dropdown currently showing **GPT-5.6 Sol**.

4\. Show that menu, including any policy or model-information controls. **Do not change the model or publish anything.** We need to identify the available governance controls—choosing a model alone is not a data-use restriction.

<img src="/assets/qs/8b_72.png" alt="Chapter 8b screenshot 72" width="99%" style="border: 1px solid #999;">

5\. This menu shows **model selection and technical details**, not data-use restrictions.  Click the **↗ arrow beside GPT-5.6 Sol** at the top-right of its information card, and show the page it opens. Leave the model selection and **User-scoped execution** unchanged—the latter controls execution-log visibility, not whether data may be sent to the LLM.

<img src="/assets/qs/8b_73.png" alt="Chapter 8b screenshot 73" width="67%" style="border: 1px solid #999;">

**You’re now in Model Catalog → GPT-5.6 Sol (model).**

- This page shows the provider, terms, and a playground—not data-access restrictions.
- The documented controls are in **Control Panel → AIP settings**. Administrators can manage model availability there and configure which marked data LLMs may process.
- Enable AIP features / Enable LLMs

**Next: Open Control Panel → AIP settings**

**Do not disable any models or change policies yet.** If that section is unavailable to your account, we’ll mark this part as inspection-only.

<img src="/assets/qs/8b_74.png" alt="Chapter 8b screenshot 74" width="92%" style="border: 1px solid #999;">

**AIP settings**

In **Control Panel**:

1\. Click **What setting are you looking for?**

2\. Search for **AIP**.

3\. Open **AIP settings** if listed.

Show that screen. **Do not change any settings yet.**

<img src="/assets/qs/8b_75.png" alt="Chapter 8b screenshot 75" width="43%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_76.png" alt="Chapter 8b screenshot 76" width="88%" style="border: 1px solid #999;">

<br>

<a id="section-8b-4a-2-693-this-is-the-relevant-governance-screen-control-panel-aip-settings"></a>


#### **8b.4a.2 (693) This is the relevant governance screen: Control Panel → AIP settings**

Three different controls are visible:

- **Palantir model access for custom workflows:** who may use the models.
- **Data access:** which **marked data** may be passed to LLMs. Currently **Allow any data** is selected.
- **Palantir models** tab: controls for individual model families.

**Important:** the Data access description says **unmarked data is always allowed when AIP is enabled**. Simply enabling a marking restriction would therefore not block our unmarked demo data.

Leave this page unchanged.

**Click Palantir models (tab) at the top**

1\. Show that tab so we can inspect whether a model-specific, reversible test is available.

<img src="/assets/qs/8b_77.png" alt="Chapter 8b screenshot 77" width="81%" style="border: 1px solid #999;">

This tab controls **model-family availability**.

2\. In **Search models or model families…**, enter **GPT-5.6**.

3\. Show the matching entries. If there are no results, search **OpenAI** instead.

**4. Do not disable anything yet.** Disabling the family used by **693_AIPL_CheckRecord (AIPLF)** could also affect other workflows using that family.

<img src="/assets/qs/8b_78.png" alt="Chapter 8b screenshot 78" width="55%" style="border: 1px solid #999;">

**GPT-5.6 Sol appears under two providers: Direct OpenAI** and **Microsoft Azure**.

5\. Click **Manage** beside **OpenAI → Direct OpenAI**, then show the dialog. **Do not change or save anything yet.** We’ll inspect the scope of the controls before choosing a test.

<img src="/assets/qs/8b_79.png" alt="Chapter 8b screenshot 79" width="70%" style="border: 1px solid #999;">

<img src="/assets/qs/8b_80.png" alt="Chapter 8b screenshot 80" width="57%" style="border: 1px solid #999;">

This page controls **the whole Direct OpenAI model family**, not access to particular data.

- **Enable this model family:** allows or blocks that family.
- **Restrict access to select organizations:** limits which organizations can use it.

Leave both unchanged.

<br>

<a id="section-8b-4a-3-data-restrictions"></a>

#### **8b.4a.3 Data restrictions**

1\. Return to: Control Panel → AIP settings → AIP settings tab → Data access

2\. Select **Allow only the following markings** to reveal its controls, then show that area. **Do not click Save**—this is an enrollment-wide setting, and we’re inspecting it first.

<img src="/assets/qs/8b_81.png" alt="Chapter 8b screenshot 81" width="53%" style="border: 1px solid #999;">

The warning means **the marking allowlist is empty**.

3\. Click **Edit** beside **Markings** and show the picker. **Do not save the enrollment settings yet.** This control restricts **marked data** sent to LLMs; the text above explicitly says **unmarked data remains allowed**.

<img src="/assets/qs/8b_82.png" alt="Chapter 8b screenshot 82" width="49%" style="border: 1px solid #999;">

No selectable markings are visible to your account even with the filter off. We cannot complete a marking-based test with this picker as it stands. So Restore the unchanged configuration:

4\. Click **Cancel** in **Manage markings**.

5\. Select **Allow any data**, the original setting.

**6. Do not save any other changes.**

<br>

<a id="section-8b-4a-4-this-section-demonstrates-where-the-controls-are-not-a-verified-allow-block-test"></a>

#### **8b.4a.4 This section demonstrates where the controls are—not a verified allow/block test**

We inspected model-family enablement and the marking-based LLM data-access control. No selectable markings were available, so we did not apply or test a data restriction. Unmarked data remains allowed when AIP is enabled.

We’re finished with 8a.4 as an inspection-only section. But we **cannot conclude that your account doesn’t support the functionality**. The controls are present; the marking picker simply showed no choices. We haven’t established why—there may be no applicable markings configured, or your account may lack visibility to them.

The accurate conclusion is: **The LLM data-access controls are available, but we could not test a marking-based restriction because no selectable markings appeared. No restrictions were applied.**

<br>

<a id="section-8b-4b-hypothetical-control-which-data-may-be-sent-to-llms-config-workflow"></a>


### **8b.4b Hypothetical " Control which data may be sent to LLMs" config/workflow**

A trial user does not have access to this functionality. So this section simply describes the hypothetical (untested) config/workflow proposed by FDE.

<img src="/assets/qs/8b_83.png" alt="Chapter 8b screenshot 83" width="58%" style="border: 1px solid #999;">

**The demo we would perform would** Use **disposable test data**, not the existing Capstone2Record workflow.

1\. **Prepare two mandatory markings:** DemoAllowed and DemoRestricted.

2\. Protect the disposable test data with **DemoRestricted**, and give the test user access to that marking.

3\. **Baseline test:** run a small AIPL that sends the test text to an LLM. Verify it succeeds.

4\. In **Control Panel → AIP settings → Data access**, select **Allow only the following markings**.

5\. Include **DemoAllowed**, but exclude **DemoRestricted**, then save.

6\. Repeat the LLM call from a session with access to **DemoRestricted**. Verify the request is **blocked**.

7\. Add **DemoRestricted** to the allowlist and repeat. Verify the request **succeeds**.

8\. Restore the original **Allow any data** setting and remove the disposable test setup.

**Important mechanism:** this control checks the mandatory markings available to the **request’s session/token**, not merely the markings on the text actually sent. An excluded marking on the token can block the request even if that particular prompt contains unmarked text.

Control LLM data access with Markings: Because this setting affects the enrollment, we would record its original state and coordinate the test before applying it.


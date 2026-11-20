---
layout: page
title: 3 Create own project with datasets
permalink: /pal_qs0_3_download_ds/
---

<br>


<!-- 3 Create own project with datasets -->
[← 2 Install marketplace app and test](/pal_qs0_2_install_mplace/) / [↑ 3.2 Foundry QS0](/pal_qs0/) / [→ 4 Build pipeline](/pal_qs0_4_pipeline/)

_Converted 2026-11-19 01:53 PM EST_

<br>

The next step is now to create everythings ourselves except the datasources.

Create new project, import the data sources , hten build the rest?

**T****hat is a cleaner approach than deleting the installed example.**

Keep **QS0b** as the reference installation and build your version in a new project.

**TOC**
- [3.2 Datasets (1) save locally then (2) import](#3-2-datasets-1-save-locally-then-2-import)
  - [Proposed sequence](#proposed-sequence)
  - [Download as CSV is visible in your first screenshot.](#download-as-csv-is-visible-in-your-first-screenshot)
- [3.3 Next: create the independent build project](#3-3-next-create-the-independent-build-project)
- [3.4 Import ELINT Example.csv](#3-4-import-elint-example-csv)
  - [ELINT Example imported successfully. The preview shows:](#elint-example-imported-successfully-the-preview-shows)
- [3.5 Import the second dataset](#3-5-import-the-second-dataset)
  - [CV ATR GEOINT Example imported successfully:](#cv-atr-geoint-example-imported-successfully)
  - [Data preparation is complete](#data-preparation-is-complete)

<br>

<a id="3-2-datasets-1-save-locally-then-2-import"></a>
### **3.2 Datasets (1) save locally then (2) import**

Downloading and reimporting gives the new project independent input datasets.

Your screenshots show approximately:

Those are Foundry’s displayed storage sizes; the downloaded files may differ. Both are small enough for a local download/upload exercise.

<br>

<a id="proposed-sequence"></a>
#### **Proposed sequence**

1\. **Download** each original input dataset.

2\. Create **QS0_Build (project)**.

3\. **Upload/import** both files as new datasets.

4\. Verify column types, timestamps, geometry strings, and row counts.

5\. Build the new pipeline from those imported datasets.

**CSV is beginner-friendly**, but we must verify the schema after importing: timestamps and geometry values may otherwise be interpreted as plain text or parsed incorrectly.

Start with **ELINT Example (dataset) → All actions** and show the menu. We’ll find the available download option and choose the format before proceeding.

<img src="/assets/qs0/ch3/3_01.png" alt="" width="92%" style="border: 1px solid #999;">

<img src="/assets/qs0/ch3/3_02.png" alt="" width="52%" style="border: 1px solid #999;">

<br>

<a id="download-as-csv-is-visible-in-your-first-screenshot"></a>
#### **Download as CSV is visible in your first screenshot.**

1\. Click **Download as CSV** for **ELINT Example (dataset)**.

2\. Keep the downloaded file as:

ELINT Example.csv

<img src="/assets/qs0/ch3/3_03.png" alt="" width="44%" style="border: 1px solid #999;">

1\. Repeat for **CV ATR GEOINT Example (dataset)**:

CV ATR GEOINT Example.csv

<img src="/assets/qs0/ch3/3_04.png" alt="" width="44%" style="border: 1px solid #999;">

<img src="/assets/qs0/ch3/3_05.png" alt="" width="66%" style="border: 1px solid #999;">

**Don’t open and resave them in Excel**—it can alter timestamps or other values. We’ll import the downloaded CSVs directly into Foundry.

If a download dialog offers a choice, select **all rows**, not just the preview sample.

Once both files are downloaded, we’ll create **QS0_Build (project)** and upload them.

Both CSVs downloaded successfully:

- **ELINT Example.csv:** 4.93 MB

- **CV ATR GEOINT Example.csv:** 15.1 MB

The CSV exports are larger than Foundry’s displayed storage sizes. That is normal; the formats and compression differ.

The first screenshot is a **download-governance checkpoint**, not a download error.

<br>

<a id="3-3-next-create-the-independent-build-project"></a>
### **3.3 Next: create the independent build project**

1\. Open **Projects & files**.

<img src="/assets/qs0/ch3/3_06.png" alt="" width="99%" style="border: 1px solid #999;">

2\. At the namespace level, select **New → New project**.

<img src="/assets/qs0/ch3/3_07.png" alt="" width="45%" style="border: 1px solid #999;">

3\. Name it:

```

QS0_Build

```

Use the same project/security setup as **QS0b**.

4\. Show the new project’s file page. We’ll upload the CSVs one at a time and verify their schemas.

<img src="/assets/qs0/ch3/3_08.png" alt="" width="44%" style="border: 1px solid #999;">

<img src="/assets/qs0/ch3/3_09.png" alt="" width="46%" style="border: 1px solid #999;">

QS0_Build (project) is created and empty.

<br>

<a id="3-4-import-elint-example-csv"></a>
### **3.4 Import ELINT Example.csv**

Drag **ELINT Example.csv** from your Downloads folder into the project’s empty **Files** area.

Show the upload/import dialog that opens. We’ll check the dataset name, CSV parsing, and column types before completing the import.

<img src="/assets/qs0/ch3/3_10.png" alt="" width="44%" style="border: 1px solid #999;">

<img src="/assets/qs0/ch3/3_11.png" alt="" width="44%" style="border: 1px solid #999;">

Keep **Upload as a structured dataset** selected, then click **Next…**.

This makes the CSV available as rows and columns for Pipeline Builder. Show the next screen so we can check its parsing and schema.

<img src="/assets/qs0/ch3/3_12.png" alt="" width="44%" style="border: 1px solid #999;">

This is the **access-requirements screen**, before parsing.

It shows:

- **Organization:** ziptieai

- **Other markings:** none

If these match the original dataset’s access requirements, leave them unchanged and click **Keep changes**.

Show the next screen. We should preserve any source markings rather than remove them during reimport.

<img src="/assets/qs0/ch3/3_13.png" alt="" width="44%" style="border: 1px solid #999;">

<img src="/assets/qs0/ch3/3_14.png" alt="" width="44%" style="border: 1px solid #999;">

You’re back at **Configure upload**. The upload has **one organization marking**, and the other-markings editor showed none selected.

Click **Upload** at the bottom right. After it completes, open the new **ELINT Example (dataset)** in **QS0_Build (project)** and show its Preview/schema screen. We still need to verify CSV parsing and column types.

<img src="/assets/qs0/ch3/3_15.png" alt="" width="44%" style="border: 1px solid #999;">

<img src="/assets/qs0/ch3/3_16.png" alt="" width="44%" style="border: 1px solid #999;">

<img src="/assets/qs0/ch3/3_17.png" alt="" width="77%" style="border: 1px solid #999;">

<img src="/assets/qs0/ch3/3_18.png" alt="" width="66%" style="border: 1px solid #999;">

<img src="/assets/qs0/ch3/3_19.png" alt="" width="99%" style="border: 1px solid #999;">

<br>

<a id="elint-example-imported-successfully-the-preview-shows"></a>
#### **ELINT Example imported successfully. The preview shows:**

- **3,206 total rows**—only 300 are displayed in the preview.

- **11 columns**.

- **timestamp:** recognized as datetime.

- **longitude, latitude, semi_major_axis, semi_minor_axis, orientation:** Double.

- **track_id, elnot, geometry, h3_index_2, elint_geometry:** String.

The geometry JSON remains inside its String columns; it has not split into extra CSV columns. **No schema changes are needed here.**

<br>

<a id="3-5-import-the-second-dataset"></a>
### **3.5 Import the second dataset**

Return to **QS0_Build (project)** and drag in:

```

CV ATR GEOINT Example.csv

```

Choose **Upload as a structured dataset** and follow the same upload process. Keep the required access markings.

Then open its Preview and show the column headers and total row count. We’ll verify its **10 columns**, particularly **detection_timestamp**, **confidence_score**, and the geometry fields.

<img src="/assets/qs0/ch3/3_20.png" alt="" width="66%" style="border: 1px solid #999;">

<img src="/assets/qs0/ch3/3_21.png" alt="" width="44%" style="border: 1px solid #999;">

<img src="/assets/qs0/ch3/3_22.png" alt="" width="99%" style="border: 1px solid #999;">

<br>

<a id="cv-atr-geoint-example-imported-successfully"></a>
#### **CV ATR GEOINT Example imported successfully:**

- **24,019 total rows**, with 300 displayed in the preview.

- **10 columns**.

- **confidence_score:** Double.

- **detection_timestamp:** datetime.

- Geometry and H3 fields remain Strings.

- **source_sensor_type:** null in the displayed rows, as in the supplied data.

<br>

<a id="data-preparation-is-complete"></a>
#### **Data preparation is complete**

**QS0_Build (project)** now has two independent inputs:

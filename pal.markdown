---
layout: page
title: 3c Enterprise
permalink: /pal/
---

<br>

The enterprise platform controls almost everything. For now this is just Palantir.

Demos (*I added numbering, conceptual diagrams, and a few error updates to the original demos*)
- **[D1: Palantir Foundry "speedrun" (quick start) (26.0705)](/3c.1_pal_foundry/)**. 
  - Demo complete... still need to write the webpage.
  - #610_pal_1_foundry_v02_26.0704_SS.docx  
  - https://learn.palantir.com/speedrun-your-first-e2e-workflow/1944887 
- **[D2: Palantir AIP "speedrun" (quick start) (26.0706)](/3c.2_pal_aip/)**. 
  - Tis is just a rough summary for now...
  - 611vvv_pal_2_aip_qs_v07_26.0713_SS (2).docx
  - https://learn.palantir.com/speedrun-your-e2e-aip-workflow
- **[D3: Palantir agentic AI "speedrun" (quick start) (26.0713)](/3c.3_pal_agentic_ai/)**.
  - #614_pal_3_agentic_ai_qs_v03_26.0715_ss.docx 
  - https://learn.palantir.com/speedrun-your-first-agentic-aip-workflow
- **[D4: Palantir ontology function "speedrun" (quick start) (26.0717)](/3c.4_pal_ontology_function/)**. 
  - At the end of this page is *good demo of how FDE/GPT5.5 fixed a problem with the demo*.
  - #615_pal_4_onto_function_qs_v02_26.0717_ss (2).docx 
  - https://learn.palantir.com/speedrun-your-first-ontology-function/2131538
- **[D5: Speedrun: Mining Your First Business Process (26.0718)](/3c.5_pal_biz_process_mining/)**. 
  - #616_pal_5_biz_process_mining_qs_v02_26.0718_ss (1).docx
  - https://learn.palantir.com/speedrun-mining-your-first-business-process
- **D6: Deep Dive: Building Your First Pipeline (26.0719)**.
  - **Some of this failed**. FDE/GPT/OPUS could not fix. 
  - outdated (2+ years) demo? MAKE THE DEMOS SIMPLER AND KEEP THEM UPDATED. frustrating.
  - #617_pal_6_first_app_v01_26.0719_ss.docx. 
  - https://learn.palantir.com/deep-dive-building-your-first-application 
- **D7: Deep Dive: Building Your First Pipeline (26.0720)**.
  - #618_pal_7_first_pipeline_v01_26.0719_ss.docx
  - https://learn.palantir.com/deep-dive-building-your-first-pipeline


<br>*01* <br><img src="/assets/pal-demo-01.png" alt="drones" width="50%" style="border: 1px solid #999;">

<!--
Palantir
Microsoft Fabric
Vertex AI
Databricks
Snowflake
Now you're inside a governed ecosystem.
Security.
Permissions.
Lineage.
Governance.
Enterprise data.
Job value: ★★★★★
Highest salaries.
Fewest jobs.
Hardest to enter.
-->

<br>

See also: 
- **[PAL notes](/3c.0_pal_notes/)**
- **Notes:**
  - *[Palantir CEO火力全开，场面控制不住了！](https://www.youtube.com/watch?v=feUFT1Q-oBA)*
  - *[zerohedge.com/ai/something-has-gone-completely-wrong-palantirs-alex-karp-goes-ballistic-openai-anthropic](https://www.zerohedge.com/ai/something-has-gone-completely-wrong-palantirs-alex-karp-goes-ballistic-openai-anthropic)*
  - *https://www.youtube.com/watch?v=lSDC6-BdVus?t=341 HBM, diagram of NN, interconnecting multiple GPUs*

<br>

--------------------------------------------------

<br>

Yes — another docs/UI mismatch.

The transform the docs call:

> **Extract rows from a JSON file**

may now appear under a different name, usually something like:

- **Parse JSON**
- **JSON to rows**
- **Extract records from JSON**
- **Read JSON files**
- **Files → JSON**
- **Create dataset from JSON**

## Most likely causes

### 1. You are in the wrong tool/mode

That step is probably meant for **Pipeline Builder**, not Workshop, Ontology Manager, or Functions.

You should be in something like:

```text
Pipeline Builder / Data pipeline / Add transform
```

Then search the transform picker for:

```text
json
```

not for the full phrase.

---

### 2. Your input is not a raw file dataset

The “extract rows from JSON file” transform usually appears only if the input is a **file-based dataset** containing JSON files.

If your input is already a structured dataset/table, Foundry may hide that transform because there is no JSON file to extract from.

---

### 3. The transform was renamed

The current equivalent is probably:

```text
Parse JSON
```

or:

```text
Read JSON
```

or:

```text
Extract records from JSON
```

## What I would try

1. Open the pipeline / transform builder.
2. Click **Add transform**.
3. Search only:

   ```text
   json
   ```

4. Pick the transform that converts JSON/file content into rows.
5. If nothing appears, confirm that your input is a raw JSON file dataset, not a structured table.

## Short answer

The docs are likely outdated. Look for **Parse JSON** or search for **json** in the transform picker. If no JSON transform appears, you are probably not using a raw JSON file dataset as the input.

<br>

----------------------------------


<br>


Python transforms run in a **Code Repository**, not directly in Pipeline Builder. Here are the steps:

## Step 1 — Create a Python Code Repository

1. From the Foundry home screen, click **New** and search for **Code Repository**.
2. Select **Python** as the language.
3. Give it a name (e.g. `transactions_json_parser`) and choose a location in your project folder.

## Step 2 — Install the required library

Once inside the repository, open the **Libraries** panel on the left side. Search for and install:

- `transforms-media` — required for `MediaSetInput` to read from your Media Set [[1]](https://ziptieai.usw-17.palantirfoundry.com/docs/foundry/transforms-python/media-sets#lightweight-support)

Commit the change after installing.

## Step 3 — Add the transform code

Open the default Python file (usually `transforms/my_transform.py`) and replace its contents with the script from before, updated with your actual output path:

```python
from transforms.api import transform, Output
from transforms.mediasets import MediaSetInput
import json
import pandas as pd

@transform(
    media_input=MediaSetInput("ri.mio.main.media-set.e6b065a6-5fc7-455d-8051-57c964cb03cd"),
    output=Output("/ziptieai-5313a6/Pal_7/pal_7_first_pipeline/transactions_parsed"),
)
def parse_json_transactions(media_input, output):
    rows = []
    for media_item in media_input.list_media_items():
        content = media_input.get_media_item(media_item.media_item_rid).read().decode("utf-8")
        for line in content.strip().splitlines():
            if line.strip():
                rows.append(json.loads(line))
    df = pd.DataFrame(rows, columns=[
        "transaction_id",
        "transaction_date",
        "units",
        "customer_id",
        "variation_id",
        "product_id"
    ])
    output.write_dataframe(df)
```

Update the `Output(...)` path to wherever you want the clean tabular dataset to land in your project.

## Step 4 — Build and run

Click the **Build** button (top right of the Code Repository). Foundry will run the transform and write the output dataset to the path you specified.

## Step 5 — Connect to Pipeline Builder

Once the output dataset exists, you can add it as an input node in ri.eddie.main.pipeline.2b185cec-e69d-480e-91f1-d3ce7d86a0fd and continue building your pipeline from there.

> **Note:** The `transforms-media` library is required because your source is a Media Set. [[1]](https://ziptieai.usw-17.palantirfoundry.com/docs/foundry/transforms-python/media-sets#lightweight-support) Without it, the `MediaSetInput` import will fail at build time.


<br>

---------------------------------------

<br>


Yes — it worked.

Your JSON file was processed into a structured dataset:

```text
transactions_parsed
```

You can see it has:

```text
50 rows
6 columns
```

Columns:

```text
transaction_id
transaction_date
units
customer_id
variation_id
product_id
```

So the flow succeeded:

```text
transactions_raw.json
        ↓
Python transform: fix json
        ↓
transactions_parsed dataset/table
```

A few notes:

- `units` was converted correctly to **double**.
- `transaction_date` is still **string**, which is okay for now because the source date format is messy JavaScript-style text.
- The output is a **Foundry dataset**, not another JSON file.
- The left panel confirms it was **Updated via `fix json`**, so your transform produced this dataset.

So yes: the file was processed, and the result is the dataset currently open in your screenshot.

<br>

------------------------

# this all looks correct (amazing .. thanks for your expert help)... but do i need to verify ? or is this already verification (looks like in the speedrun demo)

Yes — this preview is already a **basic verification**.

It shows the join is working:

- Left table: `clean transactions`
- Right table: `clean products`
- Join condition:

  ```text
  clean transactions.product_id = clean products.product_id
  ```

- Output preview has product fields added:

  ```text
  products_price
  products_product_name
  products_category
  ```

So visually, this matches the speedrun expectation.

## But I would still do two quick checks

### 1. Check for unmatched products

Because this is a **left join**, all transactions stay even if no product match exists. If there are unmatched rows, the product columns will be `null`.

In the preview, look at:

```text
products_price
products_product_name
products_category
```

If many are `null`, the join is not fully matching.

### 2. Check row count

Your input had **50 transaction rows**, but this preview shows:

```text
Previewing 172 rows
```

That could be okay if the products table has multiple rows per `product_id`, but it may also mean the join is multiplying rows.

This is important.

If each transaction should match exactly one product, then the joined result should still have about:

```text
50 rows
```

not 172.

## Possible issue

You are joining only on:

```text
product_id
```

But your data also has:

```text
variation_id
```

and the products table appears to have:

```text
products_variation_id
products_product_id
```

If product variations are unique, the correct join may need **both**:

```text
transaction.product_id = products.product_id
transaction.variation_id = products.variation_id
```

That would prevent row multiplication.

## Recommendation

Before moving on, add a second match condition:

```text
variation_id is equal to variation_id
```

or if prefixed on the right:

```text
variation_id is equal to products_variation_id
```

Then preview again.

Expected result:

```text
50 rows
```

If it becomes 50 rows, that is the correct join.


------------------


# yes, 50 rows :)

Great — that verifies the join is correct.

Before adding the second condition, the join produced 172 rows, which meant rows were being multiplied. After adding the variation/product match, it produces:


12
That matches the transaction input row count.

So your join is now logically correct:


123
And the output keeps:


12
with product details added.

So yes — this is verified.

<br>*01* <br><img src="/assets/pal-demo-7-01.png" alt="drones" width="100%" style="border: 1px solid #999;">

<br>

26.0719 (v1 26.0702)
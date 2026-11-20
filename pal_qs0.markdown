---
layout: page
title: 3.2 Foundry QS0 -- Detect/analyze haystack needles (start with Foundry example) (26.1119) (2.1)
permalink: /pal_qs0/
---

<br>



[← 3c Enterprise](/pal/)

26.1119 (v1 26.1118)


<br>

Chapters (extracted from docx)

- **[What this QS0 offers beginners](/pal_qs0_0a_best_demo/)**
- **[Short overview of all chapters (TOC)](/pal_qs0_0b_config_dias/)**
- **[1 First steps](/pal_qs0_1_introl/)**
- **[2 Install marketplace app and test](/pal_qs0_2_install_mplace/)**
- **[3 Create own project with datasets](/pal_qs0_3_download_ds/)**
- **[4 Build pipeline](/pal_qs0_4_pipeline/)**
- **[5 Create Object type](/pal_qs0_5_objectype/)**
- **[6 Display in Maps](/pal_qs0_6_maps/)**
- **[7 Create UI](/pal_qs0_7_ui/)**
- **[8 HN algorithm description](/pal_qs0_8_algorithm/)**

<br>


**Original [docx #686](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO) source file** (with notes).

BASED ON PAL example #11.  
- #622_pal_E11_geospatial_gaia_v03_26.0806_ss (v02_26.0729)

(4.0.3d) The algorithm is:
1.	4.6 (spatial) Join: create pairs where
ELINT.h3_index_2 = GEOINT.h3_index_2.
2.	4.7 Time filter: keep pairs where the GEOINT detection occurred between 10 minutes before and 1 day after the ELINT timestamp.
3.	4.8 Deduplicate: keep one arbitrary surviving pair per distinct combination of
(ELINT.track_id, ELINT.elint_geometry).
Step 3 does not keep just one combination overall—it keeps one row for each combination, yielding four rows in this example.

<img src="/assets/ALL-02bbb.png" alt="drones" width="68%" style="border: 1px solid #999;">


<img src="/assets/pal_10_20.png" alt="drones" width="44%" style="border: 1px solid #999;">



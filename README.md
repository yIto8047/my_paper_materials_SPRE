
---

## 🚀 How to Run (Google Colab)

1. Open the notebook:
   - Upload `SPRV.ipynb` to Google Colab  
   - Or open directly via GitHub link (if public)

2. Upload required CSV files when prompted:
   - `ARKS_Task1_with_Pi_and_DataSources.csv`
   - `arks_dictionary_J_ver3_phase0_asset_independent.csv`
   - `LG Asset.txt`
   - `BoE Asset.txt`
   - `Health Asset.txt`
   - 'technique_sector_long.csv'
     
3. Run cells sequentially.

4. Generated outputs:
   - AASG_SPRV_FREQUENCY_LG_LONG
   - AASG_SPRV_FREQUENCY_BoE_LONG
   - AASG_SPRV_FREQUENCT_Health_LONG
     
5. Generated Graph
     - Upload `SPRVGrapgGenerator.ipynb` to Google Colab
       
6. Upload required CSV files when prompted:
    - AASG_SPRV_FREQUENCY_LG_LONG
    - AASG_SPRV_FREQUENCY_BoE_LONG
   - AASG_SPRV_FREQUENCT_Health_LONG
     
7.Generated outputs:
    -Fig5_LG.png
    -Fig6_LG.png
    -Fig7_BoE.png
    -Fig8_BoE.png
    -Fig9_Health.png
    -Fig10_Health.png
---

## 📊 Input File Specifications

### 1️⃣ MITRE ATT＆CK STIXv2.0 for Enterprise v17.1 Json

Contains technique-level metadata.

| Column Name        | Description                                | Example        |
|-------------------|--------------------------------------------|---------------|
| technique_id      | MITRE ATT&CK Technique ID                 | T1059         |
| name              | Technique name                            | Command Exec  |
| frequency_score   | Calculated frequency metric               | 0.82          |
| applicable        | 1 = applicable / 0 = excluded             | 1             |

## 🏢 Sector-Specific Extension (Sector-Add)

AASG supports sector-specific scenario refinement through optional
sector-based filtering.

Certain attack techniques may be more relevant in specific industries
(e.g., Finance, Healthcare, Manufacturing).

### Sector Add Logic

Sector-specific weighting can be applied by:

- Adding sector relevance score per technique
- Filtering techniques based on sector applicability
- Adjusting risk propagation weights
---

### 2️⃣ relationships.csv

Represents technique co-occurrence or transition relationships.

| Column Name        | Description                          | Example   |
|-------------------|--------------------------------------|----------|
| source_id         | Source technique ID                  | T1059    |
| target_id         | Target technique ID                  | T1105    |
---

### 3️⃣ assets.csv

Defines target assets selected by analyst.

| Column Name | Description              | Example      |
|------------|--------------------------|-------------|
| asset_id   | Asset identifier         | A001        |
| asset_name | Logical asset name       | Web Server  |
| criticality| Asset criticality score  | 0.9         |

---

## ⚙️ Processing Overview

The notebook performs the following steps:

1. Load ATT&CK-derived technique dataset.
2. Compute importance score using:
   - Frequency metric
   - Applicability condition
3. Generate attack tree.
4. Construct multi-step attack scenario.
5. Apply stepwise propagated risk visualization.

---

## 🧪 Reproducibility Notes

- Tested on Google Colab (Python 3.10)
- Required libraries:
  - pandas
  - numpy
  - networkx
  - matplotlib

Install missing packages using:

```python
!pip install pandas numpy networkx matplotlib

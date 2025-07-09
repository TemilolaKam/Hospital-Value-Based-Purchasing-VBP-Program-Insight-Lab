# Hospital Value-Based Purchasing (VBP) Program Insight Lab

### Dataset

This project uses the public **FY 2025 Hospital VBP Total Performance Score file**
from the Centers for Medicare & Medicaid Services (CMS).  
* **2 489 rows** — one per eligible hospital  
* **17 columns** — identifiers + four weighted domain scores + Total Performance Score  
* Released under U.S. Government public-domain terms  
* Download URL: <https://data.cms.gov/provider-data/dataset/ypbt-wvdk#data-table>
  
### The Purpose
Forecast · Explain · Simulate — a workspace that turns Centers for Medicare & Medicaid Service’s FY-2025 HVBP dataset into decision-ready insight.

### ✨ Key features

Clean data pipeline — raw CMS CSV ➜ validated, typed parquet.

Exploratory dashboards — distributions, state choropleth, outlier table.

Baseline models — linear TPS clone + XGBoost top‑quartile classifier.

Explainability — SHAP global summary & per‑hospital waterfall charts.

Notebook‑native simulator — one helper function (simulate) for instant “what‑if” TPS and top‑quartile probability, plus ipywidget sliders.

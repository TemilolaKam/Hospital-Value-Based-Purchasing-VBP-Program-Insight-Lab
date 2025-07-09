# Hospital Value-Based Purchasing (VBP) Program Insight Lab

### Dataset

This project uses the public **FY 2025 Hospital VBP Total Performance Score file**
from the Centers for Medicare & Medicaid Services (CMS).  
* **2 489 rows** — one per eligible hospital  
* **17 columns** — identifiers + four weighted domain scores + Total Performance Score  
* Released under U.S. Government public-domain terms  
* Download URL: <https://data.cms.gov/provider-data/dataset/ypbt-wvdk#data-table>
  
### The Purpose
Hospital VBP Insight Lab is a fully‑reproducible workflow that turns Centers for Medicare & Medicaid Services FY‑2025 Hospital Value‑Based Purchasing file into four things every hospital leader wants:

| Business Need | Analytics Capability |
|----------|----------|
| Know our score early   | Linear model that exactly reproduces CMS Total Performance Score (TPS) from the four weighted domain columns.  |
| See the big picture   | Exploratory notebooks with distributions, a state‑level choropleth, and an outlier table that spotlights the 46 top performers.  |
| Understand what drives success   | XGBoost classifier + SHAP plots showing Efficiency as the dominant lever, followed by Safety when present.   |
| Simulation   | A single simulate() helper (plus optional ipywidget sliders) that returns TPS, top‑quartile probability, and a SHAP waterfall explanation—live inside Jupyter.   |


### ✨ Key features

Clean data pipeline — raw CMS CSV ➜ validated, typed parquet.

Exploratory dashboards — distributions, state choropleth, outlier table.

Baseline models — linear TPS clone + XGBoost top‑quartile classifier.

Explainability — SHAP global summary & per‑hospital waterfall charts.

Notebook‑native simulator — one helper function (simulate) for instant “what‑if” TPS and top‑quartile probability, plus ipywidget sliders.

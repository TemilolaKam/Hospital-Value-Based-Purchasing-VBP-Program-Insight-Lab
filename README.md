# Hospital Value-Based Purchasing (VBP) Program Insight Lab

### 📌 Motivation

To build a data science project that forecasts, explains, and simulates hospital performance under the Centers for Medicare & Medicaid Services FY-2025 Hospital Value-Based Purchasing program, enabling hospitals to self-score, test improvement scenarios, and understand domain drivers.

### Dataset

This project uses the public **FY 2025 Hospital VBP Total Performance Score file**
from the Centers for Medicare & Medicaid Services (CMS).  
* **2 489 rows** — one per eligible hospital  
* **17 columns** — identifiers + four weighted domain scores + Total Performance Score (TPS) 
* Released under U.S. Government public-domain terms  
* Download URL: <https://data.cms.gov/provider-data/dataset/ypbt-wvdk#data-table>

### 🛠️ Libraries Used

* pandas – data manipulation
* numpy – numerical operations
* scikit-learn – regression, classification, preprocessing
* xgboost – top-quartile prediction model
* shap – explainability (global and local)
* matplotlib, plotly – visualizations
* ipywidgets – interactive sliders in notebooks
  
### The Purpose

| Business Need | Analytics Capability |
|----------|----------|
| Know our score early   | Linear model that exactly reproduces CMS Total Performance Score (TPS) from the four weighted domain columns.  |
| See the big picture   | Exploratory notebooks with distributions, a state‑level choropleth, and an outlier table that spotlights the 46 top performers.  |
| Understand what drives success   | XGBoost classifier + SHAP plots showing what features drives total performance score the most from hospital with the top 25%  TPS  |
| Simulation   | A single simulate() helper (plus optional ipywidget sliders) that returns TPS, top‑quartile probability, and a SHAP waterfall explanation—live inside Jupyter.   |

### 📁 Repository Structure

| Folder/File | Description |
|----------|----------|
| data/raw/| Original CMS FY-2025 CSV data |
| data/processed/  | Cleaned parquet data after validation   |
| notebooks/  | Jupyter notebooks for each phase (01_load_validate to 05_simulator_demo)  |
| models/  | Saved regression and XGBoost models   |
| figures/  | Generated plots, waterfalls, and summary visuals   |


### ✨ Key features

*  Clean data pipeline — raw CMS CSV ➜ validated, typed parquet.

*  Exploratory dashboards — distributions, state choropleth, outlier table.

*  Baseline models — linear TPS clone + XGBoost top‑quartile classifier.

*  Explainability — SHAP global summary & per‑hospital waterfall charts.

*  Notebook‑native simulator — one helper function (simulate) for instant “what‑if” TPS and top‑quartile probability, plus ipywidget sliders.


### 📊 Summary of Results

*  Phase 1: Cleaned and validated CMS data, ensuring all domain scores are numeric.

*  Phase 2: Conducted EDA showing Efficiency and Safety as dominant drivers; mapped TPS by state; identified 46 outlier hospitals.

*  Phase 3: Built a linear regression model to replicate CMS TPS calculation and an XGBoost classifier predicting top-quartile hospitals with PR-AUC ≈ 0.97.

* Phase 4: Generated SHAP global summary plots and per-hospital waterfall explanations for transparency.

*  Phase 5: Developed a notebook-native simulator with ipywidget sliders to test “what-if” scenarios instantly within Jupyter Lab.
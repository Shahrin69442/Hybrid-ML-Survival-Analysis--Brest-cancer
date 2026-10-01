# Scaling Hybrid Machine Learning & Causal Inference Framework to High-Dimensional Genomic Data for Cancer Patient Survival Analysis

[![Python 3.x](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![R Statistics](https://img.shields.io/badge/R-Survival%20Package-green.svg)](https://www.r-project.org/)
[![Framework](https://img.shields.io/badge/Architecture-Hybrid%20ML%20%2B%20Causal-orange.svg)]()
[![Google Colab](https://img.shields.io/badge/Platform-Google%20Colab-yellow.svg)](https://colab.research.google.com/)

## Abstract & Research Motivation
Modern healthcare analytics requires bridging the gap between high-performance predictive modeling and rigorous biostatistical inference. While Python (`scikit-learn`, `XGBoost`) dominates scalable pattern recognition and classification tasks, R remains the undisputed gold standard for survival analysis and causal inference (`survival`, Cox Proportional Hazards). 

This project implements an enterprise-grade **Cross-Paradigm Hybrid Framework** that achieves runtime interoperability between Python and R via `rpy2`, applying it to high-dimensional genomic and clinical datasets (e.g., CPTAC Breast Cancer Proteomes) to predict patient survival trajectories and evaluate prognostic biomarkers.

---

## Core Architecture & Pipeline

1. **Predictive Engine (Python & XGBoost):**
   - High-dimensional data processing and feature engineering on genomic/clinical matrices (`12,553 × 86` proteomic profiles).
   - Optimized `XGBoost` classifier to model non-linear interactions and evaluate patient mortality risk.

2. **Causal & Survival Engine (R & Runtime Interoperability):**
   - Seamless data bridging using `rpy2` inside Google Colab.
   - Non-parametric **Kaplan-Meier Survival Analysis** and multivariate **Cox Proportional Hazards Models** (`coxph`).
   - Rigorous statistical validation via Likelihood Ratio, Wald, and Log-rank tests.

---

## Tech Stack & Dependencies
* **Languages:** Python, R
* **Machine Learning:** XGBoost, Scikit-Learn
* **Biostatistics & Survival:** R `survival` package
* **Interoperability:** `rpy2` (Runtime Data Bridging)
* **Environment:** Google Colab

---

## Getting Started & Execution

To run this project interactively in Google Colab:

1. Open a new notebook in [Google Colab](https://colab.research.google.com/).
2. Clone or copy the modular blocks from the source code.
3. Execute the environment setup and library configuration:
```python

Load your clinical and genomic datasets and execute the predictive and survival pipeline cells sequentially.
​Key Results & Metrics
​Predictive Performance: Evaluated via ROC-AUC curves and classification accuracy metrics on clinical endpoints.
​Survival Modeling: Generated robust Concordance Indexes (C-index) and hazard ratios with associated p-values reflecting clinical significance.
​Future Scope
​Scaling the architecture to full-scale multi-omics longitudinal clinical trials.
​Integrating deep learning survival models (e.g., DeepSurv) into the hybrid pipeline.
​Author
​Md Shahrin Parvez
Final-Year Statistics Student | Aspiring Biostatistician & Health Data Scientist
!pip install -q xgboost scikit-learn pandas numpy matplotlib seaborn rpy2
import rpy2
%load_ext rpy2.ipython

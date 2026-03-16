# Perinatal & Child Health Research

**Victor et al. | London School of Hygiene and Tropical Medicine (LSHTM)**

This repository contains code, outputs and published papers from research on perinatal and child health outcomes.

---

## Paper 1 — Implications for Newborn and Child Growth Classification

**Vesel L, Victor A, et al. (BJOG 2026)**
*Implications for Newborn and Child Growth Classification Using INTERGROWTH-21st and WHO Child Growth Standards*

Evidence on implications of using global growth standards across populations (LIFE dataset).

- `papers/implications/` — Published paper (PDF), supplementary evidence (S3), tables and figures

---

## Paper 2 — Predictive Modelling of Stillbirth and Neonatal Mortality in Sub-Saharan Africa

### Multicountry Analysis — Classical, Machine Learning and AI Models

TRIPOD/PROBAST-aligned systematic review and multicountry predictive modelling analysis.

---

## Overview

This repository contains the code and outputs for a systematic review and predictive modelling study of perinatal outcomes (stillbirth, neonatal death, perinatal death) across Sub-Saharan Africa, using data from 38 countries.

### Models Implemented

| Family | Models |
|--------|--------|
| Classical | Logistic Regression (L1/L2/Elastic Net) |
| Machine Learning | Random Forest, XGBoost, LightGBM, CatBoost |
| AI/Deep Learning | MLP (PyTorch + Optuna hyperparameter tuning) |

### Evaluation Framework

- **Discrimination**: AUROC (c-statistic), AUPRC
- **Calibration**: CITL, Calibration Slope, E/O Ratio, Brier Score
- **Clinical Utility**: Decision Curve Analysis (net benefit / 1,000 births)
- **Internal Validation**: Nested 5-fold CV + Bootstrap optimism-adjusted
- **Transportability**: IECV leave-one-country-out (38 SSA countries)
- **Fairness**: EOD, DPD by study, country, SES, education, age, parity
- **Interpretability**: SHAP (global + local), permutation importance, PDP

---

## Repository Structure

```
.
├── papers/
│   └── implications/                     # BJOG 2026 — Growth Standards
│       ├── BJOG_2026_Vesel_*.pdf         # Published paper
│       ├── S3_Evidence_*.docx            # Supplementary evidence (Audencio)
│       ├── S3_Supplementary_Tables.docx  # Supplementary tables
│       └── S3_Supplementary_Figures.docx # Supplementary figures
├── notebooks/
│   └── SSA_Perinatal_Proto.ipynb         # Main analysis notebook (Colab-ready)
├── outputs/
│   └── paper/
│       └── global/                       # Published figures and summary tables
├── figures/
│   └── DeepLearning_Architectures*       # Architecture diagrams
├── .gitignore
└── README.md
```

## How to Run

1. Upload `notebooks/SSA_Perinatal_Proto.ipynb` to **Google Colab**
2. Mount Google Drive and set `DATA_PATH` to your data location
3. Run all cells: *Runtime → Run all*

> **Note:** Raw data files are not included in this repository for privacy and ethical reasons.

## License

This project is part of academic research at LSHTM. Please contact the authors for data access and collaboration requests.

## Contact

- **Audencio Victor** — audenciovictor@gmail.com
- London School of Hygiene and Tropical Medicine

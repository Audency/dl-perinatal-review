# Perinatal & Child Health Research

**Audencio Victor | London School of Hygiene and Tropical Medicine (LSHTM)**

Repository for published papers, analysis code and outputs from research on perinatal and child health outcomes.

> Raw/individual-level data are **not** included for privacy and ethical reasons.

---

## Publications

### 1. Implications for Newborn and Child Growth Classification Using INTERGROWTH-21st and WHO Child Growth Standards

**Vesel L, Strout S, Parker S, Victor A, Ngatia B, Ohuma EO.**
*BJOG: An International Journal of Obstetrics & Gynaecology*, 2026.
DOI: [10.1111/1471-0528.701861](https://doi.org/10.1111/1471-0528.701861)

Secondary analysis of the LIFE study (Malawi & Tanzania, n = 608 moderately low birthweight infants) comparing how WHO Child Growth Standards and INTERGROWTH-21st standards affect growth classification and trajectory interpretation across gestational age groups. Z-scores (WAZ, LAZ, HCAZ) were computed at birth and longitudinally (0-6m, 6-12m, 12-24m) using conditional growth models.

**Files:**

| File | Description |
|------|-------------|
| `papers/implications/BJOG_2026_Vesel_Implications_Growth_Standards.pdf` | Published paper |
| `papers/implications/S3_Evidence_Implications_Growth_Standards_Audencio.docx` | S3 — Supplementary evidence |
| `papers/implications/S3_Supplementary_Tables.docx` | Supplementary tables |
| `papers/implications/S3_Supplementary_Figures.docx` | Supplementary figures |

---

### 2. Predictive Modelling of Stillbirth and Neonatal Mortality in Sub-Saharan Africa *(in progress)*

**Victor A et al. | LSHTM**

Multicountry systematic review and predictive modelling of perinatal outcomes (stillbirth, neonatal death, perinatal death) across 38 Sub-Saharan African countries. TRIPOD/PROBAST-aligned.

| Family | Models |
|--------|--------|
| Classical | Logistic Regression (L1 / L2 / Elastic Net) |
| Machine Learning | Random Forest, XGBoost, LightGBM, CatBoost |
| Deep Learning | MLP (PyTorch + Optuna) |

**Evaluation:** AUROC, AUPRC, calibration (CITL, slope, E/O, Brier), DCA, nested 5-fold CV, bootstrap optimism-adjusted, IECV leave-one-country-out, fairness (EOD, DPD), SHAP.

**Files:**

| File | Description |
|------|-------------|
| `notebooks/SSA_Perinatal_Proto.ipynb` | Main analysis notebook (Google Colab-ready) |
| `outputs/paper/global/*.png` | Published figures |
| `outputs/paper/global/*_table.csv` | Summary tables for figures |
| `figures/DeepLearning_Architectures*` | Architecture diagrams |

**How to run:**
1. Upload `notebooks/SSA_Perinatal_Proto.ipynb` to Google Colab
2. Mount Google Drive and set `DATA_PATH`
3. *Runtime > Run all*

---

## Repository Structure

```
.
├── papers/
│   └── implications/                          # BJOG 2026 — Growth Standards
│       ├── BJOG_2026_Vesel_*.pdf              # Published paper
│       ├── S3_Evidence_*.docx                 # Supplementary evidence
│       ├── S3_Supplementary_Tables.docx
│       └── S3_Supplementary_Figures.docx
├── notebooks/
│   └── SSA_Perinatal_Proto.ipynb              # Predictive modelling notebook
├── outputs/
│   └── paper/global/                          # Figures and summary tables
├── figures/
│   └── DeepLearning_Architectures*            # Architecture diagrams
└── .gitignore
```

## Contact

**Audencio Victor** — audenciovictor@gmail.com
London School of Hygiene and Tropical Medicine

# Heart Failure Readmission - Predictive analysis

Dataset from [Kaggle](https://www.kaggle.com/datasets/nudratabbas/heart-failure-readmission-and-sdoh-dataset/)

---

## Overview
This project builds a predictive model to identify heart failure patients at 
risk of hospital readmission within 30 days. Early identification of high-risk 
patients can support clinical decision-making and reduce preventable readmissions.

---

## Dataset
The dataset contains 3,000 patient records with 16 features covering clinical 
measurements, medication usage, and social determinants of health (SDoH).

| Feature | Description |
|---|---|
| `age`, `gender`, `bmi` | Patient demographics |
| `bnp`, `sodium`, `creatinine` | Clinical lab values |
| `systolic_bp`, `heart_rate` | Vital signs |
| `ace_inhibitor`, `beta_blocker`, `diuretic` | Medication usage |
| `adherence_score` | Medication adherence (0–1) |
| `income_level` | Low / Medium / High |
| `distance_to_hospital_km` | Distance to nearest hospital |
| `readmitted_30d` | Target — 1 if readmitted within 30 days |

---

## Key Findings
- The 65% accuracy ceiling is consistent across all models, suggesting the 
  signal in the dataset is genuinely weak — no feature correlates with 
  readmission above 0.19
- Medication adherence is the strongest single predictor of readmission
- Class weighting shifts the decision boundary to catch more at-risk patients 
  at the cost of more false alarms — a worthwhile trade-off in a clinical setting
- Income level and gender contribute near-zero predictive value

---

## Requirements
pandas
numpy
matplotlib
seaborn
scikit-learn

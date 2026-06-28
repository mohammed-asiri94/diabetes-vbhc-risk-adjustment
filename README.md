# 🏥 VBHC Risk Adjustment — Diabetic Patient Readmission

## Overview
End-to-end data science project applying **Value-Based Health Care (VBHC)** methodology to predict and risk-adjust 30-day hospital readmissions for diabetic patients.

## 🎯 Objective
- Predict which patients will be readmitted within 30 days
- Apply **Risk Adjustment** for fair comparison between admission types
- Calculate **O/E Ratio** and **Case Mix Index** — core VBHC metrics

## 📊 Dataset
- **Source:** UCI ML Repository — Diabetes 130-US Hospitals (1999-2008)
- **Size:** 101,766 encounters × 50 variables
- **Target:** Readmission within 30 days (11.2% positive rate)

## 🔬 Methodology
```
1. Exploratory Data Analysis (EDA)
2. Feature Engineering
3. Logistic Regression (AUC = 0.66 | Sensitivity = 67.8%)
4. Risk Adjustment → O/E Ratio + Case Mix Index
```

## 📈 Key Findings
| Finding | Detail |
|---------|--------|
| Strongest predictor | `number_inpatient` |
| Highest OR | `age[20-30)` OR ≈ 3.0 |
| Emergency O/E | 1.000 — fair performance after adjustment |
| Moderate risk group | O/E = 1.08 — needs clinical attention |

## 💡 VBHC Insight
> Emergency admissions appear worst (11.6% crude rate) but O/E = 1.0 after risk adjustment. **Raw rates mislead. Risk-adjusted O/E tells the truth.**

## 🛠️ Tools
`R` · `tidyverse` · `ggplot2` · `pROC` · `caret` · `corrplot` · `broom`

## 📁 Files
```
├── diabetes_vbhc_risk_adjustment.Rmd   # Main analysis
├── diabetic_data.csv                   # Dataset
└── README.md
```

## 🚀 How to Run
```r
install.packages(c("tidyverse", "caret", "pROC",
                   "corrplot", "broom", "gridExtra"))
# Open .Rmd in RStudio and click Knit
```

**Author:** Mohammed Asiri | UNSW Sydney

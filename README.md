# ?? COMPAS Recidivism Risk Score Analysis

> A machine learning project that analyzes and predicts recidivism risk scores using the COMPAS dataset, with a focus on comparing multiple classification models.

---

## ?? Project Overview

This project explores the **COMPAS (Correctional Offender Management Profiling for Alternative Sanctions)** dataset, which is used by the US criminal justice system to assess the likelihood of a defendant re-offending (recidivism).

The goal is to build and evaluate machine learning models that predict the **risk score text** (Low / Medium / High) based on demographic features such as gender, ethnicity, and decile score.

---

## ?? Dataset

- **Source:** `compas-scores-raw.csv`
- **Features Used:**
  - `Sex_Code_Text` — Gender of the individual
  - `Ethnic_Code_Text` — Ethnicity of the individual
  - `DecileScore` — Numeric risk score (1–10 scale)
- **Target Variable:**
  - `ScoreText` — Risk level category: Low, Medium, or High

---

## ??? Technologies Used

| Tool | Purpose |
|------|---------|
| Python | Core programming language |
| Pandas | Data loading and preprocessing |
| Scikit-learn | Machine learning models and evaluation |
| Matplotlib | Data visualization |
| Google Colab | Development environment |

---

## ?? Methodology

1. **Data Loading** — Loaded and inspected the raw COMPAS dataset
2. **Feature Selection** — Selected relevant columns: Sex_Code_Text, Ethnic_Code_Text, DecileScore, ScoreText
3. **Encoding** — Applied LabelEncoder to categorical columns
4. **Feature Scaling** — Used StandardScaler to normalize features
5. **Cross-Validation** — Applied **5-Fold KFold Cross-Validation** for robust evaluation
6. **Model Training & Evaluation** — Trained and compared 3 classification models

---

## ?? Models Compared

| Model | CV Accuracy | CV F1 Score |
|-------|-------------|-------------|
| **Logistic Regression** | 99.93% | 99.89% |
| **K-Nearest Neighbors (KNN)** | 99.97% | 99.97% |
| **Ridge Classifier** | 85.09% | 83.49% |

> ?? **Best Model:** K-Nearest Neighbors (KNN) with 99.97% accuracy and F1 score.

---

## ?? Results Visualization

The project includes bar charts comparing:
- **Cross-Validation Accuracy** across all models
- **Cross-Validation F1 Score** across all models

---

## ?? How to Run

1. Open the notebook `crp_Omar_Abuhassan.ipynb` in **Google Colab** or **Jupyter Notebook**
2. Upload the `compas-scores-raw.csv` dataset to `/content/`
3. Run all cells in order

---

## ?? Project Structure

```
CRP/
+-- crp_Omar_Abuhassan.ipynb   # Main Jupyter Notebook
+-- compas-scores-raw.csv      # Dataset (not included, download separately)
+-- README.md                  # Project documentation
```

---

## ?? Ethical Considerations

The COMPAS dataset has been widely debated in the context of **algorithmic bias**. Studies have shown that the tool may exhibit racial bias. This project is purely academic and aims to analyze model performance, **not** to validate or endorse the use of COMPAS in real criminal justice decisions.

---

## ?? Author

**Omar Abuhassan**  
Computer Science Student

---

## ?? License

This project is for educational purposes only.

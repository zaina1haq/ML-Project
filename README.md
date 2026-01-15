# 🏥 Predicting 30-Day Hospital Readmission for Diabetic Patients

This project uses machine learning to predict whether diabetic patients will be **readmitted to the hospital within 30 days after discharge**, helping identify high-risk patients and support better post-discharge care planning.

---

## 📌 Project Overview

Hospital readmissions are costly and often preventable, especially for chronic conditions like diabetes.  
This project builds and evaluates classification models using real clinical data to predict **30-day readmission risk**.

The focus is on **high recall**, prioritizing the identification of at-risk patients over overall accuracy.

---

## 📊 Dataset

- **Source:** Diabetes 130-US Hospitals Dataset (UCI ML Repository)
- **Time Period:** 1999–2008
- **Records:** 101,766 patient encounters
- **Features:** Demographics, diagnoses, medications, lab activity, hospital utilization
- **Target:**  
  - `1` → Readmitted within 30 days  
  - `0` → Not readmitted within 30 days

---

## ⚙️ Models Used

- **Logistic Regression** (class-weighted, scaled features)
- **Random Forest** (hyperparameter tuning, threshold adjustment)

Class imbalance (~11% positive cases) was addressed using **class weighting and recall-focused evaluation**.

---

## 📈 Results (Test Set)

| Model               | Recall (<30) | Precision (<30) | ROC AUC |
|--------------------|--------------|-----------------|---------|
| Logistic Regression| ~0.70        | ~0.15           | ~0.64   |
| Random Forest      | ~0.73        | ~0.15           | ~0.65   |

The **Random Forest model** achieved the highest recall, making it more suitable for healthcare risk screening.

---

## ⭐ Key Insights

- Recall is more important than accuracy in healthcare prediction tasks
- Class imbalance significantly impacts precision
- Feature engineering and threshold tuning greatly improved performance
- Visit history and treatment intensity were strong predictors of readmission

---

## 🛠️ Tools & Technologies

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

---

## 📂 Repository Structure

- Data preprocessing and feature engineering
- Model training and evaluation
- Visualizations and analysis

For detailed methodology and analysis, see the notebooks in this repository.

---

## 👥 Authors

- **Zaina Abdalhaq**
- **Zaina Dawod**

تمام، شغلك واضح إنه **كبير ومرتب** 👌
هذا **README.md كامل واحترافي**، مناسب تمامًا لـ GitHub، ومكتوب بطريقة تعكس قوة المشروع وخطواته بوضوح.
انسخيه كما هو وضعيه في ملف `README.md` داخل الريبو.

---

# 🏥 Predicting 30-Day Hospital Readmission for Diabetic Patients

This project focuses on predicting whether diabetic patients will be readmitted to the hospital within **30 days after discharge**, using machine learning techniques and real clinical data.

The goal is to support healthcare decision-making by identifying **high-risk patients** early and enabling better post-discharge care planning.

---

## 📌 Project Overview

Hospital readmissions place a heavy burden on healthcare systems, especially for patients with chronic diseases such as diabetes. Many readmissions are preventable if high-risk patients are identified early.

In this project, we developed and evaluated machine learning models to predict **30-day readmission risk** for diabetic patients using demographic, clinical, diagnostic, and treatment-related features.

---

## 📊 Dataset

* **Source:** Diabetes 130-US Hospitals Dataset (UCI Machine Learning Repository)
* **Time Period:** 1999 – 2008
* **Records:** 101,766 patient encounters
* **Features:** Demographics, hospital stay details, diagnoses, medications, lab activity
* **Problem Type:** Binary classification

  * `1` → Readmitted within 30 days
  * `0` → Not readmitted within 30 days

---

## ⚙️ Workflow

### 1️⃣ Data Loading & Inspection

* Loaded and inspected the dataset structure and size
* Reviewed feature types and basic statistics
* Examined categorical value distributions and target imbalance

---

### 2️⃣ Data Cleaning

* Dropped identifiers and non-informative columns to reduce overfitting
* Replaced `?` values with missing values
* Removed features with extremely high missing rates
* Handled missing categorical values using domain-appropriate strategies

---

### 3️⃣ Feature Engineering

Key engineered features include:

* **Diagnosis grouping:** ICD-9 codes mapped into clinical categories
* **Age mapping:** Converted age ranges into numeric midpoints
* **Lab intensity:** Lab procedures per day in hospital
* **Medication change count:** Number of medications adjusted per encounter
* **Treatment complexity:** Simplified representation of diabetes treatment
* **Total visits & health index:** Aggregated and normalized patient visit history
* **Binary target:** Converted readmission outcome into `<30` vs others

---

### 4️⃣ Exploratory Data Analysis (EDA)

* Distribution analysis for age, hospital stay, medications, and visits
* Correlation analysis between numerical features and readmission
* Visualization of readmission patterns across:

  * Age groups
  * Gender
  * Admission type
  * Discharge disposition
  * Treatment complexity

---

### 5️⃣ Encoding & Preprocessing

* One-hot encoding for categorical variables
* Feature scaling for numerical features (Logistic Regression)
* Train–test split with stratification to preserve class distribution

---

### 6️⃣ Handling Class Imbalance

* Observed strong class imbalance (~11% positive cases)
* Applied:

  * Class weighting
  * Recall-focused evaluation
  * Threshold tuning

---

### 7️⃣ Model Training

#### 🔹 Logistic Regression

* Scaled numerical features
* Class-weighted training
* Recall-oriented evaluation

#### 🔹 Random Forest

* GridSearchCV for hyperparameter tuning
* Recall used as the main optimization metric
* Threshold adjustment to improve sensitivity

---

### 8️⃣ Model Evaluation

**Metrics Used:**

* Precision
* Recall
* F1-score
* ROC AUC
* Balanced accuracy

**Final Results (Test Set):**

| Model               | Recall (<30) | Precision (<30) | ROC AUC |
| ------------------- | ------------ | --------------- | ------- |
| Logistic Regression | ~0.70        | ~0.15           | ~0.64   |
| Random Forest       | ~0.73        | ~0.15           | ~0.65   |

Random Forest achieved the **highest recall**, making it more suitable for identifying high-risk patients in healthcare settings.

---

## ⭐ Key Insights

* In healthcare problems, **recall is more critical than accuracy**
* Class imbalance significantly affects precision
* Feature engineering and threshold tuning had a major impact on performance
* Visit history and treatment intensity were among the most influential predictors

---

## 🛠️ Tools & Technologies

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn
* Jupyter Notebook

---

## 👥 Team

* **Zina Abdalhaq**
* **Zina Dawod**

---

## 🙏 Acknowledgment

Special thanks to **Eng. Asem Saleh** for his guidance, support, and valuable feedback throughout this project.

---

## 🔗 Repository

This repository contains:

* Full preprocessing pipeline
* Feature engineering steps
* Model training and evaluation
* Visualizations and analysis

---

إذا بدك:

* نسخة أقصر
* نسخة أكثر تقنية
* أو README مناسب للتقديم على internship

قوليلي وبعدّلها فورًا 🌸

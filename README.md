# 🩺 Diabetes Health Indicators — ML Classification Project

## 📌 Objective
The primary goal of this project is to **predict the likelihood of a person having diabetes** based on health-related indicators. This is a **binary classification** task, where the model outputs either:

- `0` → Non-diabetic  
- `1` → Diabetic

This predictive model can assist healthcare professionals in **early diagnosis**, **risk assessment**, and **prioritizing patient care**.

---

## 🧠 Dataset Overview
The dataset contains health-related features such as:

- **BMI** (Body Mass Index)  
- **Physical Activity**  
- **Smoking Status**  
- **High Blood Pressure**  
- **General Health Ratings**  
- **Alcohol Consumption**  
- **Cholesterol**  
- *...and more*

The target variable is:  
`Diabetes_binary` → indicates if the person is diabetic (`1`) or not (`0`).

---

## 🔍 Approach & Workflow

### 1. 🧹 Data Preprocessing
- Handled missing and inconsistent values  
- Normalized features using `StandardScaler`  
- Converted categorical indicators to numeric format where required  

---

### 2. 📊 Visual Exploratory Data Analysis (EDA)
To uncover patterns and feature relevance:
- `countplot` to visualize **class imbalance**
- `heatmap` to analyze **feature correlations**
- `boxplot` and `violinplot` to examine **feature distributions** by diabetes status
- `histogram` to observe **skews in numerical features**

These visualizations helped build a strong foundation for feature selection and model tuning.

---

### 3. 🤖 Model Training & Comparison
Multiple classification algorithms were tested and evaluated using key metrics:

- **Logistic Regression**  
- **Random Forest**  
- **XGBoost Classifier**  
- **Support Vector Machine** *(optional)*  
- **K-Nearest Neighbors** *(optional)*  

#### Metrics used:
- **Confusion Matrix**  
- **Precision**, **Recall**, **F1-score**  
- **ROC AUC Score**

> 🔎 *Our primary aim was to **maximize recall** — reducing false negatives — which is essential in medical predictions.*

Hyperparameter tuning (with `GridSearchCV`) focused on:
- `max_depth`
- `n_estimators`
- `learning_rate`
- `scale_pos_weight` *(to handle class imbalance)*

---

## 🏆 Model Results & Conclusion

- **XGBoost Classifier** achieved the **best performance**:
  - Highest **ROC AUC score**
  - Strong **recall** for diabetic (positive) cases

- It outperformed models like Logistic Regression and Random Forest, which were more prone to **overfitting the majority class**.

- Visualizations played a key role in:
  - Identifying feature relevance
  - Addressing class imbalance effectively

✅ **The final model is optimized for medical relevance** — prioritizing **catching true diabetic cases**, even if it allows a few false positives. In healthcare, this tradeoff can save lives.

---

## 🛠 Tech Stack
- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- Seaborn & Matplotlib  

---

## ✅ Future Improvements
- Add SHAP value analysis for better interpretability  
- Explore deep learning and ensemble stacking  
- Build a simple web UI for real-time predictions  

---





🩺 Diabetes Health Indicators — ML Classification Project



📌 Objective
The primary goal of this project is to predict the likelihood of a person having diabetes based on health-related indicators. This is a binary classification problem, where the model outputs either 0 (no diabetes) or 1 (diabetes).

This type of predictive model can assist healthcare professionals in early diagnosis, risk assessment, and prioritizing patient care.

🧠 Dataset Overview
The dataset contains health-related features like:

BMI (Body Mass Index)

Physical Activity

Smoking status

High Blood Pressure

General Health Ratings

Alcohol Consumption

Cholesterol and more

The target variable is Diabetes_binary — representing whether a person is diabetic or not.

🔍 Approach & Workflow
1. Data Preprocessing
Handled missing and inconsistent values

Normalized/standardized the features using StandardScaler

Converted categorical indicators to numeric where needed

2. Visual Exploratory Data Analysis (EDA)
To understand feature importance and correlation, I used:

countplot to check class imbalance

heatmaps to visualize feature correlations

boxplots and violinplots to explore distributions for each feature grouped by diabetes outcome

histograms to spot skews in numerical features

These visualizations helped uncover patterns and relationships in the data before modeling.

3. Model Training & Comparison
Several classification algorithms were tested and compared using key metrics like accuracy, F1-score, and ROC AUC:

Logistic Regression

Random Forest

XGBoost Classifier

Support Vector Machine (optional)

K-Nearest Neighbors (optional)

Each model was evaluated on:

Confusion Matrix

Precision, Recall, F1-score

ROC AUC Score

Our primary aim being recall which is the most crucial parameter(minimising false negatives).

Focused on parameters like max_depth, n_estimators, learning_rate, and scale_pos_weight (due to class imbalance)

🏆 Model Results & Conclusion
The XGBoost Classifier performed the best overall with the highest ROC AUC score and strong recall on the positive (diabetic) class.

It was better at identifying diabetic individuals compared to Logistic Regression or Random Forest, which slightly overfit to the majority (non-diabetic) class.

Visualizations guided feature relevance and imbalance handling.

The final model is optimized to maximize medical relevance: catching true positives even at the cost of some false positives — which is critical in healthcare applications.

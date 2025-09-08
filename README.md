
# Diabetes Prediction Project

This project demonstrates a complete machine learning workflow to predict whether a patient is diabetic based on diagnostic measurements.

---

## 📊 Phase 1: Exploratory Data Analysis (EDA)

- Visualized the distribution of diabetic vs non-diabetic patients.
- Explored relationships between glucose levels, BMI, and diabetes outcome.
- Used bar charts, box plots, and scatter plots to uncover patterns.

### Example Insights:
- Diabetic patients tend to have higher glucose and BMI.
- Outcome distribution: ~65% non-diabetic, ~35% diabetic.

---

## 🧹 Phase 2: Data Preparation

- Standardized features using `StandardScaler` to ensure consistent scale.
- Split dataset into training (80%) and testing (20%) sets using `train_test_split`.

### Why Standardize?
Standardization improves model performance and convergence, especially for algorithms like Logistic Regression and SVM.

---

## 🤖 Phase 3: Model Training and Evaluation

Implemented and compared two models:

### 1. Logistic Regression
- Tuned using `GridSearchCV`.
- Best parameter: `C = 10`

### 2. Random Forest
- Tuned using `GridSearchCV`.
- Best parameters: `n_estimators = 50`, `max_depth = None`

### Evaluation Metrics:
- Accuracy, Precision, Recall
- Confusion Matrix

### Results:
- Logistic Regression: Accuracy ~75%, Precision ~65%, Recall ~67%
- Random Forest: Accuracy ~71%, Precision ~59%, Recall ~64%

---

## 🚀 Phase 4: Prediction Engine

Built a prediction function that:
- Accepts new patient data as input.
- Returns prediction: "Diabetic" or "Non-Diabetic".

### Example Usage:
```python
new_patient = [2, 120, 70, 30, 100, 32.5, 0.5, 25]
predict_diabetes(new_patient)  # Output: 'Diabetic' or 'Non-Diabetic'
```

---

## 📁 File
- `diabetes.csv`: Dataset used for training and evaluation.

---

## 🛠 Technologies Used
- Python
- Pandas, Scikit-learn
- Matplotlib, Seaborn


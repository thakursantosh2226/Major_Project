# Major_Project
Machine Learning Model For Early Detection and  Prevention of Heart Blockage 
# ❤️ Heart Disease Prediction System using Machine Learning

> A complete Machine Learning based Heart Disease Prediction System built using Python, Scikit-Learn and Streamlit.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-green)
![Streamlit](https://img.shields.io/badge/Frontend-Streamlit-red)
![Scikit Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)

---

# 📌 Project Overview

Heart disease is one of the leading causes of death worldwide. Early diagnosis can significantly reduce the risk by helping doctors take preventive actions.

This project develops a Machine Learning-based Heart Disease Prediction System that predicts whether a patient is likely to have heart disease based on various medical parameters.

The project includes:

- Data preprocessing
- Data visualization
- Feature engineering
- Training multiple ML models
- Comparing model performances
- Saving trained models
- Interactive Streamlit Web Application
- Single Prediction
- Batch Prediction using CSV upload
- Prediction CSV Download

---

# 🎯 Aim of the Project

The primary objective of this project is:

- To predict heart disease using Machine Learning.
- To compare different classification algorithms.
- To identify the best-performing model.
- To provide an easy-to-use web application for prediction.
- To reduce diagnosis time through automated prediction.

---

# 🏥 Problem Statement

Heart disease diagnosis requires expert medical analysis and several clinical tests.

This project aims to assist healthcare professionals by providing an AI-based prediction system that estimates the possibility of heart disease using patient health records.

**Note:** This system is intended to support medical decision-making and should not replace professional medical diagnosis.

---

# 🧠 Machine Learning Workflow

```
Medical Dataset
       │
       ▼
Data Cleaning
       │
       ▼
Data Preprocessing
       │
       ▼
Exploratory Data Analysis
       │
       ▼
Feature Engineering
       │
       ▼
Train-Test Split
       │
       ▼
Model Training
       │
       ▼
Model Evaluation
       │
       ▼
Best Model Selection
       │
       ▼
Model Serialization (.pkl)
       │
       ▼
Streamlit Web Application
       │
       ▼
Heart Disease Prediction
```

---

# 📂 Project Structure

```
Heart-Disease-Prediction/
│
├── app.py                     # Streamlit Application
├── MAJOR_PROJECT.ipynb        # Complete ML Development Notebook
├── heart.csv                  # Dataset
│
├── LogisticR.pkl              # Logistic Regression Model
├── SVM.pkl                    # Support Vector Machine Model
├── Tree.pkl                   # Decision Tree Model
├── RandomForest.pkl           # Random Forest Model
│
├── README.md
└── requirements.txt
```

---

# 📊 Dataset Information

The dataset contains patient medical records.

## Features

| Feature | Description |
|----------|-------------|
| Age | Age of patient |
| Sex | Gender |
| ChestPainType | Type of chest pain |
| RestingBP | Resting Blood Pressure |
| Cholesterol | Cholesterol Level |
| FastingBS | Fasting Blood Sugar |
| RestingECG | ECG Results |
| MaxHR | Maximum Heart Rate |
| ExerciseAngina | Exercise-induced Angina |
| Oldpeak | ST Depression |
| ST_Slope | Slope of ST Segment |
| HeartDisease | Target Variable |

Target:

- 0 → No Heart Disease
- 1 → Heart Disease

---

# ⚙️ Data Preprocessing

The dataset was carefully preprocessed before training.

The preprocessing steps include:

### ✔ Missing Value Checking

Verified that the dataset contains no missing values.

---

### ✔ Duplicate Removal

Duplicate records were identified and checked.

---

### ✔ Categorical Encoding

Categorical variables were converted into numerical values.

Examples:

Sex

- Male → 0
- Female → 1

ExerciseAngina

- No → 0
- Yes → 1

ChestPainType

- ATA
- NAP
- ASY
- TA

were converted into numeric labels.

---

### ✔ Handling Invalid Values

Some patients had:

```
Cholesterol = 0
RestingBP = 0
```

which are medically impossible.

Instead of deleting those records, KNN Imputation was used to estimate realistic values based on neighboring samples.

This improves prediction quality.

---

### ✔ Data Type Conversion

Necessary columns were converted into integer datatype before model training.

---

# 📈 Exploratory Data Analysis (EDA)

Several visualizations were created to understand the dataset.

They include:

- Age Distribution
- Heart Disease Distribution
- Gender vs Heart Disease
- Chest Pain Type Analysis
- Resting Blood Pressure Analysis
- Cholesterol Analysis
- Maximum Heart Rate Analysis
- Exercise Angina Analysis
- ST Slope Analysis
- Oldpeak Analysis

These visualizations help identify important relationships between features and heart disease.

---

# 🤖 Machine Learning Models Used

Four classification algorithms were trained.

## 1. Logistic Regression

A linear classification algorithm used as the baseline model.

Advantages:

- Fast
- Easy to interpret
- Works well for binary classification

---

## 2. Support Vector Machine (SVM)

Creates an optimal decision boundary to separate classes.

Advantages:

- High accuracy
- Effective in high-dimensional datasets

---

## 3. Decision Tree

Uses tree-like decision rules.

Advantages:

- Easy to visualize
- Handles nonlinear relationships

---

## 4. Random Forest

An ensemble of multiple decision trees.

Advantages:

- Higher accuracy
- Reduces overfitting
- Better generalization

---

# 📊 Model Evaluation

The trained models were evaluated using standard classification metrics such as:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

A comparative analysis was performed to determine the best-performing algorithm.

---

# 💻 Streamlit Web Application

A user-friendly Streamlit application was developed.

Features include:

### Single Prediction

Users can manually enter patient details and instantly receive predictions.

---

### Batch Prediction

Users can upload a CSV file containing multiple patient records.

The application predicts heart disease for all records simultaneously.

---

### Download Predictions

After prediction, users can download the results as a CSV file.

---

# 🚀 How to Run the Project

## Step 1

Clone the repository

```bash
git clone https://github.com/yourusername/Heart-Disease-Prediction.git
```

---

## Step 2

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Step 3

Run the application

```bash
streamlit run app.py
```

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Streamlit
- Pickle

---

# 📚 Libraries Used

```python
numpy
pandas
matplotlib
seaborn
streamlit
scikit-learn
pickle
base64
```

---

# 🔍 Project Highlights

✔ Complete Machine Learning Pipeline

✔ Data Cleaning

✔ Feature Engineering

✔ KNN Imputation

✔ Data Visualization

✔ Multiple ML Algorithms

✔ Model Comparison

✔ Interactive Streamlit Dashboard

✔ Batch Prediction

✔ CSV Export

✔ Beginner Friendly

---

# 📖 Interview Explanation

If asked:

**"Explain your project."**

You can answer:

> This project predicts the likelihood of heart disease using Machine Learning. First, I collected and cleaned the dataset by removing inconsistencies and replacing medically invalid values using KNN Imputation. Then I performed exploratory data analysis to understand feature relationships. I trained four classification algorithms—Logistic Regression, Support Vector Machine, Decision Tree, and Random Forest—and compared their performance using evaluation metrics like Accuracy, Precision, Recall, and F1 Score. After selecting the best-performing model, I deployed it using Streamlit. The application supports both single-patient prediction and batch prediction through CSV upload, and users can download prediction results directly.

---

# 🎓 Learning Outcomes

Through this project I learned:

- Data preprocessing
- Feature engineering
- Machine Learning workflow
- Classification algorithms
- Model comparison
- Model serialization
- Streamlit deployment
- Building complete end-to-end ML applications

---

# 🔮 Future Enhancements

- Integration with hospital databases
- Deep Learning models
- Cloud deployment
- Explainable AI (SHAP/LIME)
- User authentication
- Patient history management
- Doctor dashboard
- REST API support
- Real-time prediction service

---

# 👨‍💻 Author

**Raja**

Bachelor of Technology (B.Tech)

Machine Learning Major Project

---

# ⭐ If you found this project useful

Please consider giving this repository a ⭐ on GitHub!

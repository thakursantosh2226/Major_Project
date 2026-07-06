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

To determine the most suitable algorithm for heart disease prediction, four supervised Machine Learning classification models were trained and evaluated. Each model has its own strengths and limitations, so comparing multiple algorithms helped identify the one that performs best on this dataset.

The dataset was divided into **training** and **testing** sets. After preprocessing and feature engineering, each model was trained using the training data and evaluated on unseen testing data using standard classification metrics.

The following evaluation metrics were used:

- **Accuracy** – Overall percentage of correctly classified patients.
- **Precision** – Measures how many patients predicted as having heart disease actually have the disease.
- **Recall (Sensitivity)** – Measures how many actual heart disease patients are correctly identified.
- **F1-Score** – Harmonic mean of Precision and Recall; useful when balancing false positives and false negatives.
- **Matthews Correlation Coefficient (MCC)** – A robust evaluation metric for binary classification that considers all four outcomes (TP, TN, FP, FN). It is especially useful for evaluating medical prediction models.

---

## 1️⃣ Logistic Regression

**Overview**

Logistic Regression is one of the most popular algorithms for binary classification problems. It predicts the probability of a patient belonging to either the "Heart Disease" or "No Heart Disease" class using the logistic (sigmoid) function.

### Why it was used

- Fast and computationally efficient
- Easy to interpret
- Works well on structured medical datasets
- Provides a strong baseline for comparison

### Advantages

- Simple implementation
- Less prone to overfitting
- Easy to explain during interviews
- Performs well when classes are linearly separable

### Limitations

- Cannot capture highly complex nonlinear relationships
- Performance depends on feature relationships

### Project Performance

- **Accuracy:** **85.87%**
- Achieved the **highest accuracy** among all tested models.
- Also showed the best balance between Precision, Recall, and F1-Score, making it the most reliable model for this dataset.

**Final Status:** ✅ **Selected as the Best Performing Model**

---

## 2️⃣ Support Vector Machine (SVM)

**Overview**

Support Vector Machine classifies data by finding the optimal hyperplane that maximizes the separation (margin) between different classes.

### Why it was used

- Excellent classifier for medium-sized datasets
- Handles high-dimensional data effectively
- Often provides high classification accuracy

### Advantages

- Works well with complex decision boundaries
- Robust against overfitting
- Effective in binary classification tasks

### Limitations

- Computationally expensive for larger datasets
- Requires careful parameter tuning
- Less interpretable than Logistic Regression

### Project Performance

- Produced competitive prediction results.
- Performed well across all evaluation metrics but remained slightly behind Logistic Regression.
- Demonstrated good generalization capability.

**Final Status:** ✔ Strong Alternative Model

---

## 3️⃣ Decision Tree

**Overview**

Decision Tree builds a flowchart-like tree structure where each node represents a decision based on a feature, eventually leading to a prediction.

### Why it was used

- Easy to visualize
- Easy to explain to non-technical users
- Captures nonlinear relationships

### Advantages

- Highly interpretable
- Requires little data preprocessing
- Can model complex feature interactions

### Limitations

- Prone to overfitting
- Small data changes can produce different trees
- Lower generalization compared to ensemble models

### Project Performance

- **Accuracy:** **80.98%**
- Produced the lowest overall accuracy among the tested models.
- Although easy to interpret, it was less effective than the other algorithms.

**Final Status:** Suitable for understanding decision logic but not selected for deployment.

---

## 4️⃣ Random Forest

**Overview**

Random Forest is an ensemble learning algorithm that combines the predictions of multiple Decision Trees to improve overall performance and reduce overfitting.

### Why it was used

- Handles nonlinear relationships effectively
- More robust than a single Decision Tree
- Produces stable predictions

### Advantages

- High prediction accuracy
- Resistant to overfitting
- Works well with real-world datasets
- Handles feature interactions automatically

### Limitations

- Larger model size
- Higher computational cost
- Less interpretable than Logistic Regression

### Project Performance

- **Accuracy:** **84.24%**
- Improved significantly over the Decision Tree.
- Delivered strong Precision, Recall, and F1-Score.
- Performed consistently but slightly below Logistic Regression.

**Final Status:** ✔ Second Best Performing Model

---

# 📊 Model Comparison

| Model | Accuracy | Overall Performance |
|-------|---------:|---------------------|
| **Logistic Regression** | **85.87%** | 🥇 Best |
| Random Forest | 84.24% | 🥈 Second Best |
| Support Vector Machine | Comparable to Random Forest | 🥉 Good |
| Decision Tree | 80.98% | Fourth |

---

# 🏆 Why Logistic Regression Was Selected

Although all four algorithms were capable of predicting heart disease, **Logistic Regression** achieved the best overall balance across the evaluation metrics.

It was selected because it:

- ✅ Achieved the **highest testing accuracy (85.87%)**
- ✅ Maintained a strong balance between **Precision**, **Recall**, and **F1-Score**
- ✅ Produced reliable predictions without overfitting
- ✅ Is computationally efficient and fast during inference
- ✅ Is highly interpretable, making it suitable for medical decision-support applications
- ✅ Generates probability scores that help explain prediction confidence

For these reasons, Logistic Regression was chosen as the **final deployment model** for the Streamlit web application, while the other trained models were retained for performance comparison and future experimentation.



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

**Santosh Kumar and Others**

Bachelor of Technology (B.Tech)

Machine Learning Major Project

---

# ⭐ If you found this project useful

Please consider giving this repository a ⭐ on GitHub!

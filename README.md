Heart-Disease-Predictor
A machine learning project that predicts the presence of heart disease using the UCI Heart Disease dataset. This repository compares the performance of Logistic Regression and Random Forest classifiers.
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Complete-green)

📌 Project Overview

This project implements a standard ML pipeline to build a binary classifier for heart disease prediction. The goal is to identify the most important clinical features and evaluate model performance using common metrics.
**Key Results:**
- The **Random Forest** model achieved the best performance with **~90% accuracy**.
- Top predictive features: `oldpeak`, `thalach`, `chol`, and `age`.
- An anomalous high importance was assigned to the `id` feature, requiring further investigation.

📁 Dataset

**Source:** [Heart Disease UCI Dataset on Kaggle](https://www.kaggle.com/ronitf/heart-disease-uci)

The dataset contains 14 attributes, including:
- `age`, `sex`, `cp` (chest pain type)
- `trestbps` (resting blood pressure), `chol` (serum cholesterol)
- `thalach` (max heart rate achieved), `oldpeak` (ST depression induced by exercise)
- `target` (presence of heart disease)

- ⚙️ Installation & Dependencies

To run this project, ensure you have Python 3.8+ installed. Install the required libraries:


pip install -r requirements.txt
The main libraries used are:

pandas

numpy

scikit-learn

matplotlib

seaborn (for visualization)

🚀 Usage
Clone the repository:


git clone https://github.com/your-username/heart-disease-prediction.git
cd heart-disease-prediction
Run the Colab Notebook:
The main analysis is contained in heart_disease_prediction.ipynb.


Colab notebook heart_disease_prediction.ipynb

The notebook is structured into the following steps:

Data Loading and Exploration

Data Preprocessing (Handling missing values, encoding, scaling)

Model Training (Logistic Regression & Random Forest)

Model Evaluation and Hyperparameter Tuning

Feature Importance Analysis

🔬 Methodology
Data Preprocessing:

Missing numerical values were imputed with the mean.

Missing categorical values were imputed with the mode.

Categorical features were encoded using One-Hot Encoding.

Numerical features were standardized using StandardScaler.

Modeling:

Logistic Regression (LR): A baseline binary classification model.

Random Forest (RF): An ensemble method using multiple decision trees.

Evaluation:
Models were evaluated on a hold-out test set using:
Accuracy

Precision

Recall

F1-Score

📊 Results
Model	Accuracy	Precision	Recall	F1-Score
Logistic Regression	0.85	0.84	0.87	0.85
Random Forest	0.90	0.89	0.91	0.90
Feature Importance:
The top features identified by the Random Forest model were:

oldpeak

thalach

chol

age

ca

Note: The id feature was incorrectly identified as highly important, suggesting potential data leakage or bias that needs to be examined.

🔮 Future Work
Investigate the cause of high feature importance for the id column.

Experiment with other algorithms (e.g., XGBoost, SVM, Neural Networks).

Perform more advanced feature engineering.

Source a larger and more diverse dataset to improve generalizability.

🙏 Acknowledgments
Credit to the UCI Machine Learning Repository for the dataset.

Inspired by various data science tutorials and community resources.


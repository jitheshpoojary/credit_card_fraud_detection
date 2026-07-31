# 💳 Credit Card Fraud Detection using Machine Learning

An end-to-end **Credit Card Fraud Detection** project that identifies fraudulent transactions using machine learning. The project follows a production-oriented workflow, including data preprocessing, feature engineering, handling class imbalance, hyperparameter tuning, threshold optimization, and comprehensive model evaluation.

The objective is to accurately detect fraudulent transactions while minimizing false positives and false negatives in a highly imbalanced dataset.

---

## 📌 Project Overview

Fraud detection is a critical application in the financial industry where fraudulent transactions represent only a tiny fraction of all transactions. Traditional machine learning models often struggle with such imbalanced data.

This project addresses these challenges by:

- Performing extensive Exploratory Data Analysis (EDA)
- Engineering informative transaction features
- Preventing data leakage throughout the pipeline
- Handling class imbalance using proper resampling techniques
- Comparing multiple gradient boosting algorithms
- Optimizing the classification threshold for business requirements
- Selecting the best-performing model based on multiple evaluation metrics

---

## 📊 Dataset

The dataset contains credit card transaction records with both legitimate and fraudulent transactions.

**Target Variable**

- **0** → Legitimate Transaction
- **1** → Fraudulent Transaction

---

## 🚀 Workflow

### 1. Data Preprocessing

- Missing value analysis
- Duplicate removal
- Data type optimization
- Outlier analysis
- Feature scaling
- Encoding categorical variables

---

### 2. Exploratory Data Analysis (EDA)

Performed detailed analysis on:

- Fraud vs Non-Fraud distribution
- Transaction amount distribution
- Fraud by transaction category
- Fraud by hour of day
- Fraud by weekday
- Customer demographics
- Merchant analysis
- Correlation analysis
- Feature relationships

---

### 3. Feature Engineering

Engineered several meaningful features including:

- Transaction frequency
- Customer age
- Business hours indicator
- Weekend indicator
- Night transaction flag
- Cyclic hour encoding
- Cyclic weekday encoding
- Category average amount
- Category amount standard deviation
- Category amount z-score
- Log-transformed city population

---

### 4. Handling Imbalanced Data

The dataset is highly imbalanced.

To prevent data leakage:

- SMOTE-Tomek was applied **only to the training folds**
- Stratified Cross Validation was used throughout model training

---

### 5. Models Compared

- CatBoost
- LightGBM
- XGBoost

Each model was independently:

- Hyperparameter tuned using Optuna
- Cross validated
- Evaluated using identical metrics

---

## 🏆 Final Model

**CatBoost Classifier**

Reason for selection:

- Excellent balance between Precision and Recall
- Strong F1 Score
- High ROC-AUC
- High PR-AUC
- Stable cross-validation performance
- Better fraud detection capability after threshold optimization

---

## 📈 Model Evaluation

Evaluation metrics include:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- PR-AUC
- Confusion Matrix
- Classification Report
- Precision-Recall Curve
- ROC Curve
- Threshold Comparison

---

## ⚙️ Hyperparameter Optimization

Hyperparameters were optimized using:

- **Optuna**
- Stratified Cross Validation
- Early Stopping
- Balanced Class Weights

---

## 📉 Threshold Optimization

Instead of using the default **0.50** threshold, multiple thresholds were evaluated to achieve the best trade-off between:

- Precision
- Recall
- F1 Score

This helps tailor the fraud detection system to real-world business requirements.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- CatBoost
- LightGBM
- XGBoost
- Optuna
- Imbalanced-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 📌 Key Highlights

- End-to-end Machine Learning pipeline
- Extensive Exploratory Data Analysis
- Advanced Feature Engineering
- Leakage-free training pipeline
- Proper handling of class imbalance
- Hyperparameter tuning with Optuna
- Threshold optimization
- Comprehensive model comparison
- Production-oriented workflow

---

## 📚 Future Improvements

- Deploy the model using Streamlit or FastAPI
- Real-time fraud detection pipeline
- Explainable AI using SHAP values
- Automated model retraining
- Model monitoring and drift detection

---

## 👨‍💻 Author

**Jithesh**

Aspiring Data Scientist passionate about Machine Learning, Deep Learning, NLP, and solving real-world problems using AI.

- LinkedIn: *Add your LinkedIn profile*
- GitHub: *Add your GitHub profile*

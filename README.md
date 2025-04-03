# 🧬 Breast Cancer Diagnosis with Logistic Regression

This project focuses on diagnosing breast cancer using machine learning models, specifically logistic regression, based on cell nuclei features extracted from digitized images of breast tissue samples. It utilizes the Breast Cancer Wisconsin Diagnostic dataset and compares logistic regression against Random Forest and Support Vector Machine classifiers.

# 📊 Dataset Overview

- Source: UCI Machine Learning Repository
- Samples: 569
- Features: 30 numeric features describing characteristics of cell nuclei in digitized images
- Target variable: diagnosis:
    - M (Malignant) → 1
    - B (Benign) → 0
 
# ⚙️ How It Works

1. Data Preprocessing:
   - Dropped unnecessary columns (id, Unnamed: 32)
   - Encoded diagnosis to binary: 1 for Malignant, 0 for Benign
   - Scaled features using StandardScaler for improved model performance

2. Model Training
   - Performed an 80/20 train-test split
   - Trained a logistic regression model
   - Saved the trained model and scaler using pickle

3. Evaluation Metrics
   - Accuracy score
   - Classification report
   - Confusion matrix

# ✅ Results & Interpretation

1. Logistic Regression

Accuracy: ~96%

Precision (malignant): 0.95

Recall (malignant): 0.96 → Performs excellently as a linear model and serves well as a baseline.

2. Random Forest Classifier

Accuracy: ~95% → Slightly better handling of non-linear relationships, but similar overall accuracy.

3. Support Vector Machine (SVM)

Accuracy: ~95% → Excellent boundary detection; slightly more computationally intensive.

4. Confusion Matrix Insights:

Very low false negatives, which is critical in medical diagnosis. High true positive rate ensures malignant tumors are correctly flagged


# 💡 Key Findings

Logistic Regression, though simple, achieved excellent performance — proving effective for structured, well-preprocessed datasets.

Random Forest and SVM had similar or slightly better accuracy but added complexity.

Feature scaling was essential to achieve consistent results across classifiers.

False negatives were minimal, highlighting the model's clinical value in identifying dangerous cases early.



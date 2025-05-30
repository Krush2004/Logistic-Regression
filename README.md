# 🧪 Breast Cancer Detection with Logistic Regression

This project demonstrates a binary classification task using **Logistic Regression** to predict whether a tumor is **malignant** or **benign** based on the **Breast Cancer Wisconsin Diagnostic Dataset**.

---

## 🎯 Objective

- Build a binary classifier using **Logistic Regression**
- Evaluate using metrics such as:
  - Confusion Matrix
  - Precision, Recall, F1-Score
  - ROC Curve and AUC
- Understand the role of the **sigmoid function** and **threshold tuning**

---

## 🛠️ Tools & Libraries

- Python
- pandas
- scikit-learn
- matplotlib
- numpy

---

## 📁 Dataset

- **Source**: Breast Cancer Wisconsin (Diagnostic) Data Set
- **Features**: 30 real-valued features computed from digitized images of a breast mass
- **Target**: `diagnosis` — Malignant (M) or Benign (B)

---

## 🚀 How It Works

1. **Load and clean the data**
   - Drop `id` and null column `Unnamed: 32`
   - Encode `diagnosis`: M → 1, B → 0

2. **Split the dataset**
   - 80% training, 20% testing

3. **Standardize features**
   - Using `StandardScaler`

4. **Train the Logistic Regression model**

5. **Evaluate performance**
   - Confusion matrix, classification report
   - ROC-AUC score and ROC curve

6. **Tune prediction threshold**
   - Adjust default 0.5 threshold to observe changes

7. **Visualize sigmoid function**

---

## 📊 Evaluation Metrics

- **Confusion Matrix**
- **Precision / Recall / F1-Score**
- **ROC-AUC Score**
- **Custom Threshold Classification**

---

## 📈 Sigmoid Function

Logistic regression uses the **sigmoid function** to output probabilities between 0 and 1:

\[
\sigma(z) = \frac{1}{1 + e^{-z}}
\]

A threshold (commonly 0.5) is applied to convert probabilities into class predictions.

---

## 📌 Example Output

```bash
Confusion Matrix:
[[71  1]
 [ 2 40]]

Classification Report:
              precision    recall  f1-score   support

           0       0.97      0.99      0.98        72
           1       0.98      0.95      0.96        42

    accuracy                           0.97       114
   macro avg       0.97      0.97      0.97       114
weighted avg       0.97      0.97      0.97       114

ROC-AUC Score: 0.99

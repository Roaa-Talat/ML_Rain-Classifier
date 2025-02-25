# Machine Learning Rain Prediction Model

---

## 📖 Project Overview
This project focuses on analyzing a weather dataset to predict the likelihood of rain using machine learning models. The dataset contains key weather features and a binary target variable (`rain` or `no rain`).

### 🎯 Objectives:
- Load and explore the dataset.
- Handle missing values using different techniques.
- Analyze data distributions and feature scaling.
- Train and evaluate multiple classification models:
  - **Decision Tree**
  - **k-Nearest Neighbors (kNN)** (both built-in and custom implementation)
  - **Naïve Bayes**
- Compare model performance using evaluation metrics.

---

## 📊 Dataset Overview
### 🔍 1. Dataset Details
✔ 2,500 rows, 6 columns covering various weather conditions.
✔ **Features:** Temperature, Humidity, Wind Speed, Cloud Cover, Pressure.
✔ **Target Variable:** Rain (binary classification: 0 = no rain, 1 = rain).

### 🔍 2. Missing Values Analysis
- The dataset contains missing values:
  - **Temperature:** 25 missing
  - **Humidity:** 40 missing
  - **Wind Speed:** 32 missing
  - **Cloud Cover:** 33 missing
  - **Pressure:** 27 missing
  - **Rain:** No missing values

---

## 🛠 Data Preprocessing
### ✅ Steps:

1️⃣ **Handling Missing Values**
   - Method 1: Replace missing values with the feature mean.
   - Method 2: Drop rows containing missing values.

2️⃣ **Feature Scaling**
   - Applied **Standardization (Z-score normalization)** after splitting data to avoid data leakage.
   
3️⃣ **Data Splitting**
   - **80% Training** / **20% Testing** using `train_test_split` from Scikit-learn.
   
4️⃣ **Encoding Target Variable**
   - Converted categorical values (`rain`/`no rain`) into binary numeric values (0 or 1).

---

## 🤖 Machine Learning Models
### 📌 1. **Decision Tree Classifier**
✔ Optimized splitting using **Entropy and Information Gain**.
✔ Evaluated on different missing value handling techniques.
✔ Model correctly classified **99% of 'No Rain' cases**, but struggled with **'Rain' cases**.

### 📌 2. **k-Nearest Neighbors (kNN)**
✔ Implemented both **built-in Scikit-learn kNN** and **custom kNN from scratch**.
✔ kNN performed well but suffered from false negatives for predicting rain.
✔ Best performance was achieved with **k = 11**.

### 📌 3. **Naïve Bayes Classifier**
✔ Handled binary classification efficiently.
✔ Accuracy remained **96%**, but recall for `Rain` was lower.
✔ Model struggled with **class imbalance**, misclassifying some rain instances.

---

## 📊 Model Performance Comparison
| Metric         | Decision Tree | kNN (k=11) | Naïve Bayes |
|---------------|--------------|------------|-------------|
| **Accuracy**  | 100%         | 97%        | 96%         |
| **Precision (Rain)** | 1.00 | 0.92 | 1.00 |
| **Recall (Rain)** | 0.96 | 0.79 | 0.68 |
| **F1-Score (Rain)** | 0.98 | 0.85 | 0.81 |
| **False Positives** | 0 | 4 | 0 |
| **False Negatives** | 2 | 12 | 18 |

---

## 🚀 Key Takeaways
✅ Decision Tree provided the highest accuracy but overfitted slightly.

✅ kNN performed well, but optimal **k-value selection is crucial**.

✅ Naïve Bayes worked well but suffered from class imbalance.

✅ Handling missing data impacts final model performance significantly.

---

## 🛠 Technologies & Libraries Used
🔹 **Python**

🔹 **Pandas, NumPy** (Data manipulation)

🔹 **Matplotlib, Seaborn** (Data visualization)

🔹 **Scikit-learn** (ML models & evaluation)

---

## 🔮 Future Enhancements
🔹 Implement **Random Forest** to improve decision tree generalization.

🔹 Balance the dataset using **oversampling techniques**.

🔹 Experiment with **deep learning models** for improved accuracy.


# 🚨 Online Scam Message Detection using Machine Learning

## Overview

Online scams such as phishing attacks, UPI fraud, fake job offers, OTP scams, lottery scams, and banking fraud messages have become increasingly common. Detecting these fraudulent messages manually is difficult due to their growing volume and evolving language patterns.

This project develops a Machine Learning-based scam message detection system that automatically classifies text messages as:

* **Scam (1) 🚨**
* **Not Scam (0) ✅**

The system uses Natural Language Processing (NLP) techniques and compares multiple machine learning models to identify the most effective approach for scam detection.

---

# Problem Statement

Fraudulent messages often imitate legitimate communication from banks, government agencies, delivery services, and employers.

The objective of this project is to:

* Automatically identify scam messages
* Reduce the risk of financial fraud
* Compare different machine learning algorithms
* Enable real-time scam prediction on unseen messages

---

# Dataset

The project combines two datasets:

### Dataset 1

* Honeypot-generated scam and legitimate messages
* Approximately 10,751 records

### Dataset 2

* Processed SMS dataset
* Approximately 5,971 records

### Combined Dataset

| Metric              | Value   |
| ------------------- | ------- |
| Total Messages      | ~16,722 |
| Scam Messages       | ~6,138  |
| Legitimate Messages | ~10,584 |

The combined dataset provides a diverse collection of real-world and synthetic scam scenarios.

---

# Data Preprocessing

Several preprocessing steps were performed before model training:

### Text Cleaning

* Converted text to lowercase
* Removed numbers
* Removed punctuation
* Removed extra whitespace

### Example

Input:

```text
Refund of Rs 7500 is ready. Share your UPI PIN to receive it.
```

Output:

```text
refund of rs is ready share your upi pin to receive it
```

---

# Feature Engineering

Text data was transformed using **TF-IDF Vectorization**.

### Configuration

* Maximum Features: 5000
* N-gram Range: (1,3)
* Minimum Document Frequency: 2
* Maximum Document Frequency: 0.95
* English Stopwords Removed

Using trigrams enables the model to capture contextual scam phrases such as:

* "share your otp"
* "verify your kyc"
* "claim your reward"
* "update bank account"

---

# Machine Learning Models

Three supervised learning models were trained and evaluated.

### 1. Multinomial Naive Bayes

A lightweight probabilistic classifier commonly used in text classification.

### 2. Logistic Regression

A strong linear baseline model for binary classification tasks.

### 3. Support Vector Machine (Linear SVC)

The final selected model due to its superior performance on high-dimensional text features.

Class weighting was applied to improve robustness.

---

# Model Performance

## Naive Bayes

| Metric   | Value  |
| -------- | ------ |
| Accuracy | 98.33% |

---

## Logistic Regression

| Metric   | Value  |
| -------- | ------ |
| Accuracy | 98.15% |

---

## Support Vector Machine (Best Model)

| Metric   | Value  |
| -------- | ------ |
| Accuracy | 98.36% |

### Classification Report (SVM)

| Class    | Precision | Recall | F1-Score |
| -------- | --------- | ------ | -------- |
| Not Scam | 0.98      | 0.99   | 0.99     |
| Scam     | 0.98      | 0.97   | 0.98     |

The SVM model achieved the highest overall accuracy and maintained strong precision and recall across both classes.

---

# Project Pipeline

Data Collection
↓
Data Cleaning
↓
Train-Test Split
↓
TF-IDF Vectorization
↓
Model Training
↓
Model Evaluation
↓
Real-Time Scam Prediction

---

# Example Prediction

Input:

```text
share your otp
```

Output:

```text
SCAM 🚨
```

Input:

```text
your salary has been credited successfully
```

Output:

```text
NOT SCAM ✅
```

---

# Scam Categories Detected

The model successfully learns patterns associated with:

* UPI Fraud
* OTP Scams
* Bank KYC Frauds
* Fake Job Offers
* Lottery Scams
* Reward Scams
* Account Verification Frauds
* Payment Request Scams

---

# Technologies Used

* Python
* Scikit-Learn
* Pandas
* NumPy
* TF-IDF Vectorization
* Matplotlib
* Seaborn
* Google Colab

---

# Key Learnings

This project provided practical experience in:

* Natural Language Processing
* Text Classification
* Feature Engineering
* TF-IDF Vectorization
* Machine Learning Model Comparison
* Model Evaluation
* Precision, Recall and F1-Score Analysis
* Real-World Fraud Detection Applications

---

# Future Improvements

Potential enhancements include:

* Fine-tuning transformer models such as BERT
* Multilingual scam detection
* Real-time SMS monitoring system
* Explainable AI for prediction interpretation
* Deployment as a web or mobile application
* Integration with spam filtering systems

---

# Conclusion

This project demonstrates that machine learning can effectively identify fraudulent messages with high accuracy. By leveraging TF-IDF features and Support Vector Machines, the system achieves over 98% accuracy while successfully detecting a wide range of common scam patterns.

The solution highlights the potential of NLP and machine learning in building intelligent fraud prevention systems for real-world applications.

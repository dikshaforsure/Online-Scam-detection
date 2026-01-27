# Online Scam Message Detection using Machine Learning

Online scams such as phishing, UPI fraud, fake job offers, and bank-related fraud messages are increasing rapidly.
This project aims to automatically detect scam messages using Natural Language Processing (NLP) and Machine Learning techniques.
A custom manually annotated dataset is used to train multiple ML models that classify messages as:
1 → Scam 🚨
0 → Not Scam ✅

🎯 Objectives

Build an end-to-end text classification pipeline
Detect scam vs non-scam messages with high accuracy
Compare performance of multiple ML models
Enable real-time prediction on unseen messages

🧠 Machine Learning Models Used

Naive Bayes
Logistic Regression
Support Vector Machine (SVM)
Among these, SVM performs best for text-based scam detection.

🗂️ Dataset Description

Custom dataset created manually
Real-world style scam and non-scam messages
Columns:
text → message content
scam → target label (1 = scam, 0 = not scam)
✔️ Manually annotated for supervised learning

⚙️ Tech Stack
Python 3
Google Colab
Scikit-learn
Pandas & NumPy
TF-IDF Vectorization
Matplotlib / Seaborn

🔄 Project Pipeline
Data Loading
Text Cleaning & Preprocessing
Train-Test Split
TF-IDF Feature Extraction
Model Training
Model Evaluation
Scam / Not-Scam Prediction

📊 Results
TF-IDF with bigrams improves classification performance
SVM achieves the highest accuracy among tested models
Effective in detecting common scam patterns like:
Bank KYC fraud
Fake job offers
OTP / UPI scams
Lottery & reward frauds

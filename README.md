# 📧 Email Spam Classifier

## 🚀 Overview
This project implements a machine learning–based email spam classifier that automatically categorizes emails as **Spam** or **Ham (Not Spam)** using Natural Language Processing (NLP) techniques.

This project demonstrates an end-to-end machine learning workflow including data preprocessing, feature extraction, model training, evaluation, and prediction.

---

## 🧩 Problem Statement
Spam emails are a major productivity and security concern. This project aims to build an automated system that accurately classifies emails based on their textual content.

---

## 📊 Dataset
- Labeled email messages:
  - `ham` – legitimate emails
  - `spam` – unwanted emails
- Columns:
  - `Category`
  - `Message`

---

## 🛠️ Tech Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- TF-IDF Vectorizer
- Jupyter Notebook

---

## 🔄 Workflow

### 1. Data Preprocessing
- Label encoding (`ham = 0`, `spam = 1`)
- Text cleaning:
  - Lowercasing
  - Removing punctuation and special characters
  - Removing extra whitespace

### 2. Feature Engineering
- Converted text data to numerical features using **TF-IDF Vectorization**
- Removed English stopwords

### 3. Model Training
- Algorithm used: **Multinomial Naive Bayes**
- Train-test split:
  - 80% Training
  - 20% Testing

### 4. Evaluation
- Model evaluated using accuracy and classification metrics

---

## 🧪 Prediction Example
```python
def predict_spam(text):
    text_tfidf = vectorizer.transform([text])
    prediction = model.predict(text_tfidf)
    return "Spam" if prediction[0] == 1 else "Ham"

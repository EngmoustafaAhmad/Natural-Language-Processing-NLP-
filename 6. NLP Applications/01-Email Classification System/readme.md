
# 📧 Email Classification System using NLP

## 📌 Overview

This project demonstrates how to build an **Email Classification System** using **Natural Language Processing (NLP)** and **Machine Learning**.

The system automatically classifies emails into categories such as:
- 📩 Spam
- 📬 Not Spam (Ham)

---

## 🚀 DAtaset Link download

🔗 [View Project Repository](https://www.kaggle.com/datasets/satyajeetbedi/email-hamspam-dataset?resource=download)

---

## 🧠 Features

- Text preprocessing (cleaning & normalization)
- Feature extraction using **TF-IDF**
- Machine Learning model for classification
- Easy-to-understand pipeline
- Scalable for real-world applications

---

## ⚙️ Technologies Used

- Python 🐍  
- Scikit-learn  
- Pandas  
- NumPy  
- Jupyter Notebook  

---

## 🔄 Workflow

### 1. Text Preprocessing
- Tokenization  
- Lowercasing  
- Removing stop words  
- Removing punctuation  

---

### 2. Feature Engineering
- Convert text into numerical features using **TF-IDF**

---

### 3. Model Training
- Train classification model such as:
  - Naive Bayes  
  - Logistic Regression  

---

### 4. Evaluation
- Accuracy score  
- Confusion matrix  

---

## 🧪 Example

```python
from sklearn.feature_extraction.text import TfidfVectorizer

tfidf = TfidfVectorizer()
X = tfidf.fit_transform(emails)

# 📧 Email Spam Classification (NLP Project)

This project is a Machine Learning model that classifies emails as **Spam** or **Ham (Not Spam)** using Natural Language Processing techniques and classification algorithms.

---

## 🚀 Project Overview

The goal of this project is to detect whether an email message is:
- **Spam (0)** → unwanted or promotional messages
- **Ham (1)** → normal, safe messages

We use:
- TF-IDF Vectorization
- Naive Bayes Classifier
- Logistic Regression Classifier

---

## 📊 Dataset

The dataset contains two columns:
- `Status` → label (ham / spam)
- `Message` → email text content

After preprocessing:
- ham → 1
- spam → 0

---

## 🧠 Machine Learning Models

### 1. Naive Bayes
A probabilistic model based on Bayes theorem:
- Fast and efficient
- Works well with text data

### 2. Logistic Regression
A linear classification model:
- More accurate for complex patterns
- Better generalization than Naive Bayes

---

## 🔄 Workflow

1. Load dataset
2. Clean missing values
3. Convert labels (ham/spam → 1/0)
4. Split data into training and testing sets
5. Convert text into numerical features using TF-IDF
6. Train models (NB & LR)
7. Evaluate performance
8. Test custom messages

---

## 🛠️ Technologies Used

- Python 🐍
- Pandas
- NumPy
- Scikit-learn
- TF-IDF Vectorizer

---

## 📈 Evaluation Metrics

We evaluate models using:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

---

## 📊 Results

Both models are compared:

| Model                | Accuracy | Performance |
|---------------------|----------|-------------|
| Naive Bayes         | High     | Fast but less robust |
| Logistic Regression | Higher   | More balanced & accurate |

---

## 🧪 Example Prediction

```python
sample = ["Congratulations! You won a free ticket. Call now!"]
```
NB Prediction: Spam
LR Prediction: Spam

---

```python
sample = ["Your order has been shipped and will arrive in 2 days!"]
```
NB Prediction: Spam
LR Prediction: Ham

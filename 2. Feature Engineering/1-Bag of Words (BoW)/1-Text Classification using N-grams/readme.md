# Text Classification using N-grams and Bag of Words (BoW) | NLP

## 📌 Overview

In **Natural Language Processing (NLP)**, text data must be converted into numerical form so that **Machine Learning models** can process it.

This project demonstrates two common techniques used for text feature extraction:

* **Bag of Words (BoW)**
* **N-grams**

These techniques transform raw text into numerical vectors that can be used for **text classification tasks** such as sentiment analysis, spam detection, and document classification.

---

# 🧠 Bag of Words (BoW)

## Concept

Bag of Words converts text into a **collection of words** and counts how many times each word appears in a sentence.

It ignores grammar and word order but keeps track of **word frequency**.

---

## Example

### Sentences

```text
I love NLP
I love machine learning
```

### Vocabulary

```text
[I, love, NLP, machine, learning]
```

### Bag of Words Matrix

| Sentence                | I | love | NLP | machine | learning |
| ----------------------- | - | ---- | --- | ------- | -------- |
| I love NLP              | 1 | 1    | 1   | 0       | 0        |
| I love machine learning | 1 | 1    | 0   | 1       | 1        |

Each sentence is converted into a **numerical vector**.

---

# ⚠️ Limitation of BoW

Bag of Words **ignores word order**.

Example:

```text
not good
good
```

BoW may treat them as very similar, even though the meanings are different.

---

# 🔎 N-grams

To solve the word order issue, we use **N-grams**.

An **N-gram** is a sequence of **N words** that appear together.

---

## Types of N-grams

### Unigram (1-gram)

```text
I love NLP
```

Result:

```text
[I, love, NLP]
```

---

### Bigram (2-gram)

```text
I love NLP
```

Result:

```text
[I love, love NLP]
```

---

### Trigram (3-gram)

```text
I love NLP
```

Result:

```text
[I love NLP]
```

---

# 💻 Implementation using Python

We use **CountVectorizer** from the `scikit-learn` library to generate Bag of Words and N-gram features.

---

## Bag of Words Example

```python
from sklearn.feature_extraction.text import CountVectorizer

text = [
    "I love NLP",
    "I love machine learning"
]

cv = CountVectorizer()

X = cv.fit_transform(text)

print(cv.get_feature_names_out())
print(X.toarray())
```

---

## N-grams Example (Unigram + Bigram)

```python
from sklearn.feature_extraction.text import CountVectorizer

text = [
    "I love NLP",
    "I love machine learning"
]

cv = CountVectorizer(ngram_range=(1,2))

X = cv.fit_transform(text)

print(cv.get_feature_names_out())
print(X.toarray())
```

### Explanation

```text
ngram_range=(1,2)
```

Means the model will include:

* **Unigrams (single words)**
* **Bigrams (two-word combinations)**

---

# 📊 Applications

These techniques are widely used in:

* Sentiment Analysis
* Spam Detection
* News Classification
* Chatbot Intent Detection
* Document Categorization

---

# 🛠 Technologies Used

* Python
* NLTK
* Scikit-learn
* NumPy


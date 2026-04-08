### 🔢 TF-IDF (Term Frequency – Inverse Document Frequency)

Measures how important a word is in a document relative to a collection of documents.

---

#### 📌 Idea

- Words that appear **frequently in one document** → important  
- Words that appear **in many documents** → less important  

---

#### 🧮 Formula

```text
TF-IDF(t, d) = TF(t, d) × IDF(t)
```
TF (Term Frequency):

Number of times term t appears in document d

IDF (Inverse Document Frequency):

IDF(t) = log ( N / df(t) )

Where:

N = total number of documents

df(t) = number of documents containing term t

🧠 Example


Document:

"this is a good movie and this movie is amazing"

"movie" appears many times → high TF

but appears in many documents → low IDF

👉 Final TF-IDF balances importance

🎯 Why TF-IDF?

Reduces importance of common words (e.g., "the", "is")

Highlights meaningful words

Improves text representation for ML models

🚀 Use Cases

Search engines ranking

Text classification

Document similarity
Information retrieval

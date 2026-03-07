<div dir="rtl">

# 🧺 Bag of Words (BoW) | معالجة اللغة الطبيعية (NLP)

## 📌 ما هو Bag of Words؟

**Bag of Words (BoW)** هو أحد أبسط الطرق المستخدمة في **تحويل النصوص إلى تمثيل رقمي** حتى يمكن لنماذج التعلم الآلي التعامل معها.

تعتمد الفكرة على:

* تقسيم النص إلى كلمات
* تجاهل ترتيب الكلمات
* حساب عدد مرات ظهور كل كلمة

ولهذا يسمى **Bag of Words** لأن الكلمات تُعامل كأنها داخل "حقيبة" بدون ترتيب.

---

# 🧠 لماذا نستخدم Bag of Words؟

نماذج **Machine Learning** لا تفهم النصوص مباشرة، بل تحتاج إلى **أرقام**.

يقوم BoW بتحويل النص إلى **مصفوفة أرقام (Vectors)** تمثل عدد تكرار الكلمات.

يستخدم في العديد من التطبيقات مثل:

* Text Classification
* Sentiment Analysis
* Spam Detection
* Document Clustering
* Search Engines

---

# 📌 مثال بسيط

لدينا الجمل التالية:

```
I love NLP
I love AI
I hate bugs
```

### 1️⃣ إنشاء Vocabulary

Vocabulary هي جميع الكلمات الفريدة الموجودة في النصوص:

```
I, love, NLP, AI, hate, bugs
```

---

### 2️⃣ تحويل الجمل إلى مصفوفة

| Sentence    | I | love | NLP | AI | hate | bugs |
| ----------- | - | ---- | --- | -- | ---- | ---- |
| I love NLP  | 1 | 1    | 1   | 0  | 0    | 0    |
| I love AI   | 1 | 1    | 0   | 1  | 0    | 0    |
| I hate bugs | 1 | 0    | 0   | 0  | 1    | 1    |

كل صف يمثل **جملة**
وكل عمود يمثل **كلمة**.

---

# ⚙ خطوات تطبيق Bag of Words

1️⃣ **Text Cleaning**

* تحويل النص إلى lowercase
* إزالة علامات الترقيم
* إزالة stop words

2️⃣ **Tokenization**

تقسيم النص إلى كلمات.

3️⃣ **Vocabulary Creation**

استخراج الكلمات الفريدة.

4️⃣ **Vectorization**

حساب عدد تكرار الكلمات.

---

# 🛠 تطبيق عملي باستخدام Python

باستخدام مكتبة **scikit-learn**

```python
from sklearn.feature_extraction.text import CountVectorizer

documents = [
"I love NLP",
"I love AI",
"I hate bugs"
]

vectorizer = CountVectorizer()

X = vectorizer.fit_transform(documents)

print(vectorizer.get_feature_names_out())
print(X.toarray())
```

### الناتج

Vocabulary:

```
['ai', 'bugs', 'hate', 'love', 'nlp']
```

Matrix:

```
[[0 0 0 1 1]
 [1 0 0 1 0]
 [0 1 1 0 0]]
```

---

# 🧩 أنواع Bag of Words

## 1️⃣ Binary Bag of Words

يحدد فقط وجود الكلمة:

```
1 = الكلمة موجودة
0 = الكلمة غير موجودة
```

---

## 2️⃣ Term Frequency (TF)

يسجل **عدد مرات ظهور الكلمة** داخل النص.

---

# 🔗 Bag of Words مع N-grams

يمكن تحسين BoW باستخدام **N-grams**.

مثال:

```
I love NLP
```

### Unigram

```
I
love
NLP
```

### Bigram

```
I love
love NLP
```

---

# 📊 مزايا Bag of Words

✔ سهل الفهم
✔ سريع التنفيذ
✔ مناسب للنماذج التقليدية
✔ يعمل جيدًا في المشاريع الصغيرة

---

# ⚠️ عيوب Bag of Words

❌ يتجاهل ترتيب الكلمات
❌ لا يفهم المعنى أو السياق
❌ ينتج عدد Features كبير
❌ لا يفهم تشابه المعاني

مثال:

```
good
great
excellent
```

BoW يعتبرها كلمات مختلفة رغم تقارب المعنى.

---

# 🔁 تحسين Bag of Words

لتجاوز بعض العيوب نستخدم:

* **TF-IDF**
* **N-grams**
* **Word Embeddings**
* **Transformers**

---

# 📂 مكان Bag of Words في Pipeline الـ NLP

```
Raw Text
   ↓
Text Preprocessing
   ↓
Tokenization
   ↓
Stopwords Removal
   ↓
Bag of Words
   ↓
Machine Learning Model
```

---

# 🚀 استخدامات Bag of Words

* Spam Detection
* Sentiment Analysis
* Document Classification
* News Categorization
* Search Engines

---

⭐ هذا الملف جزء من مشروع

**NLP-to-LLM Roadmap**

</div>

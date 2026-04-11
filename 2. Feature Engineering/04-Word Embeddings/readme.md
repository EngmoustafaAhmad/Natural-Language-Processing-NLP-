
# 🧠 Word Embedding باستخدام TensorFlow

هذا المثال يوضح كيفية بناء **Word Embedding Pipeline** باستخدام  
TensorFlow و Keras لتحويل النصوص إلى تمثيل رقمي (Vectors).

---

# 📌 Overview

في هذا المشروع نقوم بـ:
- تحويل الجمل إلى أرقام (One-Hot Encoding)
- توحيد طول الجمل (Padding)
- إنشاء طبقة Embedding
- تحويل الكلمات إلى Dense Vectors

---

# 📝 Input Sentences

```python
sent = [
    'the glass of milk',
    'the glass of juice',
    'the cup of tea',
    'I am a good boy',
    'I am a good developer',
    'understand the meaning of words',
    'your videos are good'
]

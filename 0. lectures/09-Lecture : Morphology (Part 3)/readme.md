# 📘 Lecture 9: Morphology (Part 3)

## 📌 Overview
This lecture focuses on:
- Ambiguity in morphology
- Stemming vs full morphological analysis
- The Porter Stemmer
- Arabic Morphology

---

## ❓ Quick Concept Check

### Question:
Which type of morphology keeps the **same word class**?

### ✅ Answer:
**Inflectional Morphology**

---

## 🔀 Ambiguity in Morphology

### Definition:
Ambiguity occurs when a word has **multiple valid analyses (parses)**.

### Example:

unionizable →

union + ize + able
un + ion + ize + able

👉 Both are valid → multiple interpretations

---

## ⚠️ Why Ambiguity Happens?

- In **FSTs**, different paths = different outputs  
- Unlike FSA → path didn’t matter  
- In FST → path = meaning

---

## 🧠 Handling Ambiguity

There are 3 main approaches:

1. **First Solution Only**
   - Take the first valid parse

2. **Return All Solutions**
   - Return all possible interpretations

3. **Best Path (Smart Search)**
   - Choose most likely interpretation

---

## 🔤 Morphological Complexity

Real language is NOT simple:

### Examples:
- `cats` vs `dogs` → different pronunciation (s / z)
- `fox → foxes` → add "e"
- `bag → bagged` → double letter

👉 Morphology includes:
- Spelling changes
- Pronunciation changes
- Irregular forms

---

## 🔍 Stemming vs Morphology

### 🟢 Stemming
- Extracts **root only**
- Ignores structure
- Used in **Search Engines (IR)**

### 🔴 Morphological Analysis
- Extracts:
  - Root
  - Structure
  - Meaning

---

## ⚖️ Comparison

| Feature | Stemming | Morphological Analysis |
|--------|---------|------------------------|
| Output | Root only | Full structure |
| Accuracy | Low | High |
| Speed | Fast | Slower |
| Use Case | Search engines | NLP systems |

---

## ⚙️ The Porter Stemmer

### Definition:
A popular **stemming algorithm** (Porter, 1980)

### Features:
- Rule-based
- Removes affixes
- Works without lexicon
- Fast and efficient

---

## 🔧 Example Rules

| Rule | Example |
|------|--------|
| ATIONAL → ATE | relational → relate |
| ING → ε | motoring → motor |
| SSES → SS | grasses → grass |
| IZATION → IZE | computerization → computerize |
| IZE → ε | computerize → computer |

---

### ⚠️ Important Note:
- Result is **not always a real word**
- But it's acceptable in search systems

---

## 🌍 Arabic Morphology

### Key Idea:
Arabic has **very rich and complex morphology**

---

## ✨ Features of Arabic Morphology

- Prefixes (و، ف، ب...)
- Suffixes (ها، هم...)
- Root-based system
- Gender, number, tense
- Dual form (not in English)

---

## 🧠 Example

### Word:

فسيأكلونها


### Meaning:

"And they will eat it"


### Contains:
- ف → and
- س → future
- يأكل → eat
- ون → plural
- ها → it

👉 One word = full sentence!

---

## ⚠️ Challenges in Arabic NLP

- Complex structure
- High ambiguity
- Many affixes
- Different word forms

---

## 🔁 Key Takeaways

- Ambiguity = multiple valid parses
- FST paths represent different meanings
- Stemming is simpler than full morphology
- Porter Stemmer is fast but approximate
- Arabic morphology is highly complex
- Real NLP systems must handle ambiguity

---

## 🚀 Final Insight

In real NLP systems:
- We balance between:
  - ⚡ Speed (Stemming)
  - 🎯 Accuracy (Morphological Parsing)

And often combine both depending on the application.

# 📘 Lecture 7: Morphology (Part 1)

## 📌 Overview
Morphology is a fundamental concept in **Natural Language Processing (NLP)** that studies how words are formed from smaller meaningful units called **morphemes**.

Understanding morphology is essential for:
- Text Preprocessing
- Machine Translation
- Information Retrieval
- Spell Checking

---

## 🧠 What is Morphology?

Morphology studies how words are constructed from smaller units:

- **Morphemes** → smallest units of meaning  

### Examples:
- `cats = cat + s`
- `unhappy = un + happy`

### 🔹 Types of Morphemes

| Type  | Description                 | Example         |
|-------|----------------------------|-----------------|
| Stem  | Core meaning of the word   | play, friend    |
| Affix | Added to modify meaning    | -s, un-, -ing   |

---

## 🔧 Types of Affixes

| Type       | Position        | Example                |
|------------|----------------|------------------------|
| Prefix     | Before stem    | un + do → undo         |
| Suffix     | After stem     | eat + s → eats         |
| Infix      | Inside stem    | (rare in English)      |
| Circumfix  | Around stem    | prefix + suffix        |

---

## 🔄 Types of Morphology

### 1️⃣ Inflectional Morphology
- Does **NOT change word class**
- Adds grammatical meaning

#### Examples:

| Word | Inflected Form | Class |
|------|--------------|-------|
| eat  | eats         | Verb  |
| cat  | cats         | Noun  |

#### Features:
- Plural → `cat → cats`
- Possessive → `John → John’s`
- Verb forms:
  - `walk → walked`
  - `walk → walking`

---

### 2️⃣ Derivational Morphology
- Changes **meaning AND word class**

#### Examples:

| Base    | Derived   | Change              |
|---------|----------|---------------------|
| compute | computer | Verb → Noun         |
| friend  | friendly | Noun → Adjective    |
| do      | undo     | Meaning change      |

#### Common Affixes:
- `-er` → killer  
- `-ness` → happiness  
- `-ation` → transportation  
- `-able` → breakable  

---

## ⚠️ Regular vs Irregular Forms

### ✔️ Regular:
- Follow rules  
- Example: `walk → walked`

### ❌ Irregular:
- Do not follow rules  
- Examples:
  - `go → went`
  - `mouse → mice`

---

## 🔍 Morphological Parsing

### Definition:
Breaking a word into its morphemes.

### Examples:
- `cats → cat + N + PL`
- `foxes → fox + es`

### Importance:
- Machine Translation  
- Search Engines  
- NLP Systems  

---

## 🤖 Finite-State Morphological Parsing

To build a morphological parser, we need:

### 1. Lexicon
- List of stems + affixes  
- Example:
  - `cat (noun)`
  - `walk (verb)`

### 2. Morphotactics
- Rules of morpheme order  

**Example:**
- noun + plural suffix ✔  
- plural + noun ✖  

### 3. Orthographic Rules
- Handle spelling changes  

**Example:**
- `city + s → cities`  
- `(y → ie)`

---

## 🔗 Morphology and Finite State Automata (FSA)

### FSA is used to:
- ✅ Accept valid words  
- ❌ Reject invalid words  
- Avoid storing all possible word forms  

### Example:
- Accept: `cats`  
- Reject: `foxs` ❌  

---

## ⚙️ Recognition vs Parsing

| Task        | Description               |
|------------|--------------------------|
| Recognition | Check if word is valid   |
| Parsing     | Extract structure        |

### Example:
- `ate → eat + V + PAST`

---

## 📈 Key Takeaways

- Words are built from **morphemes**
- Morphology has two types:
  - Inflectional → same class  
  - Derivational → changes class  
- Morphological parsing is critical in NLP  
- FSAs help automate word validation  
- Morphology is essential in real-world NLP systems  

---

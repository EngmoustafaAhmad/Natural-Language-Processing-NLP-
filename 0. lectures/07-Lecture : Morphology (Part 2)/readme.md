# 📘 Lecture 8: Morphology (Part 2)

## 📌 Overview
This lecture extends morphology concepts by introducing **Finite-State Transducers (FSTs)** for **morphological parsing**.

We move from simple word validation (FSA) to:
- Mapping between word forms
- Handling spelling changes
- Generating and analyzing words

---

## 📚 Lexicons in NLP

- A **lexicon** is a collection of words (stems + affixes).
- It can be represented using **Finite State Automata (FSA)**.

### Key Idea:
- Instead of storing all word forms, we:
  - Store base words
  - Use rules to generate variations

### Application:
- Spell Checking ✔  
- Word Recognition ✔  

⚠️ Limitation:
- FSA only tells:
  - ✅ Valid word
  - ❌ Invalid word  
- It does NOT provide structure (no parsing)

---

## 🔄 From FSA to FST

To perform **morphological parsing**, we use:

### 👉 Finite-State Transducer (FST)

### Definition:
An **FST** is a machine that:
- Reads an input string
- Produces an output string

### Example:

Input → cats
Output → cat +N +PL


---

## ⚙️ FSA vs FST

| Feature | FSA | FST |
|--------|-----|-----|
| Output | ❌ No | ✅ Yes |
| Purpose | Recognition | Mapping |
| Result | Accept / Reject | Transform input → output |

---

## 🔁 Two-Level Morphology

Proposed by **Koskenniemi (1983)**

Words are represented in two levels:

### 1️⃣ Lexical Level
- Structure of word
- Example:

cat +N +PL


### 2️⃣ Surface Level
- Final written form

cats


### 🎯 Goal:
Map between:

Lexical ↔ Surface


---

## 🔌 How FST Works

- Works like a **two-tape machine**:
  - Tape 1 → Input
  - Tape 2 → Output

### Example:

Tape 1: cats
Tape 2: cat +N +PL


---

## 🔤 Regular Relations

- **Regular Language** → set of strings  
- **Regular Relation** → set of string pairs  

### Example:

{ a:1 , b:2 , c:2 }


---

## 🔧 Morphological Parsing with FST

### Goal:
Convert:

Surface → Lexical
cats → cat +N +PL


### Process:
- Read characters
- Apply rules
- Output morphemes + features

---

## ✏️ Orthographic Rules

Handle spelling changes when combining morphemes.

### Example:

city + s → cities
(y → ie)


### Another Example:

fox + s → foxes


---

## 🧠 Multi-Level Tape Machines

To handle complex transformations:

We use **multiple FSTs in sequence (cascade)**

### Flow:

Lexical → Intermediate → Surface


### Steps:
1. Lexical → Intermediate (morpheme combination)
2. Intermediate → Surface (spelling rules)

---

## 🔗 Cascade Architecture

- Processing is divided into stages
- Output of one stage = input to next

### Example Pipeline:

Lexical Form
↓
Lexicon FST
↓
Intermediate Form
↓
Orthographic FST
↓
Surface Word


---

## ⚠️ Ambiguity in Parsing

Parsing is harder than generation because:

👉 One word can have multiple meanings

### Example:

foxes →

fox +N +PL
fox +V +3SG

### Problem:
- FST cannot decide correct meaning alone

### Solution:
- Use context (surrounding words)

---

## 🔁 Parsing vs Generation

| Task       | Direction |
|------------|----------|
| Parsing    | Surface → Lexical |
| Generation | Lexical → Surface |

---

## 📈 Key Takeaways

- FST extends FSA by adding **output capability**
- Used for **morphological parsing**
- Words are represented in:
  - Lexical level
  - Surface level
- Orthographic rules handle spelling changes
- Multi-level FSTs improve accuracy
- Ambiguity requires external context

---

## 🚀 Final Insight

Morphological systems in NLP are built using:
- Lexicon (words)
- Morphotactics (rules)
- Orthographic rules (spelling)
- FSTs (mapping)

Together, they allow machines to:
- Understand words
- Generate correct forms
- Handle language complexity efficiently



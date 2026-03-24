# 🔄 Finite State Machines (Part 3)

## 📌 Overview
This lecture continues the study of **Finite State Machines (FSMs)** and focuses on:

- Deterministic Recognition
- D-Recognize Algorithm
- Non-Determinism
- Equivalence between DFA and NFA
- Non-Deterministic Recognition
- Compositional Machines
- Why we use FSAs

---

# 🧠 Deterministic Recognition

## 📌 Definition
Recognition (Acceptance) is the process of:

- Checking if a string belongs to a language
- Determining if a machine accepts a string
- Matching a string with a Regular Expression

👉 All mean the same thing:

Is this string valid according to the language?

## How Recognition Works

Start at initial state (q0)

Read input symbol by symbol

Follow transitions

Stop when input ends

✅ Result:

If current state ∈ F → Accept

Else → Reject

🧪 Example: Sheep Language

Language:

{ baa!, baaa!, baaaa!, ... }

❌ Example Rejected Input:

b!aba

⚙️ D-Recognize Algorithm

📌 Definition


A table-driven algorithm used to simulate DFA behavior.

🔄 Steps

Initialize state = q0

For each symbol in input:

Look up transition in table

Move to next state

After input ends:

If state ∈ F → Accept

Else → Reject

🧠 Key Features

Deterministic → no ambiguity

Always one action per step

Works for all DFA

💡 Important Insight

Regex Matching = 

1. Convert Regex → DFA

2. Run D-Recognize

## 🔀 Non-Determinism

📌 Definition

A system where:

Multiple transitions are possible

Machine may have choices

Can include ε-transitions

⚠️ Key Idea

DFA → One path only

NFA → Many possible paths

## 🔁 ε-Transitions

Move between states without consuming input

Do NOT move tape pointer

⚖️ Equivalence (DFA vs NFA)

📌 Key Fact

DFA ≡ NFA (same power)


👉 Meaning:

Both recognize Regular Languages

NFA is NOT more powerful than DFA

🔄 Conversion

NFA → DFA (always possible)

🔍 Non-Deterministic Recognition

📌 Two Approaches

## 1️⃣ Convert then Run

NFA → DFA → D-Recognize

## 2️⃣ Direct Search

Explore all possible paths

⚙️ Recognition Logic

Accept if:

At least one path reaches final state

Reject if:

All paths fail

## 🔁 Backtracking

Try first path

If fails → go back and try another

🧩 Compositional Machines

📌 Idea

Languages = Sets of Strings

👉 So we can apply operations:

## 🔀 Operations on Languages

## 1️⃣ Union (OR)

A ∪ B → Accept strings in A or B

## 2️⃣ Concatenation

A • B → Strings from A followed by B

## 3️⃣ Negation

¬A → Strings NOT in A




⚠️ Works only with DFA


## 4️⃣ Intersection

A ∩ B = ¬(¬A ∪ ¬B)

🧪 Example

📌 Language

(01)+ | (010)+


👉 Strings:

01, 0101, ...

010, 010010, ...

🧠 Regex

(01)+|(010)+

🚀 Why Use FSA?

✅ Advantages

Simple and efficient

Great for pattern matching

Used in:

NLP

Compilers

Regex engines

⚠️ Limitations

Cannot represent full natural language

Limited to Regular Languages

## ⚖️ DFA vs NFA Trade-off

Feature	DFA	NFA

Speed	Fast	Slower

Design	Complex	Simple

Paths	One	Multiple

ε-transitions	❌ No	✅ Yes

## Key Takeaways

Recognition = checking if string ∈ language

DFA uses D-Recognize algorithm

NFA explores multiple paths

DFA and NFA are equivalent

FSAs are powerful for:

Pattern matching

Text processing


NLP preprocessing
📚 Summary
Regex → Automata → Recognition

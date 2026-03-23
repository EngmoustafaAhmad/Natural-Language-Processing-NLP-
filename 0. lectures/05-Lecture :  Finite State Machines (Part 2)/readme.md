# 🔄 Finite State Machines (Part 2)

## 📌 Overview
This lecture continues **Finite State Machines (FSMs)** and focuses on:

- Deterministic Finite Automata (DFA)
- Non-Deterministic Finite Automata (NFA)
- Differences between DFA and NFA
- Building automata for real problems

---

# 🧠 Deterministic Finite Automata (DFA)

## 📌 Definition
A DFA is a machine that:

- Has **only one possible state at a time**
- Has **exactly one transition** for each input symbol

---

## 🔧 Components of DFA

```text
{ Q , Σ , q0 , F , δ }
```
| Symbol |	Description |
|--------|--------|
| Q |	Set of states|
| Σ |	Alphabet|
| q0 |	Start state|
| F |	Accept (final) states|
| δ |	Transition function|

⚙️ How DFA Works
📥 Input:

String w

🔄 Steps:


Start at q0

Read input symbol by symbol

Move using transition function δ

End in a state:

If in F → ✅ Accept

Else → ❌ Reject

🐑 Example: Sheep Language

📌 Language:

{ baa!, baaa!, baaaa!, ... }
🔗 Regular Expression:

```
/baa+!/
```

🧠 DFA Design

Q = {q0, q1, q2, q3, q4}

Σ = {b, a, !}

Start = q0

Final = q4

⚠️ Important Note

If input does not match pattern → goes to dead (fail) state

🔢 Example: DFA for Numbers (1–99)

Accept numbers between 1 and 99

Uses digit transitions

Ensures valid numeric structure

🌐 Example: Web Address DFA

📌 Goal:

Accept valid URLs like:

http://www.facebook.com
🧠 Alphabet:
Σ = { http, ://, www, a-z, ., com, org, / }
🧾 Language of a DFA
📌 Definition

A string is accepted if:

```
L(A) = { w | δ(q0 , w) ∈ F }
```

👉 Meaning:

Start from q0
Follow transitions
End in a final state
🔍 Example: Strings Containing "01"
📌 Language:

```
L = { w | w contains "01" }
```

🔗 Regular Expression:
(0|1)*01(0|1)*
🧠 DFA Design
Q = {q0, q1, q2}
Σ = {0,1}
Start = q0
Final = q2
## 🔀 Non-Deterministic Finite Automata (NFA)
📌 Definition

An NFA:

Can be in multiple states at the same time
May have multiple transitions for same input
May include ε-transitions (no input)
🔧 Components of NFA
{ Q , Σ , q0 , F , δ }
⚠️ Difference:
δ: Q × Σ → subset of Q

👉 Returns set of states, not one state

⚙️ How NFA Works
📥 Input:

String w

🔄 Steps:
Start at q0
For each input:
Follow all possible transitions
After input ends:
If any state ∈ F → ✅ Accept
Else → ❌ Reject
🧠 Language of NFA

```
L(N) = { w | δ(q0,w) ∩ F ≠ ∅ }
```

👉 Accept if at least one path reaches final state

🔍 Example: NFA for "01"
🔗 Regular Expression:

```
(0|1)*01(0|1)*
```

💡 Why NFA?

Easier to represent regex

More flexible transitions

⚖️ DFA vs NFA

Feature	DFA	NFA

States	One at a time	Multiple

Transitions	One per input	Many possible

ε-moves	❌ No	✅ Yes

Speed	Faster	Slower (conceptually)

Design	Complex	Simpler

## Key Insight

👉 Both DFA and NFA recognize the same class: Regular Languages

🚨 Key Differences Explained

DFA:

No ambiguity

One path only

Deterministic behavior

NFA:

Multiple paths

Can "guess" correct path

Easier to construct

## Key Takeaways

DFA = strict, fast, single path

NFA = flexible, multiple paths

Both represent Regular Languages

Used in:

NLP

Compilers

Regex engines

## Applications

Lexical analysis

Pattern matching

Text validation

Search engines

NLP preprocessing

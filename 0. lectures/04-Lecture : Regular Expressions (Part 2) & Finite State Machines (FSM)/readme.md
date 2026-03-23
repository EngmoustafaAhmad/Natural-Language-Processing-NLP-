# 🔤 Regular Expressions (Part 2) & Finite State Machines (FSM)

## 📌 Overview
This lecture continues **Regular Expressions** and introduces **Finite State Machines (FSMs)**, which are fundamental for modeling languages and text processing in NLP.

---

# 🔀 Regular Expressions (Advanced)

## 🔁 Disjunction Operator `|` (OR)

### 📌 Definition
Used to match one of multiple patterns.

```regex
a|b|c
```

✅ Equivalent:
[abc]
🧪 Examples:
hello|Hello
a+|b+
ab+|ba+
🧩 Grouping with Parentheses ( )
📌 Why?

To control how disjunction applies.

/(Column[0-9]+ *)*/
💡 Meaning:
"Column" followed by digits
Optional spaces
Repeated multiple times
🧪 Examples
1️⃣ Match "cat" or "dog"

❌ Wrong (false positives):

/\b[cd][ao][tg]\b/

✔️ Correct:

/\b(cat|dog)\b/
2️⃣ Match "guppy" and "guppies"
/\bgupp(y|ies)\b/
⚓ Anchors
📌 Start of line ^
/^The/

Matches "The" only at the beginning

📌 End of line $
/The dog\.$/

Matches:

"The dog." only
⚠️ Operator Precedence
🔝 Order (High → Low):
Quantifiers (*, +, ?, {})
Concatenation
Disjunction (|)
🧪 Examples:
/the*/

✔️ Matches: theeee
❌ Not: thethe

/the|any/

✔️ Matches: the or any

🧪 Practice Examples
{lass, class, glass}
/[cg]?lass/
{jet, pet, net}
/[jpn]et/
{sun, sunday, sunrise, sunset}
/sun(ε|day|rise|set)/
❓ MCQ Concepts
✔️ Letter "b" as second character:
/[a-z]b[a-z]*/
✔️ Pattern:
/[Cc]ats?/
✅ Matches:
cat
cats
Cat
Cats
🧠 Formalisms
📌 3 Ways to Represent Languages
Regular Expressions
Text patterns
Finite State Automata (FSA)
Graph representation
Regular Grammars
Rule-based
🔄 Finite State Machines (FSM)
📌 What is FSM?
A machine used to recognize patterns (languages)
Works using states and transitions
🧩 Finite State Automata (FSA)
📌 Definition
Recognizes Regular Languages
Represented as a graph
🔧 Components of DFA

A DFA is defined as:

{ Q , Σ , q0 , F , δ }
🧱 Meaning:
Symbol	Description
Q	Set of states
Σ	Input alphabet
q0	Start state
F	Accept states
δ	Transition function
🔄 How DFA Works
📥 Input:

String w

⚙️ Steps:
Start at q0
Read input symbol by symbol
Move between states using δ
If final state ∈ F → ✅ Accept
Otherwise → ❌ Reject
🔀 Types of FSA
1️⃣ Deterministic (DFA)
Only one state at a time
2️⃣ Non-Deterministic (NFA)
Multiple possible states
🧠 Key Concept

If a language is recognized by DFA:

👉 It is a Regular Language

🧪 Regex Practice (Extra)
🎯 Character Classes
be[ls]t

Matches: belt, best

be[l-o]t

Matches: belt, bemt, bent, beot

❌ Negation
be[^0-9]t

Matches any non-digit in middle

🔁 Quantifiers
fo*ot

Matches: fot, foot, foooooot

go{2,3}gle

Matches: google, gooogle

🌟 Meta Characters
Symbol	Meaning
.	Any character
[]	Set
[^]	Negation
-	Range
🧠 Key Takeaways
Regex defines patterns for text
Parentheses control grouping
Anchors define position
FSM models language recognition
DFA = deterministic, NFA = flexible
🚀 Applications
Text processing
NLP preprocessing
Search engines
Compilers
Spell checking
📚 References
Jurafsky & Martin — Speech and Language Processing

---

لو عايز أحول لك كل المحاضرات لحد دلوقتي إلى **GitHub Repo كامل (README رئيسي + فولدر لكل Lecture + تنظيم احترافي)** قولي وهنعمله level production 🔥

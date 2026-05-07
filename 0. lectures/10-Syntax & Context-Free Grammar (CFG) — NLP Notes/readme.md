# Syntax & Context-Free Grammar (CFG) — NLP Notes

## 📌 What is Syntax?
Syntax is the study of:
- The order of words in a sentence.
- The relationship between words.

It helps determine how words combine to form meaningful sentences.

### Example
In English, a common sentence structure is:

Subject + Verb + Object

Example:
> Adel studies Automata.

---

# Why is Syntax Important?
Syntax and parsing are used in many NLP applications such as:

- Grammar Checkers
- Question Answering Systems
- Information Extraction
- Machine Translation

---

# Context-Free Grammar (CFG)

CFG is a grammar system used to describe the structure of languages.

It is also called:
- Phrase Structure Grammar
- Backus-Naur Form (BNF)

---

# Components of CFG

A CFG consists of:

## 1. Terminals
These are the actual words in the language.

Example:
```text
Adel, study, with
```
## 2. Non-Terminals

These represent grammatical categories.

Examples:
```
S  -> Sentence
NP -> Noun Phrase
VP -> Verb Phrase
Verb
Noun
```
## 3. Production Rules

Rules define how symbols can be expanded.

General form:
```
Non-terminal → terminals/non-terminals
```
Example:
```
NP → Det Nominal
```
Meaning:
A noun phrase can consist of:

Determiner + Nominal


## Example of NP Rules
```
NP → Det Nominal
NP → ProperNoun
Nominal → Noun | Nominal Noun
```
## Explanation

These rules describe:

NP can be:
Determiner + Nominal
Or:
Proper noun directly



## Important Concepts
### 1. Disjunction (|)

Means "OR"

Example:
```
Nominal → Noun | Nominal Noun
```
Meaning:
Nominal can be:

Noun
OR Nominal followed by Noun

### 2. Recursion

When the same non-terminal appears on both sides of the rule.

Example:
```
Nominal → Nominal Noun
```
This allows generating longer phrases.


## Formal Definition of CFG

A CFG contains:

### 1.Production Rules
### 2.Lexicon (words/symbols)

The grammar defines how valid sentences are formed.

## Correct CFG Rule Conditions

A valid CFG rule must:

Have exactly one non-terminal on the left side.
## Question (1)

Given:

Non-terminals = {A, B}
Terminals = {a, b}

Which rule is NOT correct?
```
1. A → a
2. A → a | bA
3. AB → a
4. a → bA
```
Solution

Incorrect rules:
```
3. AB → a
4. a → bA
```
Why?
Rule 3
```
AB → a
```
Left side contains two non-terminals.

CFG requires:

ONLY one non-terminal on the left side.
Rule 4
```
a → bA
```
Left side is a terminal.

CFG requires:

Left side must be a non-terminal.


## Question (2)

Given:

Terminals = {a, the, study}
Non-terminals = {VP, Verb, Det}

Which rule is NOT correct?
```
1. Det → a | the
2. VP → Verb
3. Verb → study
4. a → Det
```
Solution

Incorrect rule:
```
4. a → Det
```
Because:

Left side is terminal (a)
CFG rules must start with a non-terminal.
Derivation

# Lecture 02 — NLP Basics (Lexicon, POS, Ambiguity, Formal Languages)

Course: Natural Language Processing
Focus: Lexicon, POS Tagging, Ambiguity, Formal Language Theory

## 📌 Overview

This lecture introduces core NLP foundations including:

Lexicon (Vocabulary)
Part of Speech (POS)
POS Tagging
Ambiguity in language
Formal language concepts
Chomsky Hierarchy
## Lexicon

A Lexicon is a repository of words in a language.

### 🔹 Includes:
Words (stems)
Affixes
Linguistic information (e.g., noun, verb)
### 📌 Notes:
Varies across domains (e.g., medical, technical)
Words are grouped into categories
Examples:
Noun
Verb
Adjective
Preposition
## 🏷️ Part of Speech (POS)

POS represents grammatical categories of words.

### 🔹 Common POS Tags:
Noun (NN)
Verb (VB)
Adjective (JJ)
Adverb (RB)
Determiner (DET)
Preposition (P)
### 💡 Importance:
Helps understand sentence structure
Essential for syntactic analysis
## Part of Speech Tagging
### 📌 Definition:

Assigning a POS tag to each word in a sentence.

Example:
Input:  Time flies like an arrow
Output: Time/NN flies/VB like/P an/DET arrow/NN
### Why Important?
First step in NLP pipelines
Required for parsing and understanding
### Ambiguous Words

Some words have multiple POS or meanings.

Examples:

like

Verb → I like NLP
Preposition → Time flies like an arrow

back

Noun → on my back
Verb → back the project
Adjective → back door
### Solution:

➡️ Use context to determine the correct meaning

## Ambiguity in NLP

Ambiguity is a core challenge in NLP.


Types:

Lexical Ambiguity → word has multiple meanings

Syntactic Ambiguity → multiple sentence structures

Semantic Ambiguity → unclear meaning

🎯 Example:

I made her duck

Possible meanings:

Cooked duck for her

Cooked her duck

Created a duck

Made her lower her head

Transformed her into a duck 😅

## Cause:

Word ambiguity (duck, her)

Verb ambiguity (make)

## Alphabet (∑)

An alphabet is a finite set of symbols.

Examples:

Binary → {0,1}

Letters → {a–z}

Alphanumeric → {a–z, A–Z, 0–9}

## Strings

A string is a sequence of symbols from an alphabet.

Key Concepts:

Length → |w|

Empty string → ε

Concatenation → xy

Sets:

∑* → all possible strings

∑+ → all non-empty strings

## 🌐 Language

A language is a set of strings.

Definition:

L ⊆ ∑*

Examples:

Equal number of 0s and 1s

n zeros followed by n ones

❓ Membership Problem

Problem:

Determine if a string belongs to a language.

Example:

w = 100011

Language: equal number of 0s and 1s

✔ Yes

🧱 The Chomsky Hierarchy

A classification of formal languages:

Type	Machine

Regular	Finite Automata (DFA/NFA)

Context-Free	Pushdown Automata (PDA)

Context-Sensitive	Linear Bounded Automata (LBA)

Recursively Enumerable	Turing Machine (TM)

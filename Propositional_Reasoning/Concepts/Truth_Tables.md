# Truth Tables

## Intuition

We now know how to combine propositions using connectives. But how do we systematically determine the truth value of a complex compound proposition like $\neg(P \rightarrow Q) \lor (P \land \neg Q)$? 

A **truth table** is a mechanical procedure for doing exactly this. It exhaustively lists every possible combination of truth values for the component propositions, and computes the truth value of the compound proposition for each combination. No reasoning required — just systematic application of the connective definitions.

This exhaustiveness is what makes truth tables powerful: if a compound proposition is true in every row, it is true for *every possible* assignment of truth values — not just the ones we happened to check.

---

## How to Build a Truth Table

Given a compound proposition with $n$ distinct propositional variables, the truth table has $2^n$ rows — one for each possible combination of truth values.

**Step 1**: List all propositional variables as columns on the left.

**Step 2**: Fill in all $2^n$ combinations of T and F systematically.

**Step 3**: Add a column for each subexpression, working from the inside out.

**Step 4**: The final column is the truth value of the whole compound proposition.

---

## Example 1 — One Variable

$$\neg P$$

| $P$ | $\neg P$ |
|-----|---------|
| T | F |
| F | T |

$2^1 = 2$ rows.

---

## Example 2 — Two Variables

$$P \rightarrow Q$$

| $P$ | $Q$ | $P \rightarrow Q$ |
|-----|-----|------------------|
| T | T | T |
| T | F | F |
| F | T | T |
| F | F | T |

$2^2 = 4$ rows.

---

## Example 3 — Working Inside Out

$$\neg P \lor Q$$

We build this in steps — first compute $\neg P$, then compute $\neg P \lor Q$:

| $P$ | $Q$ | $\neg P$ | $\neg P \lor Q$ |
|-----|-----|---------|----------------|
| T | T | F | T |
| T | F | F | F |
| F | T | T | T |
| F | F | T | T |

Notice: the final column of $\neg P \lor Q$ is identical to the final column of $P \rightarrow Q$ above. This is not a coincidence — we will formalize this in Logical Equivalence.

---

## Example 4 — Three Variables

$$P \land (Q \lor R)$$

$2^3 = 8$ rows:

| $P$ | $Q$ | $R$ | $Q \lor R$ | $P \land (Q \lor R)$ |
|-----|-----|-----|-----------|---------------------|
| T | T | T | T | T |
| T | T | F | T | T |
| T | F | T | T | T |
| T | F | F | F | F |
| F | T | T | T | F |
| F | T | F | T | F |
| F | F | T | T | F |
| F | F | F | F | F |

---

## Counterexamples & Common Mistakes

- **Missing rows**: With $n$ variables you need exactly $2^n$ rows. Missing rows means missing cases.
- **Wrong column order**: Always build subexpressions before the full expression. Computing the outer connective before the inner ones leads to errors.
- **Confusing $\rightarrow$ with $\leftrightarrow$**: Implication is false only in one case (T, F). Biconditional is true in two cases (T,T) and (F,F).

---

## Connections

- **Logical Equivalence**: Two propositions are logically equivalent if and only if their truth tables are identical in the final column. Truth tables are the primary tool for checking equivalence.
- **Tautologies & Contradictions**: A proposition is a tautology if its final column is all T. It is a contradiction if its final column is all F. Truth tables make this checkable mechanically.
- **Logical Connectives**: Each connective is fully *defined* by its truth table. The truth table is not a consequence of the connective — it *is* the connective, semantically speaking.
- **Formal Syntax vs. Semantics**: Truth tables are a semantic tool — they assign *meaning* (truth values) to syntactic expressions. This distinction becomes central in Mathematical Logic.
- **Propositional Logic (formal)**: In the formal treatment, truth tables correspond to the notion of a **valuation** — a function assigning truth values to propositional variables.

---

## Exercises

1. Build the truth table for $P \land \neg P$. What do you notice about the final column?

2. Build the truth table for $P \lor \neg P$. What do you notice?

3. Build the truth table for $\neg(P \land Q)$ and for $\neg P \lor \neg Q$. Compare the final columns. What can you conclude?

4. Build the truth table for $P \rightarrow Q$ and for $\neg P \lor Q$. Compare the final columns.

5. Build the truth table for $(P \rightarrow Q) \land (Q \rightarrow P)$. Compare the final column to the truth table for $P \leftrightarrow Q$.
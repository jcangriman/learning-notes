# Logical Connectives

## Intuition

A single proposition like "$7$ is prime" is useful, but mathematics rarely reasons about isolated facts. We combine propositions: "$n$ is even *and* $n$ is greater than $2$", "$p$ is prime *or* $p = 1$", "*if* $n$ is even *then* $n$ is divisible by $2$." 

**Logical connectives** are the formal tools for combining propositions into more complex ones. Crucially, the truth value of a compound proposition depends *only* on the truth values of its parts — not on what those parts are about. This is what makes propositional logic a *formal* system.

---

## The Five Connectives

Let $P$ and $Q$ be propositions.

---

### Conjunction — "and" ($\land$)

$$P \land Q$$

Read: "$P$ and $Q$." True when *both* $P$ and $Q$ are true. False otherwise.

---

### Disjunction — "or" ($\lor$)

$$P \lor Q$$

Read: "$P$ or $Q$." True when *at least one* of $P$, $Q$ is true. False only when both are false.

> This is **inclusive or** — it includes the case where both are true. This differs from everyday English "or," which is sometimes exclusive ("soup or salad" usually means one or the other, not both). In logic, $\lor$ is always inclusive unless stated otherwise.

---

### Negation — "not" ($\neg$)

$$\neg P$$

Read: "not $P$." Flips the truth value of $P$. True when $P$ is false, false when $P$ is true.

> Negation is the only connective that takes a single proposition rather than two.

---

### Implication — "implies" ($\rightarrow$)

$$P \rightarrow Q$$

Read: "if $P$ then $Q$", or "$P$ implies $Q$." $P$ is called the **hypothesis** (or **antecedent**) and $Q$ is called the **conclusion** (or **consequent**).

This is the most subtle connective. It is **false only when $P$ is true and $Q$ is false** — in all other cases it is true.

The case that surprises most people: if $P$ is false, then $P \rightarrow Q$ is **true** regardless of $Q$. This is called a **vacuously true** implication. The intuition: a conditional promise is only broken if you satisfy the condition but fail to deliver the conclusion. If the condition is never met, the promise is never broken.

---

### Biconditional — "if and only if" ($\leftrightarrow$)

$$P \leftrightarrow Q$$

Read: "$P$ if and only if $Q$" (often abbreviated "iff"). True when $P$ and $Q$ have the *same* truth value — both true or both false.

$$P \leftrightarrow Q \text{ is equivalent to } (P \rightarrow Q) \land (Q \rightarrow P)$$

---

## Summary Table

| $P$ | $Q$ | $P \land Q$ | $P \lor Q$ | $\neg P$ | $P \rightarrow Q$ | $P \leftrightarrow Q$ |
|-----|-----|------------|-----------|---------|------------------|----------------------|
| T | T | T | T | F | T | T |
| T | F | F | T | F | F | F |
| F | T | F | T | T | T | F |
| F | F | F | F | T | T | T |

---

## Examples

Let $P$ = "$6$ is even" (true) and $Q$ = "$6$ is prime" (false).

| Compound Proposition | Value |
|---------------------|-------|
| $P \land Q$ — "$6$ is even and prime" | False |
| $P \lor Q$ — "$6$ is even or prime" | True |
| $\neg P$ — "$6$ is not even" | False |
| $P \rightarrow Q$ — "if $6$ is even then $6$ is prime" | False |
| $Q \rightarrow P$ — "if $6$ is prime then $6$ is even" | True (vacuously) |
| $P \leftrightarrow Q$ — "$6$ is even iff $6$ is prime" | False |

---

## Counterexamples & Common Mistakes

- **Implication is not causation**: "$P \rightarrow Q$" does not mean $P$ *causes* $Q$, only that whenever $P$ is true, $Q$ is also true.
- **Vacuous truth**: "If $0$ is odd then the moon is made of cheese" is a true proposition — because the hypothesis is false, the implication is never violated.
- **Inclusive vs. exclusive or**: "$P \lor Q$" is true when both $P$ and $Q$ are true. Exclusive or (written $P \oplus Q$) is false when both are true. We use inclusive or unless stated otherwise.
- **Implication is not symmetric**: $P \rightarrow Q$ and $Q \rightarrow P$ are different propositions with potentially different truth values.

---

## Connections

- **Truth Tables**: Each connective is fully characterized by its truth table. The next concept builds directly on this.
- **Logical Equivalence**: Two compound propositions are logically equivalent if they have identical truth tables. Many important equivalences involve connectives — for example, $P \rightarrow Q \equiv \neg P \lor Q$.
- **Proof Techniques**: Each connective corresponds to a proof strategy. To prove $P \land Q$, prove both $P$ and $Q$. To prove $P \rightarrow Q$, assume $P$ and derive $Q$. To prove $P \leftrightarrow Q$, prove both directions. These correspondences will be made fully precise in Natural Deduction.
- **Naive Set Theory**: The connectives mirror set operations exactly — $\land$ corresponds to intersection ($\cap$), $\lor$ to union ($\cup$), $\neg$ to complement. This is not a coincidence.
- **Type Theory / Curry-Howard**: Each connective corresponds to a type constructor. $P \land Q$ corresponds to a product type, $P \lor Q$ to a sum type, $P \rightarrow Q$ to a function type. This is one of the deepest connections in the curriculum.

---

## Exercises

1. Let $P$ = "$n$ is odd" and $Q$ = "$n$ is divisible by $3$." Translate the following into plain English:
   - a) $P \land Q$
   - b) $\neg P \rightarrow Q$
   - c) $P \leftrightarrow \neg Q$

a) n is odd and it is divisible by 3. b) if n is not odd, then it is divisible by 3. c) if and only if n is odd, then it is not divisible by 3.

2. Let $P$ be true and $Q$ be false. Evaluate:
   - a) $\neg P \lor Q$
   - b) $P \rightarrow Q$
   - c) $\neg(P \land Q)$
   - d) $\neg P \rightarrow \neg Q$

a) False. b) False. c) True. d) True.

3. "If it is raining then the ground is wet." Identify the hypothesis and conclusion. Under what conditions is this implication false?

Hypothesis is "It is raining." Conclusion is "the ground is wet." If it rained and the ground was not wet.

4. Give an example of a vacuously true implication using integers.

If 2<1, then 1<2.

5. Why is $P \rightarrow Q$ not the same as $Q \rightarrow P$? Give a mathematical example where one is true and the other is false.

It obvious from the truth table. There are just different. 
# Tautologies & Contradictions

## Intuition

Some propositions are true no matter what. "It is raining or it is not raining" is true regardless of the weather — you cannot construct a situation where it fails. Others are false no matter what. "It is raining and it is not raining" cannot possibly be true.

These are not interesting empirical facts about the world — they are facts about the *structure* of logic itself. **Tautologies** and **contradictions** are the logical extremes: propositions whose truth value is determined entirely by their form, not their content.

This matters because tautologies are the logical laws we can use unconditionally in any proof, and contradictions are what we aim to derive when using proof by contradiction.

---

## Formal Definitions

A proposition $P$ is a **tautology** if it is true under every possible assignment of truth values to its component variables. Written $\models P$.

A proposition $P$ is a **contradiction** (or **unsatisfiable**) if it is false under every possible assignment of truth values to its component variables.

A proposition that is neither a tautology nor a contradiction is called **contingent** — its truth value depends on the truth values of its components.

> Note: $P \equiv Q$ if and only if $P \leftrightarrow Q$ is a tautology. This connects logical equivalence directly to the concept of tautology.

---

## Propositional Schemata — A Clarification

The expressions in this note — $P \lor \neg P$, $P \land \neg P$, $P \rightarrow Q$ — are not propositions or predicates in the strict sense. They are **propositional schemata** (also called **propositional forms**).

The difference is in what the variables range over:

| Kind | Variables range over | Example |
|------|---------------------|---------|
| Predicate | Objects in a domain (integers, sets, ...) | "$n$ is prime", $n \in \mathbb{Z}$ |
| Propositional schema | Truth values $\{T, F\}$ | $P \lor \neg P$, where $P \in \{T, F\}$ |

When we write $P \lor \neg P$, the variable $P$ is a placeholder for *any proposition*. Substituting a specific proposition — say, "$7$ is prime" — gives a genuine proposition: "$7$ is prime $\lor$ $7$ is not prime."

A **tautology** is then precisely a propositional schema that produces a true proposition no matter which proposition you substitute for each variable. This is why truth tables work: checking all combinations of T and F for $P$, $Q$, $R$ is equivalent to checking all possible substitutions.

This distinction between propositional variables and object variables will be made fully precise when we reach **Formal Syntax vs. Semantics** and **First-Order Logic**.

---

## Examples of Tautologies

### Law of the Excluded Middle
$$P \lor \neg P$$

| $P$ | $\neg P$ | $P \lor \neg P$ |
|-----|---------|----------------|
| T | F | T |
| F | T | T |

Always true. Every proposition is either true or false.

### Non-Contradiction
$$\neg(P \land \neg P)$$

| $P$ | $\neg P$ | $P \land \neg P$ | $\neg(P \land \neg P)$ |
|-----|---------|-----------------|----------------------|
| T | F | F | T |
| F | T | F | T |

Always true. No proposition is both true and false.

### Hypothetical Syllogism
$$(P \rightarrow Q) \land (Q \rightarrow R) \rightarrow (P \rightarrow R)$$

Always true — if $P$ implies $Q$ and $Q$ implies $R$, then $P$ implies $R$. This is the transitivity of implication.

### Modus Ponens (as a tautology)
$$(P \land (P \rightarrow Q)) \rightarrow Q$$

Always true — if $P$ is true and $P$ implies $Q$, then $Q$ must be true.

---

## Examples of Contradictions

### Explicit Contradiction
$$P \land \neg P$$

Always false — the truth table above shows this directly.

### Any Tautology, Negated
$$\neg(P \lor \neg P)$$

Since $P \lor \neg P$ is always true, its negation is always false.

---

## Examples of Contingent Propositions

$$P \rightarrow Q$$

True in three out of four rows — neither always true nor always false. Its truth depends on $P$ and $Q$.

$$P \land Q$$

True only when both are true — contingent.

---

## Why Contradictions Matter for Proofs

Proof by contradiction works as follows: to prove $P$, assume $\neg P$ and derive a contradiction. The contradiction shows that $\neg P$ is false — and since $P \lor \neg P$ is a tautology, $P$ must be true.

The formal structure is:

$$(\neg P \rightarrow \bot) \rightarrow P$$

where $\bot$ denotes a contradiction. This is itself a tautology.

---

## Why Tautologies Matter

Tautologies are propositions we can assert in any context, without any assumptions. They are the **logical axioms** — the free resources available in every proof. When a proof system is built, its axioms are typically tautologies, and its inference rules preserve truth.

---

## Connections

- **Truth Tables**: A tautology has all T in its final column. A contradiction has all F. Truth tables are the mechanical test.
- **Logical Equivalence**: $P \equiv Q$ iff $P \leftrightarrow Q$ is a tautology. Equivalence and tautology are two sides of the same coin.
- **Proof by Contradiction**: Contradictions are the target of this proof technique. Deriving $\bot$ from an assumption means the assumption must be false.
- **Law of the Excluded Middle**: $P \lor \neg P$ is a tautology — but in **intuitionistic logic** (the logic underlying Type Theory and Lean), this is not taken as an axiom. This is one of the first places where classical and constructive logic diverge, and it has deep consequences in Type Theory.
- **Natural Deduction**: $\bot$ (contradiction) is a formal symbol in Natural Deduction. It has an elimination rule: from $\bot$, anything follows. This rule is called **ex falso quodlibet** — "from falsity, anything."
- **Soundness & Completeness**: A sound proof system only proves tautologies. A complete proof system proves *all* tautologies. These two properties together ensure the proof system captures exactly the logical truths.

---

## Exercises

1. Is $P \rightarrow P$ a tautology? Verify with a truth table.

2. Is $(P \rightarrow Q) \rightarrow (\neg P \rightarrow \neg Q)$ a tautology? Verify with a truth table. What does this tell you about the relationship between an implication and its inverse?

3. Is $P \land (P \rightarrow Q) \rightarrow Q$ a tautology? What proof rule does this correspond to?

4. Construct a contradiction using only $P$, $Q$, and the connectives $\land$ and $\neg$ — different from $P \land \neg P$.

5. **Constructive logic** is a style of logic where a proposition is only considered true if you can *explicitly construct* a proof of it. This contrasts with **classical logic**, where a proposition is true if it simply cannot be false — even if no one can exhibit a proof.

   In classical logic, to prove $P \lor Q$ it is enough to show that $\neg P \rightarrow Q$ — i.e., if $P$ is not true then $Q$ must be. You do not need to say *which* of $P$ or $Q$ is true.

   In constructive logic, to prove $P \lor Q$ you must either:
   - explicitly produce a proof of $P$, or
   - explicitly produce a proof of $Q$.

   You cannot simply rule out the alternative.

   With this in mind: why is the Law of the Excluded Middle ($P \lor \neg P$) potentially problematic in constructive logic? Consider a proposition $P$ whose truth value is currently unknown — such as Goldbach's Conjecture. What would it mean to constructively prove $P \lor \neg P$ in that case?
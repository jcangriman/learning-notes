    # Logical Equivalence

## Intuition

Two propositions can look completely different on the surface but always have the same truth value no matter what. For example, "it is not the case that it is raining and sunny" and "it is not raining or it is not sunny" say the same thing — they agree in every possible situation. 

**Logical equivalence** is the formal way of capturing this idea. It is one of the most practically useful concepts in logic, because it lets us *rewrite* propositions into more convenient forms without changing their meaning. This is the logical analogue of algebraic simplification.

---

## Formal Definition

Two propositions $P$ and $Q$ are **logically equivalent**, written $P \equiv Q$, if they have identical truth values under every possible assignment of truth values to their component variables.

Equivalently: $P \equiv Q$ if and only if $P \leftrightarrow Q$ is a tautology.

> Important distinction: $P \equiv Q$ is a *meta-level* statement about two propositions. It is not itself a proposition inside the logic — it is a claim about the logic. The biconditional $P \leftrightarrow Q$ is a proposition inside the logic. They are related but not the same thing.

---

## The Named Equivalences

These are the fundamental logical equivalences. They are named laws and will be used throughout the rest of the curriculum.

### Double Negation
$$\neg \neg P \equiv P$$

### De Morgan's Laws
$$\neg(P \land Q) \equiv \neg P \lor \neg Q$$
$$\neg(P \lor Q) \equiv \neg P \land \neg Q$$

Negation distributes over conjunction and disjunction — but it flips $\land$ to $\lor$ and vice versa.

### Implication as Disjunction
$$P \rightarrow Q \equiv \neg P \lor Q$$

Implication can always be rewritten as a disjunction. This is used constantly in proofs.

### Contrapositive
$$P \rightarrow Q \equiv \neg Q \rightarrow \neg P$$

An implication is equivalent to its contrapositive. This is the logical foundation of proof by contrapositive.

### Biconditional as Double Implication
$$P \leftrightarrow Q \equiv (P \rightarrow Q) \land (Q \rightarrow P)$$

### Commutativity
$$P \land Q \equiv Q \land P$$
$$P \lor Q \equiv Q \lor P$$

### Associativity
$$(P \land Q) \land R \equiv P \land (Q \land R)$$
$$(P \lor Q) \lor R \equiv P \lor (Q \lor R)$$

### Distributivity
$$P \land (Q \lor R) \equiv (P \land Q) \lor (P \land R)$$
$$P \lor (Q \land R) \equiv (P \lor Q) \land (P \lor R)$$

### Idempotence
$$P \land P \equiv P$$
$$P \lor P \equiv P$$

### Identity Laws
$$P \land \top \equiv P$$
$$P \lor \bot \equiv P$$

### Absorption
$$P \land \bot \equiv \bot$$
$$P \lor \top \equiv \top$$

---

## How to Verify an Equivalence

The mechanical method is to build truth tables for both sides and check that the final columns are identical.

**Example**: Verify $\neg(P \land Q) \equiv \neg P \lor \neg Q$.

| $P$ | $Q$ | $P \land Q$ | $\neg(P \land Q)$ | $\neg P$ | $\neg Q$ | $\neg P \lor \neg Q$ |
|-----|-----|------------|------------------|---------|---------|---------------------|
| T | T | T | F | F | F | F |
| T | F | F | T | F | T | T |
| F | T | F | T | T | F | T |
| F | F | F | T | T | T | T |

The columns for $\neg(P \land Q)$ and $\neg P \lor \neg Q$ are identical — so they are logically equivalent. ✅

---

## Counterexamples

- $P \rightarrow Q$ is **not** equivalent to $Q \rightarrow P$. These are called the **converse** of each other. As we noted in Concept 8, they can have different truth values.
- $P \rightarrow Q$ is **not** equivalent to $\neg P \rightarrow \neg Q$ (the **inverse**). 
- However, $P \rightarrow Q$ **is** equivalent to $\neg Q \rightarrow \neg P$ (the **contrapositive**).

This gives us a useful table:

| Name | Form | Equivalent to $P \rightarrow Q$? |
|------|------|----------------------------------|
| Original | $P \rightarrow Q$ | Yes (trivially) |
| Converse | $Q \rightarrow P$ | No |
| Inverse | $\neg P \rightarrow \neg Q$ | No |
| Contrapositive | $\neg Q \rightarrow \neg P$ | Yes |

---

## Connections

- **Truth Tables**: Logical equivalence is verified by comparing truth table columns. The definition is inseparable from the truth table method.
- **Tautologies & Contradictions**: $P \equiv Q$ iff $P \leftrightarrow Q$ is a tautology. The concepts are deeply linked.
- **Proof by Contrapositive**: The equivalence $P \rightarrow Q \equiv \neg Q \rightarrow \neg P$ is the logical justification for this proof technique.
- **Natural Deduction**: Equivalences can be used as rewrite rules inside proofs — substituting one form for an equivalent one at any step.
- **De Morgan's Laws in Set Theory**: De Morgan's laws have direct analogues for sets: $\overline{A \cap B} = \bar{A} \cup \bar{B}$ and $\overline{A \cup B} = \bar{A} \cap \bar{B}$. This is not a coincidence — it reflects the deep connection between logic and set theory.
- **Type Theory**: In type theory, logical equivalence corresponds to the existence of an isomorphism between two types — a pair of functions going back and forth that are inverses of each other.

---

## Exercises

1. Use a truth table to verify that $P \rightarrow Q \equiv \neg P \lor Q$.

2. Use a truth table to verify the contrapositive law: $P \rightarrow Q \equiv \neg Q \rightarrow \neg P$.

3. Are $P \rightarrow Q$ and $Q \rightarrow P$ logically equivalent? Verify with a truth table.

4. Simplify the following using the named equivalences (do not use truth tables — use the laws as rewrite rules):
   - a) $\neg(\neg P \lor Q)$
   - b) $\neg(P \rightarrow Q)$

5. The following argument is made: "I proved $P \rightarrow Q$, so I have also proved $Q \rightarrow P$." What is wrong with this reasoning?
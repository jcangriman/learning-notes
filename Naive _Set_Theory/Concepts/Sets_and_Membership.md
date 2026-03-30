# Sets & Membership

## Intuition

Mathematics deals with collections constantly — the collection of all even numbers, the collection of all prime numbers less than 100, the collection of all solutions to an equation. A **set** is the most primitive way of talking about a collection in mathematics.

The key idea is that a set is defined entirely by its **members** — the objects it contains. Two sets are the same if and only if they contain exactly the same objects. Nothing else matters — not the order, not how the set was described, not whether the same object appears "multiple times." Only membership.

---

## Formal Definitions

A **set** is an unordered collection of distinct objects. The objects in a set are called its **elements** or **members**.

If $a$ is an element of a set $A$, we write:
$$a \in A$$
Read: "$a$ is in $A$" or "$a$ is a member of $A$."

If $a$ is not an element of $A$, we write:
$$a \notin A$$

**Extensionality**: Two sets $A$ and $B$ are equal if and only if they have exactly the same elements:
$$A = B \iff \forall x,\ x \in A \leftrightarrow x \in B$$

This is the defining principle of sets — identity is determined entirely by membership.

---

## Ways to Define a Set

### Roster Notation
List the elements explicitly inside curly braces:
$$A = \{1, 2, 3, 4\}$$
$$B = \{2, 4, 6, 8, 10\}$$

### Set Builder Notation
Describe the elements by a property they satisfy:
$$A = \{x \in \mathbb{Z} \mid x > 0 \text{ and } x < 5\}$$
Read: "the set of all integers $x$ such that $x > 0$ and $x < 5$."

The vertical bar $\mid$ (or sometimes $:$) means "such that." The expression to the left specifies the type of object, and the expression to the right specifies the condition it must satisfy.

---

## Special Sets

**The Empty Set** $\emptyset$ (also written $\{\}$) is the set with no elements. For every object $x$:
$$x \notin \emptyset$$

It is unique — there is only one empty set, by extensionality.

**Standard Number Sets**:
- $\mathbb{N} = \{0, 1, 2, 3, \ldots\}$ — natural numbers
- $\mathbb{Z} = \{\ldots, -2, -1, 0, 1, 2, \ldots\}$ — integers
- $\mathbb{Q}$ — rational numbers (fractions)
- $\mathbb{R}$ — real numbers

---

## Examples

| Statement | True or False? |
|-----------|---------------|
| $3 \in \{1, 2, 3, 4\}$ | True |
| $5 \in \{1, 2, 3, 4\}$ | False |
| $0 \in \mathbb{N}$ | True (by our convention) |
| $-1 \in \mathbb{N}$ | False |
| $-1 \in \mathbb{Z}$ | True |
| $\emptyset \in \{\emptyset\}$ | True — the empty set is an element of this set |
| $\{1, 2, 3\} = \{3, 1, 2\}$ | True — order does not matter |
| $\{1, 1, 2\} = \{1, 2\}$ | True — repetition does not matter |

---

## Counterexamples & Common Mistakes

- **Order does not matter**: $\{1, 2, 3\} = \{3, 2, 1\}$. Sets are unordered.
- **Repetition does not matter**: $\{1, 1, 2\} = \{1, 2\}$. Each element either is or is not in the set — it cannot appear "twice."
- **$\emptyset$ vs $\{\emptyset\}$**: The empty set $\emptyset$ has no elements. The set $\{\emptyset\}$ has exactly one element — the empty set itself. These are different.
- **$\in$ is not $\subseteq$**: Membership ($\in$) is a relation between an *object* and a set. Subset ($\subseteq$) is a relation between two *sets*. We will define $\subseteq$ in the next concept, but do not conflate them.

---

## Sets vs. Predicates

Set builder notation makes the connection between sets and predicates explicit. The set:
$$\{x \in \mathbb{Z} \mid P(x)\}$$
is the collection of all integers for which the predicate $P(x)$ is true. Every set can be thought of as the extension of a predicate, and every predicate (over a given domain) defines a set.

This connection runs deep — in some foundations of mathematics, sets *are* predicates. This becomes relevant in Type Theory, where the analogue of a set is a type, and membership is replaced by type inhabitation.

---

## Connections

- **Propositions & Predicates**: "$a \in A$" is a proposition for specific $a$ and $A$. "$x \in A$" with free variable $x$ is a predicate.
- **Logical Connectives**: Set operations (coming soon) mirror logical connectives exactly — union mirrors $\lor$, intersection mirrors $\land$, complement mirrors $\neg$.
- **Subsets**: The next concept — defined in terms of membership and the universal quantifier $\forall$.
- **Functions & Relations**: Defined as special kinds of sets — membership is the primitive notion everything else builds on.
- **Type Theory**: In type theory, the role of sets is played by **types**. The membership relation $a \in A$ corresponds to the typing judgment $a : A$ — "$a$ has type $A$." This is one of the central analogies in the curriculum.

---

## Exercises

1. Let $A = \{1, 2, 3\}$ and $B = \{3, 2, 1\}$. Is $A = B$? Justify using extensionality.

2. Write the following set in roster notation: $\{x \in \mathbb{N} \mid x \text{ is even and } x < 10\}$.

3. Write the following set in set builder notation: $\{1, 4, 9, 16, 25\}$. (Hint: what do these numbers have in common?)

4. Is $\emptyset \in \emptyset$? Is $\emptyset \in \{\emptyset\}$? Explain both.

5. Is the following true or false? $\{x \in \mathbb{Z} \mid x^2 = 4\} = \{2, -2\}$. Justify your answer.

6. Consider the set $\{x \in \mathbb{Z} \mid x \neq x\}$. What set is this equal to, and why?
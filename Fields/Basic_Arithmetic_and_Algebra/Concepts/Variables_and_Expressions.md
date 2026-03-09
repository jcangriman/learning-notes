# Variables & Expressions

## Intuition

Throughout the previous concepts, we have been quietly using variables without formally defining them. We wrote $n = 2k$, $a \mid b$, $p = a \times b$ — and you understood intuitively what was meant. Now we make this precise.

A **variable** is a placeholder — a name that stands in for an unspecified element of some collection. The collection it ranges over is called its **domain**. This is a simple idea, but it is the bridge between arithmetic (which talks about specific numbers) and logic (which talks about *all* numbers, or *some* numbers, or *what happens when* a number has a certain property).

Without variables, every statement would be about a specific number. With variables, we can make statements about entire collections at once.

---

## Formal Definitions

A **variable** is a symbol (typically $n$, $k$, $x$, $y$, $a$, $b$, ...) that represents an unspecified element of a given **domain**.

The **domain** of a variable is the set of values it is allowed to take. We always specify this explicitly — for example, "let $n \in \mathbb{Z}$" means $n$ is a variable whose domain is the integers.

An **expression** is a combination of variables, constants, and operations that represents a value. Examples: $2k + 1$, $a \times b$, $n^2 - 1$.

A **predicate** (or **open formula**) is a statement containing one or more variables whose truth value depends on what values those variables take.

- $P(n)$: "$n$ is even" — true when $n = 4$, false when $n = 3$.
- $Q(a, b)$: "$a \mid b$" — true when $a = 2, b = 6$, false when $a = 3, b = 7$.

A predicate becomes a **proposition** (with a definite truth value) in two ways:
1. **Substitution** — replace the variable with a specific value: $P(4)$ is the proposition "4 is even," which is true.
2. **Quantification** — bind the variable with $\forall$ or $\exists$: "for all $n$, $n$ is even or $n$ is odd" is a proposition (and a true one). We will formalize quantifiers later.

---

## Examples

| Expression | Type | Notes |
|------------|------|-------|
| $2k + 1$ | Expression | Represents a value — depends on $k$ |
| "$n$ is odd" | Predicate | True or false depending on $n$ |
| "$7$ is odd" | Proposition | Substituted $n = 7$ — definitely true |
| "$a \mid b$" | Predicate | Depends on both $a$ and $b$ |
| "$2 \mid 6$" | Proposition | Substituted $a = 2, b = 6$ — true |
| "for all $n \in \mathbb{Z}$, $n + 0 = n$" | Proposition | Quantified — definitely true |

---

## Substitution

When we substitute a value $v$ for a variable $x$ in an expression or predicate, we replace every occurrence of $x$ with $v$.

For example, if $P(n)$ is the predicate "$n^2 - 1 = (n-1)(n+1)$":
- $P(3)$ becomes "$3^2 - 1 = (3-1)(3+1)$", i.e., "$8 = 8$" — true.
- $P(0)$ becomes "$0^2 - 1 = (0-1)(0+1)$", i.e., "$-1 = -1$" — true.

This is the same operation we performed in all our divisibility proofs — we introduced a variable $k$ as a witness, then used it in expressions.

---

## Counterexamples

- A variable without a specified domain is ambiguous. Writing "$n$ is prime" means something different if $n \in \mathbb{Z}$ versus $n \in \mathbb{N}$ (negative integers are neither prime nor composite).
- An expression like $2k + 1$ is **not** a proposition — it has no truth value, only a numeric value depending on $k$.
- Substituting a value outside the domain is a type error — if $n \in \mathbb{Z}$, substituting $n = 2.5$ is not valid.

---

## Connections

- **Propositions & Truth Values**: A predicate is not yet a proposition. Substitution or quantification is what converts it into one.
- **Quantifiers ($\forall$, $\exists$)**: These are the formal tools for binding variables and producing propositions from predicates. Everything we have written informally ("for all integers $n$...", "there exists $k$ such that...") will be made precise with quantifiers.
- **Type Theory**: In type theory, every variable has a **type** — a precise specification of its domain. The notion of a variable ranging over a domain is directly formalized as a typed variable. This is one of the deepest connections in our entire curriculum.
- **Proof Techniques**: Every proof we have written introduced variables with explicit domains ("let $n \in \mathbb{Z}$") and witnesses ("there exists $k$ such that $n = 2k$"). These are applications of substitution and existential quantification.

---

## Exercises

1. Let $P(n)$ be the predicate "$n^2$ is even." What is $P(3)$? What is $P(4)$? Are these predicates or propositions?
P(3) = 9 which is false, P(4) = 16 which is true. They are propositions. 
2. Let $Q(a, b)$ be the predicate "$a \mid b$." Write out $Q(3, 12)$ and $Q(4, 9)$ as explicit propositions and determine their truth values.
3 | 12 = True, 4 | 9 = False. 
3. Consider the expression $2k + 1$ with domain $k \in \mathbb{Z}$. Is this expression a predicate, a proposition, or neither? What kind of object does it produce when you substitute $k = 5$?
Neither. 11 which is a integer. 
4. What is the difference between the predicate "$n$ is prime" and the proposition "$7$ is prime"?
Predicate depends on n to determine its true value. Proposition is just the truth value true. 
5. We have been writing things like "let $k \in \mathbb{Z}$ such that $n = 2k$" throughout our proofs. Identify the variable, its domain, and the predicate in that phrase.
Variable is k. Domain is integers. Predicate is that n is equal to k multiplied by 2. In a way n is a variable, but it remains fixed to whatever k ends up being so it is not exactly a normal variable. 
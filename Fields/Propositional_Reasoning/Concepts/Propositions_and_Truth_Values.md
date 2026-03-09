# Propositions & Truth Values

## Intuition

Mathematics is built on *statements*. But not all statements are equal. Some sentences make a definite claim about the world — they are either true or false. Others are questions, commands, or open-ended expressions that do not have a truth value at all.

Logic is the study of *reasoning* — and to reason formally, we need to be precise about what kinds of sentences we are reasoning about. The concept of a **proposition** draws the boundary: it separates the sentences logic can work with from those it cannot.

---

## Formal Definitions

A **proposition** (also called a **statement**) is a declarative sentence that has exactly one **truth value** — either **true** (written $T$ or $\top$) or **false** (written $F$ or $\bot$).

This rests on two foundational principles:

**Law of the Excluded Middle**: Every proposition is either true or false — there is no middle ground.

**Law of Non-Contradiction**: No proposition is both true and false simultaneously.

Together these ensure that every proposition has *exactly one* truth value.

A **predicate** is a sentence containing one or more free variables. It is not yet a proposition — its truth value depends on what values the variables take. It becomes a proposition either by **substitution** (replacing variables with specific values) or by **quantification** (binding variables with $\forall$ or $\exists$).

---

## Examples

| Sentence | Proposition? | Truth Value |
|----------|-------------|-------------|
| "$2 + 2 = 4$" | Yes | True |
| "$2 + 2 = 5$" | Yes | False |
| "Every even number $> 2$ is the sum of two primes" | Yes | Unknown — but still a proposition |
| "There are infinitely many prime numbers" | Yes | True |
| "$n$ is even" | No — predicate | Depends on $n$ |
| "Close the door" | No — command | No truth value |
| "Is it raining?" | No — question | No truth value |

---

## Unknown Truth Values

A sentence can be a proposition even if its truth value has not been determined. What matters is that it *has* a truth value — not that we have discovered it.

**Goldbach's Conjecture** — "every even integer greater than $2$ is the sum of two primes" — has been unproven for over 280 years. It is nevertheless a proposition, because it makes a definite claim that is either true or false.

---

## Propositions vs. Predicates — Revisited

From Concept 6, we know that a predicate $P(n)$ becomes a proposition in two ways:

- **Substitution**: $P(7)$ — "$7$ is prime" — is a proposition with truth value *true*.
- **Quantification**: "for all $n \in \mathbb{Z}$, $n$ is even or $n$ is odd" — is a proposition with truth value *true*.

The sentence "$n$ is prime" on its own is neither true nor false — it is waiting for $n$ to be resolved.

---

## Notation

We use letters $P$, $Q$, $R$ (sometimes $A$, $B$, $C$) to denote arbitrary propositions, especially when we want to reason about their structure without caring about their specific content.

---

## Counterexamples

- **The Liar Paradox**: "This sentence is false." If it is true, then it is false. If it is false, then it is true. This sentence violates the Law of Non-Contradiction and is therefore **not a proposition** — it is not a well-formed declarative statement in our logical system.
- **Vague sentences**: "This number is large" — without a precise definition of "large," this has no definite truth value and is not a proposition.

---

## Connections

- **Predicates & Variables**: A predicate is a proposition with free variables. This connection runs through the entire curriculum.
- **Logical Connectives**: Propositions are the raw material that connectives ($\land$, $\lor$, $\neg$, $\rightarrow$, $\leftrightarrow$) combine into compound propositions.
- **Truth Tables**: Once we have propositions and connectives, truth tables let us systematically compute the truth value of any compound proposition.
- **Type Theory**: In type theory, propositions are identified with **types**, and truth values are replaced by the question of whether a type is **inhabited** (has a proof term) or not. The Law of the Excluded Middle becomes a non-trivial axiom rather than a given.

---

## Exercises

1. Which of the following are propositions? For those that are, state their truth value (or say it is unknown):
   - a) "$4$ is divisible by $2$"
   - b) "$x + 1 = 3$"
   - c) "There exists an integer $n$ such that $n^2 = 2$"
   - d) "Multiply both sides by $2$"
   - e) "The product of two odd integers is odd"

2. We proved in Concept 4 that "the product of two odd integers is odd." Is this sentence a proposition or a predicate? What makes it different from "$n$ is odd"?

3. Consider the sentence "This sentence is false." Why does it fail to be a proposition? Which of the two foundational laws does it violate?

4. Give an example of a proposition whose truth value is currently unknown (other than Goldbach's Conjecture).
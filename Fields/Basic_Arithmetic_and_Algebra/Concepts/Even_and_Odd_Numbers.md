# Even & Odd Numbers

## Intuition

Even and odd are probably the most familiar mathematical concepts you have — you've known them since childhood. But here we do something important: we stop relying on intuition ("even numbers are 0, 2, 4, 6...") and instead give a **precise definition** in terms of divisibility. This is a small but significant shift — it means we can now *prove* things about even and odd numbers, rather than just recognizing them.

---

## Formal Definitions

Let $n \in \mathbb{Z}$.

**$n$ is even** if $2 \mid n$, i.e., there exists an integer $k$ such that:
$$n = 2k$$

**$n$ is odd** if $n$ is not even, i.e., there exists an integer $k$ such that:
$$n = 2k + 1$$

> Every integer is either even or odd — never both, never neither. This is our first example of a **partition**: two categories that are mutually exclusive and jointly exhaustive.

---

## Examples

| $n$ | Even or Odd? | Witness $k$ |
|-----|-------------|-------------|
| $0$ | Even | $k = 0$, since $0 = 2 \times 0$ |
| $4$ | Even | $k = 2$, since $4 = 2 \times 2$ |
| $-6$ | Even | $k = -3$, since $-6 = 2 \times (-3)$ |
| $7$ | Odd | $k = 3$, since $7 = 2(3) + 1$ |
| $-3$ | Odd | $k = -2$, since $-3 = 2(-2) + 1$ |

---

## Counterexamples

- $0$ is **even**, not neither — $0 = 2 \times 0$ is a valid witness.
- Negative integers are subject to the same definitions — $-3$ is odd, $-4$ is even.
- There is no integer that is both even and odd — if $n = 2j$ and $n = 2k+1$, then $2j = 2k+1$, which gives $2(j-k) = 1$, meaning $2 \mid 1$ — but we can verify directly that no integer witness exists for that.

---

## Key Facts Worth Proving

These are standard results you will prove in the exercises:

- Even + Even = Even
- Odd + Odd = Even
- Even + Odd = Odd
- Even × Even = Even
- Odd × Odd = Odd
- Even × Odd = Even

---

## Connections

- **Divisibility**: Even/odd is a direct application of divisibility. Mastering these proofs is practice for divisibility proofs in general.
- **Proof by Contradiction**: The cleanest proof that no integer is both even and odd uses contradiction — assume it is both and derive an impossibility.
- **Propositional Reasoning**: "$n$ is even" is a proposition (for a fixed $n$). "$n$ is even or $n$ is odd" is a tautology — always true — which we will revisit when we study logical connectives.
- **Partitions & Set Theory**: Even and odd integers partition $\mathbb{Z}$ into two disjoint sets whose union is all of $\mathbb{Z}$. This is a preview of set-theoretic thinking.

---

## Exercises

1. Is $0$ even or odd? Provide the witness $k$.
0 is even. Witness is 0. 
2. Is $-7$ even or odd? Provide the witness $k$.
-7 is odd. Witness is -4. 
3. Prove that the sum of two even integers is even. (Use the definition — introduce witnesses for each, then find a witness for the sum.)
n = 2 * k
d = 2 * j 
n + d = 2 * k + 2 * j = 2 * (k + j)
k + j is the witness. n+d is even. 
4. Prove that the sum of two odd integers is even.
n = 2*k + 1
d = 2*j + 1 
n + d = 2*(k+j+1)
The sum of two odd integers is even. Witness is k+j+1.
5. Prove that the product of two odd integers is odd.
n = 2*k + 1
d = 2*j + 1 
n * d = 4kj + 2k + 2j + 1 = 2(2kj + k +j) + 1
Witness is 2kj + k + j. The product is an odd integer. 
6. Is the product of an even and an odd integer always even? Prove it.
n = 2*k + 1
d = 2*j 
n * d = 2(2kj + j)
witness is 2kj +j. Product of even and odd is even. 
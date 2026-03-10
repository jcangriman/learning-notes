# Prime Numbers

## Intuition

Some integers are "atomic" — they cannot be broken down into smaller factors. Others are "composite" — they are built by multiplying smaller pieces together. **Prime numbers** are the atoms of multiplication. Every integer can be built by multiplying primes together, and this decomposition is unique. This makes primes the fundamental building blocks of arithmetic.

But more importantly for us, the *definition* of a prime is a statement about divisibility — which means reasoning about primes is practice for the kind of precise, definition-driven proof writing we have been developing.

---

## Formal Definition

An integer $p$ is **prime** if:

1. $p > 1$, and
2. the only positive divisors of $p$ are $1$ and $p$ itself.

Equivalently, $p$ is prime if $p > 1$ and whenever $p = a \times b$ for positive integers $a, b$, then either $a = 1$ or $b = 1$.

An integer $n > 1$ that is **not** prime is called **composite**. It has at least one positive divisor other than $1$ and itself.

> The number $1$ is neither prime nor composite by convention. This is not arbitrary — it is chosen to make the Fundamental Theorem of Arithmetic (below) work cleanly.

---

## Examples

| $n$ | Prime? | Reason |
|-----|--------|--------|
| $2$ | Yes | Divisors are $1$ and $2$ only |
| $3$ | Yes | Divisors are $1$ and $3$ only |
| $4$ | No | $4 = 2 \times 2$, so $2$ is a divisor |
| $7$ | Yes | Divisors are $1$ and $7$ only |
| $15$ | No | $15 = 3 \times 5$ |
| $1$ | No | Excluded by definition |
| $2$ | Yes | The only even prime |

---

## The Fundamental Theorem of Arithmetic

Every integer $n > 1$ can be written as a product of primes, and this factorization is **unique** up to the order of the factors.

For example:
$$60 = 2 \times 2 \times 3 \times 5 = 2^2 \times 3 \times 5$$

This is called the **prime factorization** of $n$. We will not prove this theorem here, but it is worth knowing — it is the reason primes are considered the building blocks of arithmetic.

---

## Counterexamples

- $1$ is **not** prime — if it were, prime factorizations would not be unique ($6 = 2 \times 3 = 1 \times 2 \times 3 = 1 \times 1 \times 2 \times 3 \ldots$).
- $2$ is the **only even prime** — every other even number is divisible by $2$, giving it a divisor other than $1$ and itself.
- Not all odd numbers are prime — $9 = 3 \times 3$, $15 = 3 \times 5$, and so on.

---

## Infinitely Many Primes

There are infinitely many prime numbers. This is one of the oldest results in mathematics, proved by Euclid around 300 BC. The proof is a beautiful example of **proof by contradiction**, which we will study formally in Proof Techniques. For now, here is the sketch:

> Suppose there were only finitely many primes $p_1, p_2, \ldots, p_n$. Consider the number $N = (p_1 \times p_2 \times \cdots \times p_n) + 1$. Then $N$ is not divisible by any of $p_1, \ldots, p_n$ (dividing always leaves remainder $1$). So either $N$ is prime itself, or it has a prime factor not in our list. Either way, our list was incomplete — a contradiction.

---

## Connections

- **Divisibility**: Primality is defined entirely in terms of divisibility. A prime is precisely an integer whose only divisors are trivial.
- **Proof by Contradiction**: Euclid's proof of infinitely many primes is the canonical first example of this technique.
- **Propositional Reasoning**: "$n$ is prime" is a proposition for any fixed $n$. "There exist infinitely many primes" is also a proposition — and a true one.
- **Variables & Expressions**: The definition of prime uses the universal pattern "for all $a, b$, if $p = a \times b$ then..." — our first informal encounter with the universal quantifier $\forall$.

---

## Exercises

1. Is $49$ prime? Justify using the definition.
7*7 = 49. 
2. Is $2$ the only even prime? Prove it. (Hint: what does it mean for a number greater than $2$ to be even, in terms of divisibility?)
Lets say p is prime, p > 2, and it is also even. So p = 2*k. That means p is divisble by 2. Therefore p is not a prime. 
3. List all prime numbers less than $20$.
2, 3, 5, 7, 11, 13, 17, 19
4. What is the prime factorization of $84$?
84 = 2^2 * 3 * 7
5. Why is $1$ excluded from the definition of prime? What would go wrong if we allowed $1$ to be prime?
If prime was included, prime factorizations would not be unique. 
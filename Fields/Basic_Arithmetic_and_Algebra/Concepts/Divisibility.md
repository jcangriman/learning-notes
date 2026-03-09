# Divisibility

## Intuition

We saw that division does not always stay inside the integers — $7 \div 2 = 3.5$ escapes $\mathbb{Z}$. But sometimes division *does* produce a whole number: $6 \div 2 = 3$. The question **divisibility** asks is simply: *when does this happen?*

Instead of asking "what is $a \div b$?", we ask "does $b$ divide $a$ evenly, with nothing left over?" This shift — from computing an answer to asking a yes/no question — is our first step toward thinking like a logician.

---

## Formal Definition

Let $a, b \in \mathbb{Z}$ with $b \neq 0$.

We say **$b$ divides $a$**, written $b \mid a$, if there exists an integer $k$ such that:

$$a = b \times k$$

If $b$ divides $a$, we also say:
- $b$ is a **divisor** (or **factor**) of $a$
- $a$ is a **multiple** of $b$

If no such $k$ exists, we write $b \nmid a$ and say $b$ **does not divide** $a$.

> Important: The notation $b \mid a$ is a **proposition** — it is either true or false. It is not the same as $a / b$, which is a number. This distinction matters.

---

## Examples

| Statement | $k$ witness | True or False? |
|-----------|-------------|----------------|
| $2 \mid 6$ | $k = 3$, since $6 = 2 \times 3$ | True |
| $3 \mid 12$ | $k = 4$, since $12 = 3 \times 4$ | True |
| $5 \mid 0$ | $k = 0$, since $0 = 5 \times 0$ | True |
| $2 \mid 7$ | No integer $k$ satisfies $7 = 2 \times k$ | False |
| $n \mid n$ | $k = 1$, since $n = n \times 1$ | True for all $n \neq 0$ |
| $1 \mid n$ | $k = n$, since $n = 1 \times n$ | True for all $n$ |

---

## Key Properties of Divisibility

Let $a, b, c \in \mathbb{Z}$. The following hold:

**Reflexivity**: $a \mid a$ for all $a \neq 0$.

**Transitivity**: If $a \mid b$ and $b \mid c$, then $a \mid c$.

**Linearity**: If $a \mid b$ and $a \mid c$, then $a \mid (b + c)$.

More generally: if $a \mid b$ and $a \mid c$, then $a \mid (bx + cy)$ for any integers $x, y$.

---

## Counterexamples

- $2 \mid 7$ is **false** — there is no integer $k$ with $7 = 2k$. Note $k = 3.5$ is not an integer.
- Divisibility is **not symmetric**: $2 \mid 6$ but $6 \nmid 2$.
- $0 \mid a$ is **never true** for $a \neq 0$ — we would need $a = 0 \times k = 0$, a contradiction.

---

## Connections

- **Even & Odd Numbers**: Directly defined using divisibility — $n$ is even if and only if $2 \mid n$.
- **Prime Numbers**: Defined in terms of which numbers have no divisors other than $1$ and themselves.
- **Proof Techniques**: Divisibility proofs are among the first places where the technique of direct proof is applied — you prove $b \mid a$ by explicitly constructing the witness $k$.
- **Propositional Reasoning**: The statement $b \mid a$ is a proposition. The definition "there exists $k$ such that $a = bk$" is our first informal encounter with the existential quantifier $\exists$, which we will formalize later.

---

## Exercises

1. Is $4 \mid 20$? If so, what is the witness $k$?
Yes. 5.
2. Is $6 \mid 15$? Justify your answer.
No. 6 * 3 = 18, 6* 2 = 12. There is no integer that multiplied by 6 would produce 15. 6 multiplied by numbers higher than 3 would produce numbers higher than 15, and 6 multiplied by numbers below 2, would produce numbers below 15. 
3. Prove that if $a \mid b$ and $b \mid c$, then $a \mid c$. (Hint: write out what each divisibility statement means in terms of a witness integer, then combine them.)
a | b, b = a * k
b | c, c = b * y
a | c, c = b * y = (a * k) * y = a * (ky)
ky is the witness integer. 
4. Does $5 \mid 0$? Does $0 \mid 5$? Explain both.
5 divides 0. 0 = 5 * 0 = 0 
0 does not divide 5. 5 /= 0 * k = 0
5. If $a \mid b$, does it follow that $a \mid (b + a)$? Justify your answer.
a | b , b = a * k
b + a = a * k + a = a * (k + 1)
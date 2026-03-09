# Basic Operations

## Intuition

Once you have numbers, the next question is: *what can you do with them?* The basic operations — addition, subtraction, multiplication, and division — are the fundamental ways of combining numbers to produce new ones. But beyond just computing answers, what matters for logic and proof is understanding the **properties** these operations obey. Those properties are what we reason *about* when we write proofs.

---

## Formal Definitions

Let $a, b, c$ be integers.

**Addition** ($+$): Combines two numbers into their sum. $a + b = c$ means $c$ is the total of $a$ and $b$.

**Subtraction** ($-$): $a - b$ is the unique integer $c$ such that $b + c = a$.

**Multiplication** ($\times$ or $\cdot$): Repeated addition. $a \times b$ means $a$ added to itself $b$ times (for positive $b$).

**Division** ($\div$ or $/$ ): $a \div b$ is the number $c$ such that $b \times c = a$. 

> Critical point: Division does not always produce an integer. $7 \div 2 = 3.5$, which is not in $\mathbb{Z}$. This is why division is treated separately and motivates the concept of **divisibility**.

---

## Key Properties

These properties hold for addition and multiplication over the integers:

**Commutativity**
$$a + b = b + a$$
$$a \times b = b \times a$$
Order does not matter.

**Associativity**
$$(a + b) + c = a + (b + c)$$
$$(a \times b) \times c = a \times (b \times c)$$
Grouping does not matter.

**Distributivity**
$$a \times (b + c) = (a \times b) + (a \times c)$$
Multiplication distributes over addition.

**Identity Elements**
- $a + 0 = a$ — zero is the additive identity.
- $a \times 1 = a$ — one is the multiplicative identity.

**Additive Inverse**
- For every integer $a$, there exists $-a$ such that $a + (-a) = 0$.

---

## Closure

An important concept: a set is **closed** under an operation if applying that operation to elements of the set always produces another element of the set.

| Operation | Closed over $\mathbb{N}$? | Closed over $\mathbb{Z}$? |
|-----------|--------------------------|--------------------------|
| Addition | Yes | Yes |
| Subtraction | No ($0 - 1 = -1 \notin \mathbb{N}$) | Yes |
| Multiplication | Yes | Yes |
| Division | No | No |

---

## Examples

- $3 + 5 = 8$ — addition of naturals, result is a natural.
- $3 - 5 = -2$ — subtraction of integers, result is an integer but not a natural.
- $4 \times (-3) = -12$ — multiplication of integers.
- $7 \div 2 = 3.5$ — division escapes $\mathbb{Z}$ entirely.

---

## Counterexamples

- Subtraction is **not** commutative: $5 - 3 \neq 3 - 5$.
- Division is **not** associative: $(8 \div 4) \div 2 = 1$ but $8 \div (4 \div 2) = 4$.
- Division by zero is **undefined** — there is no integer $c$ such that $0 \times c = 7$.

---

## Connections

- **Divisibility**: Directly motivated by the failure of division to close over $\mathbb{Z}$. We ask instead: *when does division produce a whole number?*
- **Even & Odd Numbers**: Defined using multiplication — $n$ is even if $n = 2 \times k$ for some integer $k$.
- **Variables & Expressions**: Properties like commutativity are our first examples of statements that hold *for all* integers — a pattern that will become the universal quantifier $\forall$ in logic.
- **Proof Techniques**: Many early proofs are just careful applications of these properties in sequence.

---

## Exercises

1. Is subtraction commutative? Give a counterexample if not.
It is not. 2 - 1 = 1, 1 - 2 = -1 
2. Is subtraction associative? Give a counterexample if not.
Yes. 
3. Using only the properties listed above, explain why $a \times 0 = 0$ for any integer $a$. (Hint: think about what $0$ is in terms of addition, and apply distributivity.)
a x 0 = a x ( 0 x 0) = (ax0) + (ax0)
(ax0) - (ax0) = ax0 
0 = ax0
4. Is $\mathbb{N}$ closed under subtraction? Justify your answer.
The natural numbers are not closed under substraction. 1 - 2 creates an element -1 which is not in the natural number set. 
5. Which of the four operations is $\mathbb{Z}$ *not* closed under, and why?
Division. 1/2. There is not integer x, such that 2 * n = 1. 










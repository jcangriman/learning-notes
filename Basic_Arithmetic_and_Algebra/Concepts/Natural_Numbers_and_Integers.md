# Natural Numbers & Integers

## Intuition

Counting is the most primitive mathematical act. Before any algebra, before any logic, humans needed to answer the question: *how many?* The **natural numbers** are the answer to that question — they are the counting numbers.

But counting only gets you so far. Once you start asking questions like *"what do I have left after spending more than I own?"*, you need numbers that go below zero. That extension gives you the **integers**.

These two collections — naturals and integers — are the universe in which almost all of our early examples in logic and proof will live.

---

## Formal Definitions

**The Natural Numbers** are the set of non-negative whole numbers:

$\mathbb{N} = \{0, 1, 2, 3, 4, \ldots\}$

> Note: Some definitions start $\mathbb{N}$ at 1 rather than 0. We include 0 here, which is the more common convention in logic and type theory.

**The Integers** extend the natural numbers by including all negative whole numbers:

$\mathbb{Z} = \{\ldots, -3, -2, -1, 0, 1, 2, 3, \ldots\}$

The symbol $\mathbb{Z}$ comes from the German word *Zahlen*, meaning "numbers."

Every natural number is an integer, but not every integer is a natural number. In other words, $\mathbb{N} \subseteq \mathbb{Z}$ (we will make this "subset" notation precise later).

---

## The Number Line

The integers can be visualized as evenly spaced points on a line, extending infinitely in both directions:

```
← . . . -3  -2  -1   0   1   2   3 . . . →
```

The natural numbers occupy the right half, starting at 0.

---

## Examples

| Number | Natural? | Integer? |
|--------|----------|----------|
| 0 | Yes | Yes |
| 7 | Yes | Yes |
| -4 | No | Yes |
| 2.5 | No | No |
| 1000000 | Yes | Yes |

---

## Counterexamples

- $2.5$ is **not** an integer — integers are whole numbers only.
- $-1$ is **not** a natural number — naturals do not go below zero.
- There is **no largest** natural number or integer — both collections are infinite.

---

## Connections

- **Basic Operations**: Addition, subtraction, and multiplication of integers always produce integers. Division does not always — this tension motivates the study of divisibility.
- **Variables & Expressions**: When we write $n$ as a variable ranging over integers, we mean $n$ could be *any* element of $\mathbb{Z}$. The concept of a variable only makes sense once you have a clear collection for it to range over.
- **Even & Odd Numbers**: Defined in terms of integers and divisibility — coming soon.
- **Propositional Reasoning**: Many of our first logical examples will use statements like "let $n$ be an integer" — you need to know what that means.

---

## Exercises

1. Is $0$ a natural number? Is it an integer? (Note: think carefully — the answer depends on the convention, and we stated ours above.)
It is a natural number and an integer. 
2. Give an example of an integer that is not a natural number.
-1
3. Is the collection of integers finite or infinite? How do you know?
Infinite. Integers contain natural numbers which we already know are infinite. 
4. If $n$ is a natural number, is $n - 1$ always a natural number? What about $n - 1$ always being an integer?
n -1 is not always a natural number. 0 - 1 is -1 which is an integer. 
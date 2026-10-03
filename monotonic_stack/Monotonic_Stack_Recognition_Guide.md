# Monotonic Stack Recognition Guide

## What is a Monotonic Stack?

A **monotonic stack** is just a normal stack where the elements are
always maintained in either:

-   **Monotonically Increasing** order
-   **Monotonically Decreasing** order

Whenever a new element breaks that order, we pop elements until the
order is restored.

------------------------------------------------------------------------

# How to Recognize a Monotonic Stack Problem

Instead of memorizing problems, use this checklist.

## ✅ 1. Look for "Next" or "Previous"

If the problem asks for:

-   Next Greater Element
-   Next Smaller Element
-   Previous Greater Element
-   Previous Smaller Element

A monotonic stack is one of the first approaches you should consider.

Examples:

-   739. Daily Temperatures
-   496. Next Greater Element I
-   503. Next Greater Element II
-   901. Online Stock Span

------------------------------------------------------------------------

## ✅ 2. Look for "Nearest" or "First"

Keywords such as:

-   nearest
-   first
-   closest

Examples:

-   First greater element to the right
-   Nearest smaller element on the left

These are classic monotonic stack signals.

------------------------------------------------------------------------

## ✅ 3. Every Element Needs Information About Its Neighbors

If the problem says:

> For every element...

and then asks about:

-   the next greater element
-   the next smaller element
-   the previous greater element
-   the previous smaller element

it's a strong indication that a monotonic stack may help.

------------------------------------------------------------------------

## ✅ 4. Your Brute Force Uses Nested Loops

If your first solution looks like:

``` python
for i in range(n):
    for j in range(i + 1, n):
        if arr[j] > arr[i]:
            ...
```

you're repeatedly scanning left or right for every element.

Ask yourself:

> Can I remember useful candidates using a stack instead?

Many O(n²) solutions become O(n).

------------------------------------------------------------------------

## ✅ 5. Some Elements Become Permanently Useless

This is the strongest clue.

Example:

    73 74 75

Once you process **75**, the temperature **74** can never be the answer
for any element further left because **75 is both closer (from the left
element's perspective) and warmer**.

Whenever you realize:

> "Once I see this element, some previous candidates become useless
> forever."

think **Monotonic Stack**.

------------------------------------------------------------------------

# Compare With Other Patterns

## Two Pointers

Typical clues:

-   Sorted array
-   Two ends
-   Move left/right pointers

Examples:

-   Two Sum II
-   Container With Most Water

------------------------------------------------------------------------

## Sliding Window

Typical clues:

-   Subarray
-   Substring
-   Contiguous window

Keywords:

-   longest
-   shortest
-   at most K
-   exactly K

------------------------------------------------------------------------

## Heap (Priority Queue)

Typical clues:

-   Top K
-   Largest K
-   Smallest K
-   Highest priority

------------------------------------------------------------------------

## Binary Search

Typical clues:

-   Minimum possible
-   Maximum possible
-   First True
-   Last False

------------------------------------------------------------------------

## Monotonic Stack

Typical clues:

-   Next
-   Previous
-   Nearest
-   First greater
-   First smaller
-   Span
-   Visibility

------------------------------------------------------------------------

# Mental Model

When solving a problem, ask:

> **"If I already knew everything to my right (or left), what
> information would I want to keep?"**

Answer:

Only the elements that can still be useful.

The monotonic stack stores exactly those useful candidates and removes
everything that has become permanently useless.

------------------------------------------------------------------------

# Practice Problems (Recommended Order)

1.  496. Next Greater Element I
2.  739. Daily Temperatures
3.  503. Next Greater Element II
4.  901. Online Stock Span
5.  402. Remove K Digits
6.  84. Largest Rectangle in Histogram

------------------------------------------------------------------------

# Interview Checklist

Before coding, ask yourself:

-   Does every element need information about elements to its left or
    right?
-   Is it asking for the **nearest** or **first** greater/smaller
    element?
-   Does my brute-force solution scan left or right for every element?
-   Can some elements become permanently useless once a better candidate
    appears?

If the answer is **Yes** to two or more of these questions, seriously
consider using a **Monotonic Stack**.

------------------------------------------------------------------------

# Golden Rule

> **Don't recognize the stack. Recognize the relationship between
> elements.**

If the problem is fundamentally about finding the **nearest
greater/smaller element**, the monotonic stack is often the right tool.

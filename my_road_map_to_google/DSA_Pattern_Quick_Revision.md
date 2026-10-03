# DSA Pattern Quick Revision — Google L4

> **17 problems | HashMap / HashSet / Sliding Window / Two Pointers**

| # | Problem + LeetCode Link | General Intuition | Time Complexity | Difficulty |
|---:|---|---|---|:---:|
| 1 | [Contains Duplicate — LC 217](https://leetcode.com/problems/contains-duplicate/) | **HashSet:** keep values seen so far. If `x in seen`, duplicate found; otherwise add `x`. | **O(n)** avg. | 🟢 Easy |
| 2 | [Valid Anagram — LC 242](https://leetcode.com/problems/valid-anagram/) | **Frequency HashMap:** store `character → count`. Anagrams must have identical frequency for every character. | **O(n)** | 🟢 Easy |
| 3 | [Two Sum — LC 1](https://leetcode.com/problems/two-sum/) | **Complement + HashMap:** for current `x`, look for `target-x` among previous values. Store `value → index`. | **O(n)** avg. | 🟢 Easy |
| 4 | [Ransom Note — LC 383](https://leetcode.com/problems/ransom-note/) | **Frequency consumption:** count available characters, then decrement counts while consuming the ransom note. | **O(m+n)** | 🟢 Easy |
| 5 | [Majority Element — LC 169](https://leetcode.com/problems/majority-element/) | **Frequency:** count `value → frequency` and return the value whose count exceeds `n//2`. Boyer-Moore can reduce space to O(1). | **O(n)** | 🟢 Easy |
| 6 | [Group Anagrams — LC 49](https://leetcode.com/problems/group-anagrams/) | **HashMap grouping:** create a canonical frequency signature for each word and use `signature → list of words`. | **O(n·k)** | 🟡 Medium |
| 7 | [Top K Frequent Elements — LC 347](https://leetcode.com/problems/top-k-frequent-elements/) | **Frequency + Buckets:** count frequencies, place each value in `bucket[frequency]`, then scan buckets from high to low. | **O(n)** | 🟡 Medium |
| 8 | [Longest Consecutive Sequence — LC 128](https://leetcode.com/problems/longest-consecutive-sequence/) | **HashSet + sequence start:** only start when `n-1` is absent; then keep checking `n+1`. This avoids rescanning from the middle. | **O(n)** avg. | 🟡 Medium |
| 9 | [Contains Duplicate II — LC 219](https://leetcode.com/problems/contains-duplicate-ii/) | **Value → latest index:** when a duplicate appears, check `i-last[x] <= k`, then update `last[x] = i`. | **O(n)** avg. | 🟢 Easy |
| 10 | [Isomorphic Strings — LC 205](https://leetcode.com/problems/isomorphic-strings/) | **Two-way mapping:** maintain `s→t` and `t→s` so the mapping is one-to-one in both directions. | **O(n)** | 🟢 Easy |
| 11 | [Subarray Sum Equals K — LC 560](https://leetcode.com/problems/subarray-sum-equals-k/) | **Prefix Sum + frequency:** current prefix `S` needs an earlier prefix `S-k`. Store `prefix_sum → frequency` and add its count to the answer. | **O(n)** avg. | 🟡 Medium |
| 12 | [Happy Number — LC 202](https://leetcode.com/problems/happy-number/) | **Cycle detection:** repeatedly transform the number; use a HashSet of states. Reaching `1` is success; seeing a state again means a cycle. | **O(log n)** per transformation; bounded states | 🟢 Easy |
| 13 | [Valid Sudoku — LC 36](https://leetcode.com/problems/valid-sudoku/) | **Multiple Sets:** maintain seen values for each row, column, and 3×3 box. Reject if a value already exists in any relevant set. | **O(1)** for 9×9 | 🟡 Medium |
| 14 | [4Sum II — LC 454](https://leetcode.com/problems/4sum-ii/) | **Pair-sum precomputation:** rewrite `(A+B)+(C+D)=0`. Store `A+B → frequency`; for each `C+D`, lookup `-(C+D)`. | **O(n²)** | 🟡 Medium |
| 15 | [Longest Substring Without Repeating Characters — LC 3](https://leetcode.com/problems/longest-substring-without-repeating-characters/) | **Sliding Window + HashMap:** maintain a window of unique characters. Store `char → latest index`; on duplicate, jump `left` past its previous index. | **O(n)** | 🟡 Medium |
| 16 | [3Sum — LC 15](https://leetcode.com/problems/3sum/) | **Sort + Two Pointers:** fix one value, then find the remaining pair with `left/right`. Sum too small → `left++`; too large → `right--`; skip duplicates. | **O(n²)** | 🟡 Medium |
| 17 | [4Sum — LC 18](https://leetcode.com/problems/4sum/) | **Sort + Two Pointers:** fix two values, then two-pointer the remaining pair. Sorting makes pointer movement valid; skip duplicates at every level. | **O(n³)** | 🟡 Medium |

---

## Pattern Recognition — 10 Second Checklist

| Signal | Pattern / Data Structure |
|---|---|
| **Have I seen this value before?** | HashSet |
| **How many times does it occur?** | HashMap → frequency |
| **Where did I see it?** | HashMap → index |
| **What value do I need to complete the target?** | HashMap → complement |
| **Group things with the same property** | HashMap → signature/group |
| **Count subarrays with target sum** | Prefix Sum + HashMap frequency |
| **Repeatedly transform a state** | HashSet → cycle detection |
| **Contiguous subarray/substring with a property** | Sliding Window |
| **Sorted array + pair/triplet/quadruplet** | Two Pointers |
| **Four separate arrays + equation** | Pair-sum precomputation + HashMap |

---

## Core Mental Models

### HashMap
**Remember information about the past so the current element can be answered in O(1) average time.**

### HashSet
**Remember what has already appeared when you only care about existence, uniqueness, or repeated states.**

### Prefix Sum
**Turn a subarray-sum question into a difference between two prefix sums.**

### Sliding Window
**Maintain a valid contiguous window; expand right, and when the invariant breaks, move left until it becomes valid again.**

### Two Pointers
**Sorting creates order. Use that order to decide whether moving `left` or `right` makes the sum closer to the target.**

### Precomputation
**Calculate reusable information once, store it, and avoid repeating the same work.**

---

## Google L4 Revision Rule

For every problem, before coding, be able to answer:

1. **What pattern is this?**
2. **What is my invariant?**
3. **What exactly am I storing?**
4. **Why does this eliminate repeated work?**
5. **What is the time and space complexity?**
6. **What are the important edge cases / duplicate cases?**

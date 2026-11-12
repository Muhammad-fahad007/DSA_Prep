# FAANG DSA Pattern Tree

Use this as a pattern-first roadmap for SWE interview preparation.

```text
DSA
│
├── 1. Arrays & Strings  (DONE) Pass-1
│   ├── Two Pointers
│   │   ├── Opposite-direction pointers
│   │   ├── Same-direction pointers
│   │   └── Read / write pointers
│   ├── Sliding Window
│   │   ├── Fixed-size window
│   │   └── Variable-size window
│   ├── Prefix Sum
│   │   ├── 1D Prefix Sum
│   │   ├── Prefix Sum + HashMap
│   │   └── 2D Prefix Sum
│   ├── Kadane's Algorithm
│   ├── Sorting + Scan
│   ├── Frequency Counting
│   └── Matrixf
│       ├── Traversal
│       ├── Rotation
│       ├── Spiral
│       └── Grid Simulation 

│
├── 2. Hashing (DONE) Pass 1
│   ├── HashMap
│   ├── HashSet
│   ├── Frequency Map
│   ├── Complement Lookup
│   ├── Grouping
│   └── Prefix Sum + HashMap
│
├── 3. Linked List
│   ├── Fast & Slow Pointers
│   │   ├── Cycle Detection
│   │   ├── Find Middle
│   │   └── Cycle Starting Point
│   ├── Dummy Node
│   ├── Reversal
│   │   ├── Entire List
│   │   ├── Partial List
│   │   └── K-Group Reversal
│   ├── Two Pointers
│   │   └── Kth Node From End
│   └── Merge
│       ├── Two Sorted Lists
│       └── K Sorted Lists
│
├── 4. Stack
│   ├── Monotonic Stack
│   │   ├── Next Greater
│   │   ├── Next Smaller
│   │   ├── Previous Greater / Smaller
│   │   └── Histogram Problems
│   ├── Parentheses / Matching
│   ├── Expression Evaluation
│   └── Simulation
│
├── 5. Queue / Deque
│   ├── BFS Queue
│   ├── Level-Order Processing
│   └── Monotonic Queue
│       └── Sliding Window Maximum
│
├── 6. Binary Search
│   ├── Classic Binary Search
│   ├── First / Last Occurrence
│   ├── Lower / Upper Bound
│   ├── Rotated Sorted Array
│   ├── Search in Matrix
│   └── Binary Search on Answer
│       ├── Minimum Possible Value
│       └── Maximum Possible Value
│
├── 7. Trees
│   ├── DFS
│   │   ├── Preorder
│   │   ├── Inorder
│   │   └── Postorder
│   ├── BFS
│   │   └── Level Order
│   ├── Recursive Tree Patterns
│   │   ├── Height / Depth
│   │   ├── Diameter
│   │   ├── Balanced Tree
│   │   └── Path Problems
│   └── Lowest Common Ancestor
│
├── 8. Binary Search Tree (BST)
│   ├── BST Property
│   ├── Inorder = Sorted
│   ├── Search / Insert
│   ├── Validate BST
│   ├── Kth Smallest
│   └── Lowest Common Ancestor
│
├── 9. Heap / Priority Queue
│   ├── Top K
│   ├── Kth Largest / Smallest
│   ├── Merge K Sorted
│   ├── Scheduling
│   ├── Running Median
│   │   └── Two Heaps
│   └── Heap + HashMap
│
├── 10. Graphs
│   ├── DFS
│   │   ├── Connected Components
│   │   ├── Islands
│   │   └── Cycle Detection
│   ├── BFS
│   │   ├── Unweighted Shortest Path
│   │   ├── Level Traversal
│   │   └── Multi-Source BFS
│   ├── Topological Sort
│   │   ├── DFS Approach
│   │   └── Kahn's Algorithm
│   ├── Union-Find / DSU
│   │   ├── Connectivity
│   │   └── Cycle Detection
│   ├── Weighted Graph
│   │   ├── Dijkstra
│   │   ├── Bellman-Ford
│   │   └── Floyd-Warshall
│   └── Minimum Spanning Tree
│       ├── Prim
│       └── Kruskal
│
├── 11. Backtracking
│   ├── Subsets
│   ├── Permutations
│   ├── Combinations
│   ├── Combination Sum
│   ├── Grid / Word Search
│   ├── Palindrome Partitioning
│   └── Constraint Search
│       ├── N-Queens
│       └── Sudoku
│
├── 12. Intervals
│   ├── Merge Intervals
│   ├── Insert Interval
│   ├── Meeting Rooms
│   ├── Interval Scheduling
│   ├── Sort by Start / End
│   └── Sweep Line
│
├── 13. Greedy
│   ├── Local Optimal Choice
│   ├── Sort + Greedy
│   ├── Interval Greedy
│   ├── Jump Problems
│   ├── Scheduling
│   └── Resource Allocation
│
├── 14. Dynamic Programming
│   ├── 1D DP
│   │   ├── Fibonacci-style
│   │   ├── Climbing Stairs
│   │   ├── House Robber
│   │   ├── Take / Skip
│   │   └── Longest Increasing Subsequence
│   ├── Knapsack
│   │   ├── 0/1 Knapsack
│   │   └── Unbounded Knapsack
│   ├── String DP
│   │   ├── Longest Common Subsequence
│   │   ├── Edit Distance
│   │   └── Palindrome DP
│   └── 2D / Grid DP
│       ├── Unique Paths
│       ├── Min / Max Path
│       └── Grid State Transitions
│
├── 15. Bit Manipulation
│   ├── Check Bit
│   ├── Set Bit
│   ├── Clear Bit
│   ├── Toggle Bit
│   ├── AND / OR / XOR
│   ├── Count Set Bits
│   ├── Power of Two
│   ├── XOR Cancellation
│   ├── Brian Kernighan: n & (n - 1)
│   └── Bitmasking
│       └── Generate Subsets
│
├── 16. Trie
│   ├── Prefix Search
│   ├── Word Dictionary
│   └── Trie + DFS
│
├── 17. Math
│   ├── GCD / LCM
│   ├── Prime Numbers / Sieve
│   ├── Modular Arithmetic
│   └── Basic Combinatorics
│
└── 18. Advanced Data Structures
    ├── Union-Find
    ├── Trie
    ├── Segment Tree
    └── Fenwick Tree
```

## Recognition Cheatsheet

```text
Contiguous subarray / substring        -> Sliding Window / Prefix Sum
Sorted array                           -> Two Pointers / Binary Search
Pair / complement lookup               -> HashMap
Next greater / smaller                 -> Monotonic Stack
Cycle in linked list                   -> Fast & Slow Pointers
Kth from end of linked list            -> Two Pointers
Top K / Kth largest / smallest         -> Heap
Repeatedly need min / max              -> Heap
Tree level by level                    -> BFS
Tree path / subtree information        -> DFS / Recursion
Unweighted shortest path               -> BFS
Positive weighted shortest path        -> Dijkstra
Dependencies / ordering                -> Topological Sort
Connectivity / merging groups          -> Union-Find
All combinations / choices             -> Backtracking
Overlapping [start, end] ranges         -> Sort + Intervals
Optimization with repeated subproblems -> Dynamic Programming
Minimum/maximum feasible answer         -> Binary Search on Answer
Where do bits differ?                  -> XOR
```

## Priority

### Tier 1 — Master
Arrays & Strings, Hashing, Two Pointers, Sliding Window, Stack, Binary Search,
Linked Lists, Trees, BFS/DFS, Heap, Graphs.

### Tier 2 — Be Comfortable
Intervals, Backtracking, 1D DP, Greedy, Topological Sort, Union-Find,
Bit Manipulation.

### Tier 3 — Learn After the Core
2D DP, Trie, Dijkstra/MST, advanced graph algorithms, Segment Tree,
Fenwick Tree, advanced math.

## Interview Problem-Solving Flow

```text
New Problem
    ↓
Understand Input + Constraints
    ↓
Work Through Example
    ↓
Think of Brute Force
    ↓
Identify Bottleneck
    ↓
Recognize Pattern
    ↓
Derive Optimized Solution
    ↓
Explain Before Coding
    ↓
Code
    ↓
Test Edge Cases
    ↓
Time + Space Complexity
```


High priority
- HashMap / HashSet
- Arrays / Strings
- Two Pointers
- Sliding Window
- Binary Search
- Trees / BST
- Graphs
- Heap / Priority Queue
- BFS / DFS
- Dynamic Programming
- Intervals / Greedy
Medium priority
- Linked Lists
- Stack / Monotonic Stack
- Prefix Sum
- Backtracking
- Union Find
- Trie


Topic	Priority	What you should know
Arrays / HashMap / HashSet	🔴 Very High	Prefix sum, frequency, sorting, Kadane
Strings	🔴 Very High	Hashing, sliding window, parsing
Graphs	🔴 Very High	BFS, DFS, Dijkstra, Topo, DSU
Trees / BST	🔴 Very High	DFS/BFS, LCA, recursion, BST
Binary Search	🔴 Very High	Especially binary search on answer
DP	🔴 Very High	1D, 2D, subsequence, knapsack, state
Heap / Priority Queue	🟠 High	Top-K, scheduling, K-way merge, Dijkstra
Trie	🟠 High	Prefix, search, Trie + DFS
Intervals	🟠 High	Merge, overlap, scheduling
Sliding Window	🟠 High	Variable/fixed window
Two Pointers	🟠 High	Sorted arrays, pair/triplet problems
Stack	🟠 High	Parentheses, expression, simulationd
Monotonic Stack	🟠 High	Next greater/smaller, histogram
Queue / Deque	🟡 Medium	BFS, monotonic deque, sliding window
Linked List	🟡 Medium	Reverse, fast/slow, merge, cycle, LRU
Backtracking	🟡 Medium	Subsets, permutations, combinations, grid
Recursion	🟡 Medium	Tree/graph/backtracking foundation
Greedy	🟡 Medium-High	Intervals, scheduling, optimization
Bit Manipulation	🟡 Medium	XOR, masks, shifts, bit counting
Union Find	🟡 Medium	Connectivity, cycles, grouping
Math / Probability	🟡 Medium	Counting, probability, observations
Matrix	🟡 Medium	Traversal, grid BFS/DFS
Segment Tree	🟢 Low	Know concept; don't grind
Fenwick Tree	🟢 Low	Awareness/basic problems
Advanced Graph	🟢 Low	MST etc. after fundamentals
Advanced DP	🟢 Low	Only after core DP is strong
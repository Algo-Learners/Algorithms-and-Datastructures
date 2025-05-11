# Introduction to Big-O notation
Big-O notation is a mathematical concept used in computer science to describe the performance or complexity of an algorithm, especially in terms of time and space as the input size grows.

What Big-O actually measure is that as the size of the input grows, how does that affect 
the performance of the algorithm (how much does the algorithm slow down).

## Why Is Big-O Important?

  [x] Helps compare algorithms.

  [x] Predicts how an algorithm scales with larger inputs.

  [x] Highlights bottlenecks in performance.


## What Does Big-O Measure?

   [x] Time Complexity – How long an algorithm takes to run.

   [x] Space Complexity – How much memory an algorithm uses.



## Common Big-O Time Complexities

| Big-O      | Name             | Example                                        |
| ---------- | ---------------- | ---------------------------------------------- |
| O(1)       | Constant time    | Accessing an array element by index            |
| O(log n)   | Logarithmic time | Binary search                                  |
| O(n)       | Linear time      | Loop through array                             |
| O(n log n) | Linearithmic     | Merge sort, quicksort (average case)           |
| O(n²)      | Quadratic time   | Nested loops, bubble sort                      |
| O(2ⁿ)      | Exponential time | Solving the traveling salesman via brute-force |
| O(n!)      | Factorial time   | Generating all permutations                    |

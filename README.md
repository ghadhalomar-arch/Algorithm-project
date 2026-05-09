# ATM Change-Making Algorithms Project

This project implements and compares three different algorithmic approaches to solve the "Change-Making Problem": finding the minimum number of banknotes required to make up a specific amount.

## Implemented Algorithms

### 1. Greedy Algorithm
The Greedy approach always selects the largest possible banknote denomination at each step until the total amount is reached.
*   **How it works:** It makes the "locally optimal" choice at each stage.
*   **Pros:** Extremely fast and simple to implement.
*   **Cons:** It might not always provide the absolute minimum number of notes for all currency systems, though it works for most standard ones.

### 2. Brute Force Algorithm
This algorithm explores every possible combination of banknotes to find the one that results in the minimum count.
*   **How it works:** It uses nested loops to iterate through all possible quantities of each denomination (500, 100, 50, 10, 5, 1).
*   **Pros:** Guaranteed to find the optimal (mathematically best) solution.
*   **Cons:** Very inefficient for large amounts due to high computational complexity (Exponential time).

### 3. Dynamic Programming (DP)
Dynamic Programming solves the problem by breaking it down into smaller sub-problems and storing their results in a table to avoid redundant calculations.
*   **How it works:** It builds a table (2D array) representing the minimum notes needed for every amount from 0 up to the target.
*   **Pros:** Always finds the optimal solution with much better performance than Brute Force.
*   **Cons:** Requires additional memory (Space Complexity) to store the DP table.

---

## Comparison Table

| Feature | Greedy Algorithm | Brute Force | Dynamic Programming |
| :--- | :--- | :--- | :--- |
| **Speed (Efficiency)** | Very Fast ($O(n)$) | Very Slow (Exponential) | Efficient ($O(n \times m)$) |
| **Optimality** | Not always optimal | Always optimal | Always optimal |
| **Logic** | Simple / Direct | Exhaustive Search | Sub-problem Solving |
| **Best Use Case** | Standard Currencies | Tiny amounts only | Complex/Ideal systems |

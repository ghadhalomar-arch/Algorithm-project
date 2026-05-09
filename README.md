# ATM Change-Making Algorithms Project

This project implements and compares three different algorithmic approaches to solve the "Change-Making Problem": finding the minimum number of banknotes required to make up a specific amount.

## Implemented Algorithms

### 1. Greedy Algorithm
The Greedy approach always selects the largest possible banknote denomination at each step until the total amount is reached.
*   **How it works:** It makes the "locally optimal" choice at each stage.
*   **Pros:** Extremely fast and simple to implement.
*   **Cons:** It might not always provide the absolute minimum number of notes for all currency systems.

### 2. Brute Force Algorithm
This algorithm explores every possible combination of banknotes to find the one that results in the minimum count.
*   **How it works:** It uses nested loops to iterate through all possible quantities of each denomination.
*   **Pros:** Guaranteed to find the optimal solution.
*   **Cons:** Extremely inefficient for large amounts due to the nested loop structure.

### 3. Dynamic Programming (DP)
Dynamic Programming solves the problem by breaking it down into smaller sub-problems and storing their results in a table.
*   **How it works:** It builds a 2D table to compute the value of the optimal solution for each sub-amount.
*   **Pros:** Always finds the optimal solution with much better performance than Brute Force.
*   **Cons:** Requires additional memory to store the DP table.

---

## Comparison Table

| Feature | Greedy Algorithm | Brute Force | Dynamic Programming |
| :--- | :--- | :--- | :--- |
| **Time Complexity** | $O(n)$ | $O(n^k)$ | $O(n)$ |
| **Optimality** | Not always optimal | Always optimal | Always optimal |
| **Logic** | Simple / Direct | Exhaustive Search | Sub-problem Solving |
| **Best Use Case** | Standard Currencies | Small amounts only | Complex/Ideal systems |

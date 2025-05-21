# LeetCode-Problems
Mothers Day and Fathers Day Challenge problems

# 🚀 LeetCode 119 - Pascal's Triangle II
## Problem Description
Given an integer `rowIndex`, return the `rowIndex`-th (0-indexed) row of Pascal's Triangle.
In Pascal’s Triangle, each number is the sum of the two numbers directly above it.
### Example:
Input: rowIndex = 3
Output: [1, 3, 3, 1]

## Approach
We start with the first element `1` and iteratively build each row using the previous values.  
We update the list in reverse order to avoid overwriting values.

## Key Takeaways
Pascal's Triangle builds from previous rows.
Reverse traversal helps avoid overwriting values while updating.

# 🚀Leetcode 678 - Valid Parenthesis String
## Problem Statement
Given a string `s` containing only three types of characters: `'('`, `')'`, and `'*'`, return `true` if `s` is **valid**.
### A valid string must follow these rules:
- Every `'('` must have a corresponding `')'`.
- Every `')'` must have a corresponding `'('`.
- `'('` must appear before the corresponding `')'`.
- `'*'` can be treated as `'('`, `')'`, or an empty string `""`.
- 
## Examples
Input: s = "()"
Output: true
## Approach
We use a **Greedy** strategy to keep track of the **range** of possible open parentheses at any point:
### Steps:
1. Iterate through each character in the string.
2. Update `minOpen` and `maxOpen` based on character:
   - `'('`: increment both
   - `')'`: decrement both
   - `'*'`: decrement `minOpen`, increment `maxOpen`
3. If at any point `maxOpen < 0`, return `false`.
4. If `minOpen` drops below 0, reset it to 0.
5. After the loop, return `true` if `minOpen == 0`.

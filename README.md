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

# Approach

Finding the two minimum numbers in an array can be approached in several ways, ranging from brute force to more efficient algorithms. Here are some of these approaches:

## 1. Brute Force Approach

The brute force approach involves sorting the entire array and then picking the first two elements as the smallest. However, this method is inefficient for large arrays due to its high time complexity of O(n log n) for sorting.

## 2. Optimal Approach

The optimal approach is similar to the simple iterative method but ensures that we handle edge cases more efficiently. It requires only one pass through the array, making it O(n).

### Algorithm:

- Initialize `min1` and `min2` with the first element and `INT_MAX`, respectively.
- Iterate through the array starting from the second element:
  - If an element is smaller than `min1`, update `min2` to the old `min1` and update `min1`.
  - If an element is between `min1` and `min2`, update `min2`.

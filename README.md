# LeetCode 209 - Minimum Size Subarray Sum

## Problem Description

Given an array of positive integers `nums` and a positive integer `target`, find the minimum length of a contiguous subarray whose sum is greater than or equal to `target`.

If no such subarray exists, return `0`.

## Example

Input:

target = 7
nums = [2,3,1,2,4,3]

The subarray `[4,3]` has a sum of `7` and its length is `2`.

Output:

2

## Approach

We use the **Sliding Window** technique.

Two pointers, `left` and `right`, are used to represent the current window.

We expand the window by moving `right` and adding elements to `current_sum`.

When the sum becomes greater than or equal to `target`, we try to shrink the window from the left while keeping the sum valid.

For every valid window, we update the minimum length.

Since all numbers are positive, removing elements from the left will always decrease the sum, which makes the sliding window approach efficient.

## Algorithm

1. Initialize `left` as `0`.
2. Keep track of the current window sum.
3. Move `right` through the array and add each value to the sum.
4. When the sum is at least `target`, update the minimum length.
5. Remove the leftmost element and move `left` forward.
6. Continue until the complete array is processed.
7. Return the minimum length, or `0` if no valid subarray exists.

## Time Complexity

**O(n)**

Each element is added to and removed from the sliding window at most once.

## Space Complexity

**O(1)**

Only a few variables are used apart from the input array.

## Key Concepts

- Sliding Window
- Two Pointers
- Arrays
- Subarrays
- Optimization

## Author

T.nandhini

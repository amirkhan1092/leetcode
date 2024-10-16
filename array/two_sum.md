# Two Sum

**Problem Link**: [Two Sum](https://leetcode.com/problems/two-sum)

## Problem Description:
Given an array of integers `nums` and an integer `target`, return the indices of the two numbers that add up to the target.

## Approach:
- Use a HashMap to store each element and its index.
- For each element `num`, compute `target - num`.
- If the difference exists in the map, return the current index and the index from the map.
- Time complexity: O(n)

## Solution (Python):
```python
def twoSum(nums, target):
    num_map = {}
    for i, num in enumerate(nums):
        if target - num in num_map:
            return [num_map[target - num], i]
        num_map[num] = i

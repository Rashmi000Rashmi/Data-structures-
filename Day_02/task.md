- Date: 24 Aug 2024
# Question 1: 
### Duplicate Integer
Two Integer Sum
Given an array of integers nums and an integer target, return the indices i and j such that nums[i] + nums[j] == target and i != j.

You may assume that every input has exactly one pair of indices i and j that satisfy the condition.

Return the answer with the smaller index first.

Example 1:

Input: 
nums = [3,4,5,6], target = 7

Output: [0,1]
Explanation: nums[0] + nums[1] == 7, so we return [0, 1].

### Example 2:

Input: nums = [4,5,6], target = 10

Output: [0,2]
### Example 3:

Input: nums = [5,5], target = 10

Output: [0,1]
### Constraints:

2 <= nums.length <= 1000
-10,000,000 <= nums[i] <= 10,000,000
-10,000,000 <= target <= 10,000,000
 

## Link : https://neetcode.io/problems/two-integer-sum

# Question 2: 
### Anagram Groups

Given an array of strings strs, group all anagrams together into sublists. You may return the output in any order.

An anagram is a string that contains the exact same characters as another string, but the order of the characters can be different.

### Example 1:

Input: strs = ["act","pots","tops","cat","stop","hat"]

Output: [["hat"],["act", "cat"],["stop", "pots", "tops"]]
### Example 2:

Input: strs = ["x"]

Output: [["x"]]
### Example 3:

Input: strs = [""]

Output: [[""]]
### Constraints:

1 <= strs.length <= 1000.
0 <= strs[i].length <= 100
strs[i] is made up of lowercase English letters.




## Link : https://neetcode.io/problems/anagram-groups

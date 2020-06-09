---
layout: page
title:  "Leetcode Notes"
subtitle: "By Yi"
date:   2020-06-09 14:47:21 +0530
categories: Note
---

# Linked List
## 344. Reverse String

Write a function that reverses a string. The input string is given as an array of characters char[].

Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

You may assume all the characters consist of printable ascii characters.
<br>

### Approach 1: Recursion, In-Place, \mathcal{O}(N)O(N) Space
```python
class Solution:
    def reverseString(self, s):
        def helper(left, right):
            if left < right:
                s[left], s[right] = s[right], s[left]
                helper(left + 1, right - 1)

        helper(0, len(s) - 1)
```
# Freshman-Immigration-LeetCode-Problems


### Reverse String
* Problem link: https://leetcode.com/problems/reverse-string/

```python
class Solution(object):
    def reverseString(self, s):
        l = 0
        r = len(s) - 1
        while l < r:
            s[l], s[r] = s[r], s[l]
            l += 1
            r -= 1
```





### Two Sum
* **Problem Link:** [LeetCode - Two Sum](https://leetcode.com/problems/two-sum/)

```python
class Solution(object):
    def twoSum(self, nums, target):
        for i in range(0, len(nums)):
            for j in range(i + 1, len(nums)):
                if nums[i] + nums[j] == target:
                    return [i, j]
```





### Longest Common Prefix
* **Problem Link:** [LeetCode - Longest Common Prefix](https://leetcode.com/problems/longest-common-prefix/)

```python
class Solution(object):
    def longestCommonPrefix(self, strs):
        ans = ""
        st = strs[0]
        for i in range(1, len(strs)):
            if len(strs[i]) < len(st):
                st = strs[i]

        for i in range(0, len(st)):
            ch = st[i]
            
            for j in range(0, len(strs)):
                if strs[j][i] != ch:
                    return ans
            ans += ch
        return ans
```

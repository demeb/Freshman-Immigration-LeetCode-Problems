# Freshman-Immigration-LeetCode-Problems

reverse-string problem:

class Solution(object):
    def reverseString(self, s):
        l = 0
        r = len(s)-1
        while l < r:
            a = s[l]
            b = s[r]
            s[l] = b
            s[r] = a
            l += 1
            r -= 1

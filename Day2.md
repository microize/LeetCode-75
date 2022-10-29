205. Isomorphic Strings
https://leetcode.com/problems/isomorphic-strings/

Given two strings s and t, determine if they are isomorphic.

Two strings s and t are isomorphic if the characters in s can be replaced to get t.

All occurrences of a character must be replaced with another character while preserving the order of characters. No two characters may map to the same character, but a character may map to itself.

 

Example 1:

Input: s = "egg", t = "add"
Output: true
Example 2:

Input: s = "foo", t = "bar"
Output: false
Example 3:

Input: s = "paper", t = "title"
Output: true

Solution:

class Solution:
    def isIsomorphic(self, s: str, t: str) -> bool:
        dic_s = {}
        dic_t = {}

        for s1,t1 in zip(s,t):
            if (s1 in dic_s and dic_s[s1]!=t1) or (t1 in dic_t and dic_t[t1]!=s1):
                return False
            dic_s[s1]=t1
            dic_t[t1]=s1
        return True
        
**************************************************
**************************************************

392. Is Subsequence
https://leetcode.com/problems/is-subsequence

Given two strings s and t, return true if s is a subsequence of t, or false otherwise.

A subsequence of a string is a new string that is formed from the original string by deleting some (can be none) of the characters without disturbing the relative positions of the remaining characters. (i.e., "ace" is a subsequence of "abcde" while "aec" is not).

 

Example 1:

Input: s = "abc", t = "ahbgdc"
Output: true

Example 2:

Input: s = "axc", t = "ahbgdc"
Output: false

Solution:

class Solution:
    def isSubsequence(self, s: str, t: str) -> bool:
        p1=0
        p2=0
        while p1<len(s) and p2<len(t):
            if s[p1]==t[p2]:
                p1+=1
                p2+=1
            else:
                p2+=1
        if p1==len(s):
            return True
        return False

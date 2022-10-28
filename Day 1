1480. Running Sum of 1d Array
https://leetcode.com/problems/running-sum-of-1d-array/description/

Given an array nums. We define a running sum of an array as runningSum[i] = sum(nums[0]…nums[i]).
Return the running sum of nums.

Example 1:

Input: nums = [1,2,3,4]
Output: [1,3,6,10]
Explanation: Running sum is obtained as follows: [1, 1+2, 1+2+3, 1+2+3+4].

Solution 1:

class Solution:
    def runningSum(self, nums: List[int]) -> List[int]:
        return accumulate(nums)
        
Solution 2:       
class Solution:
    def runningSum(self, nums: List[int]) -> List[int]:
        sum_ele = 0
        out_lst =[]
        for ele in nums:
            sum_ele+=ele
            out_lst.append(sum_ele)
        return out_lst
        
**************************************************************************************
**************************************************************************************

724. Find Pivot Index

Given an array of integers nums, calculate the pivot index of this array.
The pivot index is the index where the sum of all the numbers strictly to the left of the index is equal to the sum of all the numbers strictly to the index's right.
If the index is on the left edge of the array, then the left sum is 0 because there are no elements to the left. This also applies to the right edge of the array.
Return the leftmost pivot index. If no such index exists, return -1.

 

Example 1:

Input: nums = [1,7,3,6,5,6]
Output: 3
Explanation:
The pivot index is 3.
Left sum = nums[0] + nums[1] + nums[2] = 1 + 7 + 3 = 11
Right sum = nums[4] + nums[5] = 5 + 6 = 11
Example 2:

Input: nums = [1,2,3]
Output: -1
Explanation:
There is no index that satisfies the conditions in the problem statement.
Example 3:

Input: nums = [2,1,-1]
Output: 0
Explanation:
The pivot index is 0.
Left sum = 0 (no elements to the left of index 0)
Right sum = nums[1] + nums[2] = 1 + -1 = 0

Solution 1:

class Solution:
    def pivotIndex(self, nums: List[int]) -> int:
        left,total = 0,sum(nums)
        for ind,val in enumerate(nums):
            if left*2+val==total:
                return ind
            left+=val
        return -1

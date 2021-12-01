Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        for i in range(len(nums)):
            if target-nums[i] in nums[i+1:]:
                a = i
                b = [j for j, x in enumerate(nums[i+1:]) if x ==target-nums[i]][0] + i
                b = b+1
                break
        return [a, b]
```

Success
Details 
Runtime: 664 ms, faster than 36.49% of Python3 online submissions for Two Sum.
Memory Usage: 15.1 MB, less than 61.95% of Python3 online submissions for Two Sum.
Next challenges:
3Sum
4Sum
Two Sum II - Input Array Is Sorted
Two Sum III - Data structure design
Subarray Sum Equals K
Two Sum IV - Input is a BST
Two Sum Less Than K
Max Number of K-Sum Pairs
Count Good Meals
Count Number of Pairs With Absolute Difference K
Number of Pairs of Strings With Concatenation Equal to Target
Show off your acceptance:

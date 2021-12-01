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

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3c0e7e89-b343-4e8f-a718-06dc2e4c0889/Untitled.png)
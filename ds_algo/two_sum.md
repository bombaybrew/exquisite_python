## Two Sum

- Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target. 
- You may assume that each input would have exactly one solution, and you may not use the same element twice. 
- You can return the answer in any order.

###
```
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:

        result = [0, 1]

        nums_length = len(nums)
        
        for i in range(nums_length):
            for j in range(i+1, nums_length):
                if (nums[i] + nums[j] == target):
                    return[i, j]
    
        return result
```
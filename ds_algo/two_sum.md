## Two Sum

- Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target. 

###
```python
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

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:

        seen = {}
        
        for key, value in enumerate(nums):
            
            compliment = target-value
                
            if compliment in seen:
                return [key, seen[compliment]]
            
            seen[value] = key
            
        raise ValueError('No two sum solution found')
```

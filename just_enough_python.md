
## Loops

```python
nums = [0,1,2,3,4]

for num in nums:
  print(num)
  
for idx in range(len(nums)):
  print(num[idx])

for i in range(nums_length):
  for j in range(i+1, nums_length):
    if (nums[i] + nums[j] == target):
      return[i, j]
            
for key, val in enumerate(nums):
  print('key - ', key, ' value - ', val)
```

## Dict
```python
nums = [5,3,4]

print(dict(zip(nums, nums)))
# Output
{5: 5, 3: 3, 4: 4}

print(dict(zip(nums, list(range(len(nums))))))
# Output
{5: 0, 3: 1, 4: 2}
```

## Max
```python
max_num = max(max_num, 5)
```

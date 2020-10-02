## Longest Substring
- Given a string, find the length of the longest substring without repeating characters.

###
```python
class Solution:

    def lengthOfLongestSubstring(self, s: str) -> int:
        start_idx = 0
        sub_dict = {}
        max_length = 0
        
        for idx, val in enumerate(s):
            if (val in sub_dict) and (sub_dict[val] >= start_idx):
                start_idx = sub_dict[val] + 1
            else:
                max_length = max(max_length, idx - start_idx + 1)
            
            sub_dict[val] = idx
                    
        return max_length
```

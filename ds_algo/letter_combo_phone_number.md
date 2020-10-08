# Letter combination for phone number
- Given a string containing digits from 2-9 inclusive, return all possible letter combinations that the number could represent. Return the answer in any order.

```python
class Solution:
    
    def getCombo(self, combo_array, collector):
        result = []
        
        if not collector: return combo_array
        
        for letter in combo_array:
            for item in collector:
                result.append(item + letter)

        return result
        
    def letterCombinations(self, digits: str) -> List[str]:
        
        result = []
        
        digits_hash = {'2': ['a','b','c'], 
                       '3': ['d','e','f'], 
                       '4': ['g','h','i'], 
                       '5': ['j','k','l'],
                       '6': ['m','n','o'], 
                       '7': ['p','q','r','s'], 
                       '8': ['t','u','v'], 
                       '9': ['w','x','y','z']}
        
        for digit in digits:   
            result = self.getCombo(digits_hash[digit], result)
            
        return result
```

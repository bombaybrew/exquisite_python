# Pascal's Traingle

```python
class Solution:
    
    def calcRow(listResult: List[int]):

        listLen = len(listResult)
        result = [1]
        for i in range(listLen-1):
            result.append(listResult[i] + listResult[i+1])
        result.append(1)

        return result

    def getRow(self, rowIndex: int) -> List[int]:
        
        if rowIndex == 0:
            return [1]
        
        if rowIndex == 1:
            return [1, 1]
        
        return Solution.calcRow(self.getRow(rowIndex-1))
        
```

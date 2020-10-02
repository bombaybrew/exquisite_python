### Rotate Image
- Given an nxn 2D matrix representing an image, rotate the image by 90 degrees.

```python
class Solution:
    def rotate(self, matrix: List[List[int]]) -> None:
        
        m_size = len(matrix)
        limit = ceil(m_size/2)
        x_limit = m_size - 1
        
        print('size, limit', m_size, limit)
    
        for idx_x in range(limit):
            
            for idx_y in range(idx_x, x_limit - idx_x):
                print('x, y, limit, size ', idx_x, idx_y, limit, m_size)
                temp = matrix[idx_x][idx_y]
                matrix[idx_x][idx_y] = matrix[x_limit - idx_y][idx_x]
                matrix[x_limit - idx_y][idx_x] = matrix[x_limit - idx_x][x_limit - idx_y]
                matrix[x_limit - idx_x][x_limit - idx_y] = matrix[idx_y][x_limit - idx_x]
                matrix[idx_y][x_limit - idx_x] = temp

```

```python
class Solution:
    def rotate(self, matrix: List[List[int]]) -> None:

        m_size = len(matrix)
        # transpose
        for i in range(m_size - 1):
            for j in range(i, m_size):
                matrix[i][j], matrix[j][i] = matrix[j][i], matrix[i][j]
        # mirror
        for i in range(ceil(m_size/2)):
            for j in range(m_size):
                matrix[j][i], matrix[j][m_size - 1 - i] = matrix[j][m_size - 1 - i], matrix[j][i]
```

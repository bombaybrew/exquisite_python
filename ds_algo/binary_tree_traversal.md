## pre-order traversal
- root > left > right
```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right

class Solution:
    def preorderTraversal(self, root: TreeNode) -> List[int]:
        
        if not root: return
        result = []
        
        # add root
        result.append(root.val)
        
        # check left
        if root.left:
            result = result + self.preorderTraversal(root.left)
        
        # check right
        if root.right:
            result = result + self.preorderTraversal(root.right)
        
        return result
```

## in-order traversal
- left > root > right
```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right
        
class Solution:
    def inorderTraversal(self, root: TreeNode) -> List[int]:
        
        if not root: return
        result = []
        
        # left
        if root.left:
            result = result + self.inorderTraversal(root.left)
        
        # root
        result.append(root.val)
        
        # right
        if root.right:
            result = result + self.inorderTraversal(root.right)
            
        return result
```

## post-order traversal
- left > right > root

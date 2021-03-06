# Reverse a Linked List


### Iterative

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def reverseList(self, head: ListNode) -> ListNode:
        
        prevNode = None
        currNode = head
        
        while (currNode):
            tempNode = currNode.next
            currNode.next = prevNode
            prevNode = currNode
            currNode = tempNode
            
        return prevNode
```

### Recursive
```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def reverseList(self, head: ListNode) -> ListNode:
        
        if not head:
            return head
        
        if head.next:
            newHead = self.reverseList(head.next)
            head.next.next = head
            head.next = None
            return newHead
        else:
            return head
```

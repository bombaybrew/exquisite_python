# Group Anagram
- Given an array of strings, group the anagrams together.

```python
class Solution:
    
    def calcHash(self, item):
        primes  = [2,3,5,7,11,13,17,19,23,29,31,37,41,43,47,53,59,61,67,71,73,79,83,89,97,101,103,107,109,113,127,131]
        hash = 1
        for char in item:
            hash = hash * primes[ord(char)-97]
        return hash

    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:

        hashSet = {}
        for item in strs:
            hash = self.calcHash(item)
            
            if hash in hashSet:
                hashSet.get(hash).append(item)
            else:
                hashSet[hash] = [item]
            
        return hashSet.values()
```
```python
class Solution:
    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
        
        hashSet = {}
        for item in strs:
            sorted_item = ''.join(sorted(item))
            
            if sorted_item in hashSet:
                hashSet[sorted_item].append(item)
            else:
                hashSet[sorted_item] = [item]
                
        return hashSet.values()
```

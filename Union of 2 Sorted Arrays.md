## 01. Union of 2 Sorted Arrays

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/union-of-two-sorted-arrays-1587115621/1)

### Problem Description

**Task:** Given two sorted arrays a[] and b[], where each array may contain duplicate elements , the task is to return the elements in the union of the two arrays in sorted order. Union of two arrays can be defined as the set containing distinct elements that are present in either of the arrays.Examples:Input: a[] = [1, 2, 3, 4, 5], b[] = [1, 2, 3, 6, 7]Output: [1, 2, 3, 4, 5, 6, 7]Explanation: Distinct elements including both the arrays are: 1 2 3 4 5 6 7.Input: a[] = [2, 2, 3, 4, 5], b[] = [1, 1, 2, 3, 4]

#### Examples

##### Example 1

- **Output:**
```text
[1, 2]
```
- **Explanation:** Distinct elements including both the arrays are: 1 2.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n + m)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Python)

- **Submitted:** 2026-09-28 20:18:24
- **Status:** Correct
- **Marks:** 4

```python
class Solution:
    def findUnion(self, a, b):
        n=len(a)
        m=len(b)
        
        i=0
        j=0
        
        result=[]
        
        while i<n and j<m:
            if a[i]<=b[j]:
                if len(result)==0 or result[-1]!=a[i]:
                    result.append(a[i])
                    
                i+=1
                
            else:
                if len(result)==0 or result[-1]!=b[j]:
                    result.append(b[j])
                j+=1
                
        while i<n:
            if len(result)==0 or result[-1]!=a[i]:
                result.append(a[i])
                
            i+=1
            
        while j<m:
            if len(result)==0 or  result[-1]!=b[j]:
                result.append(b[j])
                
            j+=1
            
        return result
```

*Generated on: 28/9/2026, 8:19:01 pm*
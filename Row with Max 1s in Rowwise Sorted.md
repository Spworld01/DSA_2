## 01. Row with Max 1s in Rowwise Sorted

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/row-with-max-1s0023/1)

### Problem Description

**Task:** Given a 2D binary array arr[][] consisting of only 1s and 0s. Each row of the array is sorted in non-decreasing order. Find and return the index of the first row that contains the maximum number of 1s. If no such row exists, return -1.Note: The array follows 0-based indexing.Examples:Input: arr[][] = [[0,1,1,1], [0,0,1,1], [1,1,1,1]]

#### Examples

##### Example 1

- **Output:**
```text
-1
```
- **Explanation:** No row contains any 1s, so the output is -1.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n + m)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Python)

- **Submitted:** 2026-10-14 18:40:02
- **Status:** Correct
- **Marks:** 4

```python
class Solution:
    def rowWithMax1s(self, arr: list[list[int]]) -> int:
        r=len(arr)
        c=len(arr[0])
        
        
        maximum=0
        row=0
        
        for i in range(r):
            count=0
            for j in range(c):
                if arr[i][j]==1:
                    count+=1
                    
                
                    
                    
            
            if count>maximum:
                row=i
                maximum=max(maximum,count)
            
                
        if maximum==0:
            return -1
            
                
        
            
        return row
```

*Generated on: 14/10/2026, 6:41:05 pm*
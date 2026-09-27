## 01. Rotate Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/rotate-array-by-n-elements-1587115621/1)

### Problem Description

**Task:** Given an array arr[]. Rotate the array to the left (counter-clockwise direction) by d steps, where d is a positive integer. Do the mentioned change in the array in place.Note: Consider the array as circular.Examples :Input: arr[] = [1, 2, 3, 4, 5], d = 2

#### Examples

##### Example 1

- **Output:**
```text
[3, 9, 1, 7]
```
- **Explanation:** when we rotate 9 times, we'll get [3, 9, 1, 7] as resultant array.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (3)

#### Solution 1 (Python)

- **Submitted:** 2026-09-27 17:34:14
- **Status:** Correct
- **Marks:** 0

```python
class Solution:
    def rotateArr(self, arr, d):
     
        
        def rotate_(arr,left,right):
            while left<right:
                arr[left],arr[right]=arr[right],arr[left]
                left+=1
                right-=1
                
        n=len(arr)
        
        d=d%n
       
        rotate_(arr,0,d-1)
        rotate_(arr,d,n-1)
        rotate_(arr,0,n-1)
```

#### Solution 2 (Python)

- **Submitted:** 2026-09-27 17:33:46
- **Status:** Correct
- **Marks:** 0

```python
class Solution:
    def rotateArr(self, arr, d):
     
        
        def rotate_(arr,left,right):
            while left<right:
                arr[left],arr[right]=arr[right],arr[left]
                left+=1
                right-=1
                
        n=len(arr)
        
        d=d%n
       
        rotate_(arr,0,d-1)
        rotate_(arr,d,n-1)
        rotate_(arr,0,n-1)
```

#### Solution 3 (Python)

- **Submitted:** 2026-09-27 17:05:02
- **Status:** Correct
- **Marks:** 1

```python
class Solution:
    def rotateArr(self, arr, d):
     
        
        def rotate_(arr,left,right):
            while left<right:
                arr[left],arr[right]=arr[right],arr[left]
                left+=1
                right-=1
                
        n=len(arr)
        
        d=d%n
       
        rotate_(arr,0,d-1)
        rotate_(arr,d,n-1)
        rotate_(arr,0,n-1)
```

*Generated on: 27/9/2026, 5:48:44 pm*
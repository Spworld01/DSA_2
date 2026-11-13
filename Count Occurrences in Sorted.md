## 01. Count Occurrences in Sorted

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/number-of-occurrence2259/1)

### Problem Description

**Task:** Given a sorted array arr[] and a number target, find the number of occurrences of target in given array. Examples:Input: arr[] = [1, 1, 2, 2, 2, 2, 3], target = 2

#### Examples

##### Example 1

- **Output:**
```text
3
```
- **Explanation:** target = 12 occurs 3 times in the given array so the output is 3.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Python)

- **Submitted:** 2026-11-13 18:07:46
- **Status:** Correct
- **Marks:** 4

```python
class Solution:
    def lowerbound___(self,arr,target):
        n=len(arr)
        low=0
        high=n-1
        ib=-1
        while low<=high:
            mid=(low+high)//2
            if arr[mid]>=target:
                ib=mid
                high=mid-1
            else:
                low=mid+1
        return ib
        
    def upperbound__(self,arr,target):
        n=len(arr)
        low=0
        high=n-1
        up=n
        while low<=high:
            mid=(low+high)//2
            if arr[mid]>target:
                up=mid
                high=mid-1
            else:
                low=mid+1
        return up
                
    def countFreq(self, arr, target):
        IB=self.lowerbound___(arr,target)
        if IB==-1 or arr[IB]!=target:
            return 0
        UP=self.upperbound__(arr,target)
        
        return UP-IB
```

*Generated on: 13/11/2026, 6:15:50 pm*
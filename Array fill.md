## 01. Array fill

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/vector-fill/1)

### Problem Description

**Task:** Given an integer array arr[] and an integer k, fill the entire array with the value k such that every element of the array becomes equal to k.Examples:Input: arr[] = [1, 2, 3, 4], k = 0

#### Examples

##### Example 1

- **Output:**
```text
[-2]
```
- **Explanation:** The single element in the array is replaced with -2.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 09:32:04
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public void fillArray(int[] arr, int k) {
        // code here
        for(int i = 0; i < arr.length; i++) {
            arr[i] = k;
        }
    }
}
```

*Generated on: 11/1/2026, 9:32:17 AM*
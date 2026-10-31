## 01. Max and Min Product from 2 Arrays

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/product-of-maximum-in-first-array-and-minimum-in-second3943/1)

### Problem Description

**Task:** Given two arrays of arr1 and arr2, the task is to calculate the product of the maximum element of the first array arr1, and minimum element of the second array arr2.Examples :Input : arr1[] = [5, 7, 9, 3, 6, 2], arr2[] = [1, 2, 6, 1, 9]

#### Examples

##### Example 1

- **Output:**
```text
9
```
- **Explanation:** The max in arr1 is 9. The min element in arr2 is 1. The product is 9*1 = 9.

##### Example 2

- **Input:**
```text
arr1[] = [0, 0, 0, 0], arr2[] = [1, 1, 2]Output : 0
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n + m)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-31 11:46:56
- **Status:** Correct
- **Marks:** 1

```java
class Solution {

    public long minMaxProduct(int[] arr1, int[] arr2) {
        // code here
        int maxi = Integer.MIN_VALUE;
        int mini = Integer.MAX_VALUE;
        for(int i = 0; i < arr1.length; i++) {
            maxi = Math.max(maxi, arr1[i]);
        }
        for(int i = 0; i < arr2.length; i++) {
            mini = Math.min(mini, arr2[i]);
        }
        return maxi * mini;
    }
}
```

*Generated on: 10/31/2026, 11:47:16 AM*
## 01. Missing in Another Shuffled Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/missing-number-in-shuffled-array0938/1)

### Problem Description

**Task:** Given an array arr1. The contents of arr are copied into another array arr2 and numbers are shuffled. Also, one element is removed from arr2. The task is to find the missing element.Examples:Input: arr1[] = [4, 8, 1, 3, 7] and arr2[] = [7, 4, 3, 1]

#### Examples

##### Example 1

- **Output:**
```text
8
```
- **Explanation:** 8 is the only element missing from arr2.

##### Example 2

- **Input:**
```text
arr1[] = [12, 10, 15, 23, 11, 30] and arr2[] = [15, 12, 23, 11, 30]
```
- **Output:**
```text
10Explanation: 10 is the only element missing from arr2.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** Not found
- **Expected Auxiliary Space Complexity:** Not found

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 10:39:50
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int findMissing(int[] arr1, int[] arr2) {
        // code here
        int s1 = 0;
        int s2 = 0;
        for(int i = 0; i < arr1.length; i++) {
            s1 += arr1[i];
        }
        for(int i = 0; i < arr2.length; i++) {
            s2 += arr2[i];
        }
        return s1 - s2;
    }
}
```

*Generated on: 11/1/2026, 10:40:21 AM*
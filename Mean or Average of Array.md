## 01. Mean or Average of Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/mean0021/1?utm_source=chatgpt.com)

### Problem Description

**Task:** Given an array arr[], return the floor value of the mean of its elements.Examples:Input: arr[] = [1, 3, 4, 2, 6, 5, 8, 7]Output: 4Explanation: Sum of the elements is 1 + 3 + 4 + 2 + 6 + 5 + 8 + 7 = 36, Mean = 36/8 = 4.5, floor(4.5) = 4.Input: arr[] = [4, 4, 4, 4, 4]Output: 4Explanation: Sum of the elements is 4 + 4 + 4 + 4 + 4 = 20, Mean = 20/5 = 4

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 11:01:26
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public static int findMean(int[] arr) {
        // code here
        int n = arr.length;
        int sum = 0;
        for(int i : arr) {
            sum += i;
        }
        return sum / n;
    }
};
```

*Generated on: 11/1/2026, 11:11:10 AM*
## 01. Multiply Left and Right Array Sums

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/multiply-left-and-right-array-sum1555/1)

### Problem Description

**Task:** Given an array of integers arr[], divide it into two subarrays left and right such that left contains the first half of the elements and right contains the remaining elements. If the size of the array is odd, the right subarray contains one extra element. Compute the sum of elements in both subarrays and return the product of these two sums.Examples :Input : arr = [1, 2, 3, 4]

#### Examples

##### Example 1

- **Output:**
```text
21
```
- **Explanation:** Sum up an array from index 0 to 1 = 3, Sum up an array from index 2 to 3 = 7. Their multiplication is 21.

##### Example 2

- **Input:**
```text
arr = [1, 2]
```
- **Output:**
```text
2 Explanation: Their multiplication is 1*2 is equal to 2.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-31 10:31:27
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int multiply(int[] arr) {
        // code here
        int leftSum = 0;
        int rightSum = 0;
        int n = arr.length;
        for(int i = 0; i < n; i++) {
            if(i < n / 2) leftSum += arr[i];
            else rightSum += arr[i];
        }
        return leftSum * rightSum;
    }
}
```

*Generated on: 10/31/2026, 10:31:44 AM*
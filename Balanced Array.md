## 01. Balanced Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/balanced-array07200720/1)

### Problem Description

**Task:** Given an array arr[] of even size, find the minimum value that needs to be added to any one element so that the array becomes balanced. An array is considered balanced when the sum of elements in the left half is equal to the sum of elements in the right half.Examples :Input: arr = [1, 5, 3, 2]

#### Examples

##### Example 1

- **Output:**
```text
2
```
- **Explanation:** Sum of first 3 elements is 1 + 2 + 1 = 4, Sum of last three elements is 2 + 1 + 3 = 6, To make the array balanced you can add 2.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-31 10:39:43
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int minValueToBalance(List<Integer> arr) {
        // code here
        int leftSum = 0;
        int rightSum = 0;
        int n = arr.size();
        for(int i = 0; i < n; i++) {
            if(i < n / 2) leftSum += arr.get(i);
            else rightSum += arr.get(i);
        }
        return Math.abs(rightSum - leftSum);
    }
};
```

*Generated on: 10/31/2026, 10:40:05 AM*
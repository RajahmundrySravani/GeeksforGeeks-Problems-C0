## 01. Min and Max in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/find-minimum-and-maximum-element-in-an-array4428/1?utm_source=chatgpt.com)

### Problem Description

**Task:** Given an array arr[]. Your task is to find the minimum and maximum elements in the array.Examples:Input: arr[] = [1, 4, 3, 5, 8, 6]

#### Examples

##### Example 1

- **Output:**
```text
[3, 15]Explanation: minimum and maximum element of array are 3 and 15.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-24 15:54:56
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public ArrayList<Integer> getMinMax(int[] arr) {
        // code Here
        int mini = Integer.MAX_VALUE;
        int maxi = Integer.MIN_VALUE;
        for(int i : arr) {
            mini = Math.min(mini, i);
            maxi = Math.max(maxi, i);
        }
        ArrayList<Integer> a = new ArrayList<>();
        a.add(mini);
        a.add(maxi);
        return a;
    }
}
```

*Generated on: 11/1/2026, 11:10:39 AM*
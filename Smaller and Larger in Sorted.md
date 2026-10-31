## 01. Smaller and Larger in Sorted

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/smaller-and-larger4005/1)

### Problem Description

**Task:** Given a sorted array arr[] and a value target, return an array of size 2. The first value is the number of elements less than or equal to the target, and the second value is the number of elements greater than or equal to the target.Examples:Input: arr[] = [1, 2, 8, 10, 11, 12, 19], target = 0

#### Examples

##### Example 1

- **Output:**
```text
[0, 7]
```
- **Explanation:** There are 6 elements less or equal to 12 and 4 elements greater or equal to 12.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-31 09:54:37
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    int[] getMoreAndLess(int[] arr, int target) {
        // code here
        int cntless = 0;
        int cnthigh = 0;
        for(int i : arr) {
            if(i <= target) cntless++;
            if(i >= target) cnthigh++;
        }
        return new int[] {cntless, cnthigh};
    }
}
```

*Generated on: 10/31/2026, 9:54:50 AM*
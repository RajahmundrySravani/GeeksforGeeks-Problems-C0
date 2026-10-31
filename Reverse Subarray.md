## 01. Reverse Subarray

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/reverse-sub-array5620/1)

### Problem Description

**Task:** Given an array arr, you need to reverse a subarray of that array. The range of this subarray is given by indices l and r (1-based indexing).Examples:Input: arr[] = [1, 2, 3, 4, 5, 6, 7], l = 2, r = 4

#### Examples

##### Example 1

- **Output:**
```text
[4, 7, 6, 1]
```
- **Explanation:** After reversing the elements in range 1 to 4 (1, 6, 7, 4), modified array is 4, 7, 6, 1.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-31 12:32:04
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public static ArrayList<Integer> reverseSubArray(ArrayList<Integer> arr, int l,
                                                     int r) {
        // code here
        Collections.reverse(arr.subList(l - 1, r));
        ArrayList<Integer> ans = new ArrayList<Integer>(arr);
        return ans;
    }
}
```

*Generated on: 10/31/2026, 12:32:32 PM*
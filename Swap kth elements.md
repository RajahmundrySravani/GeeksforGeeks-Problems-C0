## 01. Swap kth elements

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/swap-kth-elements5500/1)

### Problem Description

**Task:** Given an array arr[], swap the k^th element from the beginning with the k^th element from the end.Note: 1-based indexing is followed.Examples :Input: arr[] = [1, 2, 3, 4, 5, 6, 7, 8], k = 3

#### Examples

##### Example 1

- **Output:**
```text
[5, 1, 6, 3, 2]
```
- **Explanation:** 2^nd element from beginning is 3 and from end is 1.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(1)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-31 10:02:40
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public void swapKth(List<Integer> arr, int k) {
        // code here
        int n = arr.size();
        int ele1 = arr.get(k - 1);
        int ele2 = arr.get(n - k);
        arr.set(k - 1, ele2);
        arr.set(n - k, ele1);
        
    }
}
```

*Generated on: 10/31/2026, 10:02:56 AM*
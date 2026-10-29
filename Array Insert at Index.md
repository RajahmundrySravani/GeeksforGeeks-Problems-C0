## 01. Array Insert at Index

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/array-insert-at-index/1)

### Problem Description

**Task:** Given an array arr(0-based index) and two positive integer index and val. You need to insert an val at given index.Examples:Input: arr[] = [1, 2, 3, 4, 5], index = 5, val = 90Output: 1 2 3 4 5 90

#### Examples

##### Example 1

- **Output:**
```text
[1, 2, 90, 3, 4, 5]
```
- **Explanation:** 90 is inserted at index 2(0-based indexing). After inserting, array elements are like [1, 2, 90, 3, 4, 5].

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-29 23:16:04
- **Status:** Correct
- **Marks:** 1

```java
import java.util.*;

class Solution {
    public void insertAtIndex(ArrayList<Integer> arr, int index, int val) {
        // code here
        arr.add(index, val);
    }
}
```

*Generated on: 10/29/2026, 11:16:27 PM*
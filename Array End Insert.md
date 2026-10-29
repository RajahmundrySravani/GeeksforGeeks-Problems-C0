## 01. Array End Insert

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/array-insert-at-end/1)

### Problem Description

**Task:** Given an array arr[] that is not completely filled and a value val, you have to insert the value at the end of the array.Examples :Input: arr[] = [1, 2, 3, 4, 5], val = 90

#### Examples

##### Example 1

- **Output:**
```text
[1, 2, 3, 50]
```
- **Explanation:** After inserting 50 at the end, we have array elements as 1 2 3 50.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(1)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-29 23:40:27
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public void insertAtEnd(ArrayList<Integer> arr, int val) {
        // code here
        arr.add(val);
    }
}
```

*Generated on: 10/29/2026, 11:40:40 PM*
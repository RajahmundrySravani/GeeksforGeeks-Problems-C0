## 01. Elements in Range

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/elements-in-the-range2834/1)

### Problem Description

**Task:** Given an array arr[] containing distinct positive integers, and two integers start and end defining a range. Find if the array contains all elements within inclusive range [start, end].Examples :Input: start = 2, end = 5, arr[] = [1, 4, 5, 2, 7, 8, 3]

#### Examples

##### Example 1

- **Output:**
```text
false
```
- **Explanation:** The array does not contain 6; hence, it does not contain all the elements in the range [2, 6]. Therefore, the output is false.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-29 23:38:18
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public boolean checkElements(int start, int end, int[] arr) {
        Arrays.sort(arr);
        int i = 0;
        int n = arr.length;
        while(i < n && i <= start) {
            if(arr[i] == start) break;
            i++;
        }
        while(i < n && start <= end) {
            if(arr[i] != start++) return false;
            i++;
        }
        return start > end;
    }
}
```

*Generated on: 10/29/2026, 11:38:33 PM*
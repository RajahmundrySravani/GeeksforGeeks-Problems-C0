## 01. Smallest Repeating K Times

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/smallest-number-repeating-k-times3239/1)

### Problem Description

**Task:** Given an array arr, the goal is to find out the smallest number that is repeated exactly ‘k’ times.Note: If there is no such element then return -1.Example:Input: arr[] = [2, 2, 1, 3, 1], k = 2

#### Examples

##### Example 1

- **Output:**
```text
2
```
- **Explanation:** 5 and 2 each appear exactly 1 time. Since we need the smallest, the output is 2.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 10:27:37
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int findDuplicate(int[] arr, int k) {
        // code here
        TreeMap<Integer, Integer> tm = new TreeMap<>();
        for(int i : arr) {
            tm.put(i, tm.getOrDefault(i, 0) + 1);
        }
        for(int key : tm.keySet()) {
            if(tm.get(key) == k) return key;
        }
        return -1;
    }
};
```

*Generated on: 11/1/2026, 10:40:35 AM*
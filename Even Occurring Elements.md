## 01. Even Occurring Elements

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/even-occurring-elements4332/1)

### Problem Description

**Task:** Given an array arr[] of integers, find and return the elements with even occurrences in the array. If no such element exists, return -1. Elements should be returned in order of occurrence.Examples:Input: arr[] = [9, 12, 23, 10, 12, 12, 15, 23, 14, 12, 15]Output: [12, 15, 23]Explanation: The numbers 12, 15, and 23 each appear an even number of times.Input: arr[] = [23, 12, 56, 34, 32]Output: [-1]Explanation: Every number in the array occurs an odd number of times.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 10:05:32
- **Status:** Correct
- **Marks:** 1

```java
import java.util.*;

class Solution {
    public ArrayList<Integer> findEvenOccurrences(int[] arr) {
        // code here
        LinkedHashMap<Integer, Integer> ls = new LinkedHashMap<>();
        int n = arr.length;
        for(int i = 0; i < n; i++) {
            ls.put(arr[i], ls.getOrDefault(arr[i], 0) + 1);
        }
        ArrayList<Integer> a = new ArrayList<>();
        for(int key : ls.keySet()) {
            if(ls.get(key) % 2 == 0) {
                a.add(key);
            }
        }
        if(a.isEmpty()) a.add(-1);
        return a;
    }
}
```

*Generated on: 11/1/2026, 10:41:10 AM*
## 01. Elements Less Than K

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/elements-less-than-k/1)

### Problem Description

**Task:** Given an array arr[] and an integer k, return all elements of arr that are less than k. The elements in the returned vector should appear in the same order as in the original array. Note: If no element is less than k, return an empty vector.Examples :Input: arr[] = [5, 3, 6, 1, 3], k = 4

#### Examples

##### Example 1

- **Output:**
```text
3 1 3
```
- **Explanation:** The elements less than 4 are 3, 1, 3, and their original order is preserved.

##### Example 2

- **Input:**
```text
arr[] = [5, 6, 7], k = 5
```
- **Output:**
```text
[]
```
- **Explanation:** There is no element less than 5.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 09:48:19
- **Status:** Correct
- **Marks:** 1

```java
import java.util.*;

class Solution {
    public ArrayList<Integer> elementsLessThanK(int[] arr, int k) {
        // code here
        ArrayList<Integer> a = new ArrayList<>();
        for(int i = 0 ; i < arr.length; i++) {
            if(arr[i] < k) a.add(arr[i]); 
        }
        return a;
    }
}
```

*Generated on: 11/1/2026, 10:41:59 AM*
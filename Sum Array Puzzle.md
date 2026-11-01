## 01. Sum Array Puzzle

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/sum-array-puzzle/1)

### Problem Description

**Task:** Given an array arr[] of integers, modify the array such that each element at index i becomes the sum of all elements of the array except the element present at index i.That is, update each element as: arr[i] = arr[0] + arr[1] + ... + arr[i-1] + arr[i+1] + ... + arr[n-1]Examples:Input: arr[] = [3, 6, 4, 8, 9]

#### Examples

##### Example 1

- **Output:**
```text
[1, 1, 0]Explanation: Each element is replaced with the sum of all other elements in the array.
```
- **Explanation:** For each index, replace the current element with the sum of all remaining elements in the array. At index 0, sum = 6 + 4 + 8 + 9 = 27 At index 1, sum = 3 + 4 + 8 + 9 = 24 At index 2, sum = 3 + 6 + 8 + 9 = 26 At index 3, sum = 3 + 6 + 4 + 9 = 22 At index 4, sum = 3 + 6 + 4 + 8 = 21 Thus, the modified array becomes [27, 24, 26, 22, 21].Input: arr[] = [0, 0, 1] At index 0, sum = 0 + 1 = 1 At index 1, sum = 0 + 1 = 1 At index 2, sum = 0 + 0 = 0 Thus, the modified array becomes [1, 1, 0].

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 10:12:14
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public void sumArray(int[] arr) {
        // code here
        int n = arr.length;
        int sum = 0;
        for(int i : arr) {
            sum += i;
        }
        for(int i = 0; i < n; i++) {
            arr[i] = sum - arr[i];
        }
    }
}
```

*Generated on: 11/1/2026, 10:41:01 AM*
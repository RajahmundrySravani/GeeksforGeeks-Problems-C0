## 01. Sum of Distinct in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/sum-of-distinct-elements4801/1)

### Problem Description

**Task:** You are given an array arr. Find the sum of distinct elements in an array.Examples:Input: arr[] = [1, 2, 3, 4, 5]

#### Examples

##### Example 1

- **Output:**
```text
5
```
- **Explanation:** Only Distinct element is 5. So sum is 5.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-31 12:49:53
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    int findSum(int[] arr) {
        // code here
        HashSet<Integer> hs = new HashSet<>();
        for(int i : arr) {
            hs.add(i);
        }
        int sum = 0;
        for(int i : hs) {
            sum += i;
        }
        return sum;
    }
}
```

*Generated on: 10/31/2026, 12:50:10 PM*
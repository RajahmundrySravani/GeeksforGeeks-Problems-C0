## 01. Small Factorial

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/small-factorial0854/1?utm_source=chatgpt.com)

### Problem Description

**Task:** Calculate factorial of a given number N.
Example 1:

#### Examples

##### Example 1

- **Input:**
```text
5
```
- **Output:**
```text
120
```
- **Explanation:** 1 * 2 * 3 * 4 * 5 = 120. Your Task: You don't need to read or print anything. Your task is to complete the function find_fact() which takes n as input parameter and returns factorial of N. Expected Time Complexity: O(N) Expected Space Complexity: O(1)

#### Constraints

- **1.** `1 <= N <= 18`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** Not found
- **Expected Auxiliary Space Complexity:** Not found

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 11:00:18
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public long find_fact(int n) {
        // Code here
        long fact = 1;
        for(int i = 1; i <= n; i++) {
            fact *= i;
        }
        return fact;
    }
}
```

*Generated on: 11/1/2026, 11:11:21 AM*
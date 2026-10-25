## 01. Count Divisors of 1 to n

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/james-bond-and-divisors5539/1?page=2&category=Prime%20Number&sortBy=submissions)

### Problem Description

**Task:** Given an integer n, find the sum of the count of divisors for each number from 1 to n.

#### Examples

##### Example 1

- **Input:**
```text
n = 2
```
- **Output:**
```text
3
```
- **Explanation:** 1 has 1 divisor: {1}. 2 has 2 divisors: {1, 2}. The total count is 1 + 2 = 3.

##### Example 2

- **Input:**
```text
n = 5
```
- **Output:**
```text
10
```
- **Explanation:** 1 has 1 divisor: {1}. 2 has 2 divisors: {1, 2}. 3 has 2 divisors: {1, 3}.4 has 3 divisors: {1, 2, 4}.5 has 2 divisors: {1, 5}. The total count is 1 + 2 + 2 + 3 + 2 = 10.

#### Constraints

- **1.** `1 ≤ n ≤ 10⁵`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-25 21:27:41
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    public int divCountSum(int n) {
        // code here
        int cnt = 0;
        for(int i = 1; i <= n; i++) {
            cnt += n / i;
        }
        return cnt;
        
    }
}
```

*Generated on: 10/25/2026, 9:29:17 PM*
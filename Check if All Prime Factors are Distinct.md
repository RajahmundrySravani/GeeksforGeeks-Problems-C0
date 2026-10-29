## 01. Check if All Prime Factors are Distinct

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/prime-factorization-and-geek-number1915/1)

### Problem Description

**Task:** Given a number, check if all prime factors appear only once in prime factorization.

#### Examples

##### Example 1

- **Input:**
```text
n = 22
```
- **Output:**
```text
true Explaination: 22 = 2¹¹¹^1. Here all the powers of prime numbers are one.
```

##### Example 2

- **Input:**
```text
n = 4
```
- **Output:**
```text
false Explaination: 4 = 2². Here all the powers of all the prime are not one.
```

#### Constraints

- **1.** `1 ≤ n ≤ 10⁶`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(sqrt(n))
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-29 16:06:03
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    public boolean distinctPF(int n) {
        // code here
        for(int i = 2; i <= n / i; i++) {
            if(n % i == 0) {
                n = n / i;
                if(n % i == 0) return false;
            }
        }
        return true;
    }
}
```

*Generated on: 10/29/2026, 4:06:24 PM*
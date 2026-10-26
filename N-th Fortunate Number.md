## 01. N-th Fortunate Number

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/find-n-th-fortunate-number5740/1?page=3&category=Prime%20Number&sortBy=submissions)

### Problem Description

**Task:** Given an integer n, find the n^th Fortunate number. For a positive integer n, let p be the product of the first n prime numbers, i.e. prime factorials (or primorials) of order n. The Fortunate number is the smallest integer m > 1 such that: p + m is a prime number.

#### Examples

##### Example 1

- **Input:**
```text
n = 3
```
- **Output:**
```text
7
```
- **Explanation:** Product of first 3 primes: 2 × 3 × 5 = 30. The smallest m > 1 such that 30 + m is prime is 7. Note that 30 + 7 = 37

##### Example 2

- **Input:**
```text
n = 5
```
- **Output:**
```text
23
```
- **Explanation:** Product of first 5 primes: 2 × 3 × 5 × 7 × 11 = 2310. The smallest m > 1 such that 2310 + m is prime is 23. Note that 2310 + 23 = 2333

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n + m * sqrt(p + m))
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-26 10:56:19
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    private boolean isPrime(long x) {
        if (x < 2) return false;
        if (x % 2 == 0) return x == 2;

        for (long i = 3; i <= x / i; i += 2) {
            if (x % i == 0) return false;
        }
        return true;
    }

    public int nthFortunateNum(int n) {
        long pro = 1;
        int count = 0;
        int num = 2;

        while (count < n) {
            if (isPrime(num)) {
                if (pro > Long.MAX_VALUE / num) return -1;
                pro *= num;
                count++;
            }
            num++;
        }

        for (long m = 2; m <= Integer.MAX_VALUE - pro; m++) {
            if (isPrime(pro + m)) return (int) m;
        }

        return -1;
    }
}
```

*Generated on: 10/26/2026, 10:56:58 AM*
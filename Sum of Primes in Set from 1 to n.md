## 01. Sum of Primes in Set from 1 to n

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/sum-of-all-prime-numbers-between-1-and-n4404/1)

### Problem Description

**Task:** Given a positive integer n, compute and return the sum of all prime numbers between 1 and n (inclusive).Examples:Input: n = 5

#### Examples

##### Example 1

- **Output:**
```text
10
```
- **Explanation:** 2, 3 and 5 are prime numbers between 1 and 5(inclusive), and their sum is 2 + 3 + 5 = 10.

##### Example 2

- **Input:**
```text
n = 10
```
- **Output:**
```text
17
```
- **Explanation:** 2, 3, 5 and 7 are prime numbers between 1 and 10(inclusive), and their sum is 2 + 3 + 5 + 7 = 17.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(nloglogn)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-25 07:06:49
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public int primeSum(int n) {
        // code here
        boolean isPrime[] = new boolean[n + 1];
        for(int i = 2; i <= n; i++) {
            isPrime[i] = true;
        }
        for(int i = 2; i * i <= n; i++) {
            if(isPrime[i]) {
                for(int j = i * i; j <= n; j = i + j) {
                    isPrime[j] = false; 
                }
            }
        }
        int sum = 0;
        for(int i = 2; i <= n; i++) {
            if(isPrime[i]) {
                sum += i;
            }
        }
        return sum;
        
    }
}
```

*Generated on: 10/25/2026, 7:34:47 AM*
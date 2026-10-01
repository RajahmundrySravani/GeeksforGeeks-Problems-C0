## 01. Prime Number

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/prime-number2314/1)

### Problem Description

**Task:** Given a number n, determine whether it is a prime number or not.Note: A prime number is a number greater than 1 that has no positive divisors other than 1 and itself.Examples :Input: n = 7

#### Examples

##### Example 1

- **Output:**
```text
false
```
- **Explanation:** 1 has only one divisor (1 itself), which is not sufficient for it to be considered prime.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(sqrt(n))
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (5)

#### Solution 1 (Java)

- **Submitted:** 2026-10-01 06:13:55
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    static boolean isPrime(int n) {
        // code here
        if(n <= 1) return false;
        if(n == 2 || n == 3) return true;
        if(n % 2 == 0) return false;
        if(n % 3 == 0) return false;
        for(int i = 5; i * i <= n; i += 6) {
            if(n % i == 0 || n % (i + 2) == 0) return false;
        }
        return true;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-09-27 21:16:36
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    static boolean isPrime(int n) {
        // code here
        if(n <= 1) return false;
        if(n == 2 || n == 3) return true;
        if(n % 2 == 0) return false;
        if(n % 3 == 0) return false;
        for(int i = 5; i * i <= n; i += 6) {
            if(n % i == 0 || n % (i + 2) == 0) return false;
        }
        return true;
    }
}
```

#### Solution 3 (Java)

- **Submitted:** 2026-07-27 13:32:05
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    static boolean isPrime(int n) {
        // code here
        if(n <= 1) return false;
        if(n == 2 || n == 3) return true;
        if(n % 2 == 0) return false;
        if(n % 3 == 0) return false;
        for(int i = 5; i * i <= n; i += 6) {
            if(n % i == 0 || n % (i + 2) == 0) return false;
        }
        return true;
    }
}
```

#### Solution 4 (Java)

- **Submitted:** 2026-07-27 13:30:33
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    static boolean isPrime(int n) {
        // code here
        if(n <= 1) return false;
        if(n == 2 || n == 3) return true;
        if(n % 2 == 0) return false;
        if(n % 3 == 0) return false;
        for(int i = 5; i * i <= n; i += 6) {
            if(n % i == 0 || n % (i + 2) == 0) return false;
        }
        return true;
    }
}
```

#### Solution 5 (Java)

- **Submitted:** 2026-07-26 15:27:54
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    static boolean isPrime(int n) {
        // code here
        if(n <= 1) return false;
        if(n == 2 || n == 3) return true;
        if(n % 2 == 0) return false;
        if(n % 3 == 0) return false;
        for(int i = 5; i * i <= n; i += 6) {
            if(n % i == 0 || n % (i + 2) == 0) return false;
        }
        return true;
    }
}
```

*Generated on: 1/10/2026, 6:16:31 am*
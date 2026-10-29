## 01. Unique Prime Factors in Sorted Order

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/prime-factors5052/1)

### Problem Description

**Task:** Given a number n. Find its unique prime factors in increasing order.

#### Examples

##### Example 1

- **Input:**
```text
n = 100
```
- **Output:**
```text
[2, 5]
```
- **Explanation:** Unique prime factors of 100 are 2 and 5.

##### Example 2

- **Input:**
```text
n = 60
```
- **Output:**
```text
[2, 3, 5]
```
- **Explanation:** Prime factors of 60 are 2, 2, 3, 5. Unique prime factors are 2, 3 and 5.

#### Constraints

- **1.** `1 ≤ n ≤ 10⁶`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(sqrt(n))
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-29 15:38:21
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public static ArrayList<Integer> primeFac(int n) {
        // code here
        ArrayList<Integer> a = new ArrayList<>();
        for(int i = 2; i <= n / i; i++) {
            if(n % i == 0) {
                a.add(i);
                while(n % i == 0) {
                    n /= i;
                }
            }
        }
        if(n > 1) a.add(n);
        return a;
    }
    public static boolean isPrime(int n) {
        if(n <= 1) return false;
        if(n == 2 || n == 3) return true;
        if(n % 2 == 0 || n % 3 == 0) return false;
        for(int i = 5; i <= n / i; i += 6) {
            if(n % i == 0 || n % (i + 2) == 0) return false;
        }
        return true;
    }
}
```

*Generated on: 10/29/2026, 3:38:52 PM*
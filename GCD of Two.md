## 01. GCD of Two

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/gcd-of-two-numbers3459/1)

### Problem Description

**Task:** Given two positive integers a and b, find GCD of a and b.

> **Note:** Don't use the inbuilt gcd function

#### Examples

##### Example 1

- **Input:**
```text
a = 20, b = 28
```
- **Output:**
```text
4
```
- **Explanation:** GCD of 20 and 28 is 4

##### Example 2

- **Input:**
```text
a = 60, b = 36
```
- **Output:**
```text
12
```
- **Explanation:** GCD of 60 and 36 is 12

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log(min(a, b)))
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-09-29 13:38:27
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public static int gcd(int a, int b) {
        // code here
        while(a != 0 && b != 0) {
            if(a < b) {
                b = b % a;
            }
            else {
                a = a % b;
            }
        }
        if(a == 0) return b;
        return a;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2025-04-19 19:33:32
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
  public:
    int gcd(int a, int b) {
        // code here
        while( a > 0 && b > 0)
        {
            if( a > b) a = a % b;
            else b = b % a;
        }
        if( a == 0) return b;
        else return a;
    }
};
```

*Generated on: 29/9/2026, 1:38:52 pm*
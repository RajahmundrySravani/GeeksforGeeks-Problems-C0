## 01. LCM And GCD

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/lcm-and-gcd4516/1)

### Problem Description

**Task:** Given two integers a and b, You have to compute their LCM and GCD and return an array containing their LCM and GCD.Examples:Input: a = 5 , b = 10

#### Examples

##### Example 1

- **Output:**
```text
[1, 1]
```
- **Explanation:** LCM of 1 and 1 is 1, while their GCD is 1.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log(min(a, b))
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-29 15:06:56
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public static int[] lcmAndGcd(int a, int b) {
        // code here
        return new int[] {lcm(a, b), gcd(a, b)};
    }
    public static int gcd(int a, int b) {
        while(a != 0 && b != 0) {
            if(a > b) a %= b;
            else b %= a;
        }
        if(a == 0) return b;
        return a;
    }
    public static int lcm(int a, int b) {
        int lcm = (a / gcd(a, b)) * b;
        return lcm;
    }
}
```

*Generated on: 10/29/2026, 3:09:44 PM*
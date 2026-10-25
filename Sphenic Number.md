## 01. Sphenic Number

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/sphenic-number5922/1?page=2&category=Prime%20Number&sortBy=submissions)

### Problem Description

**Task:** Given a positive integer n, find if it is a Sphenic Number. A number is called a Sphenic Number if it is the product of exactly three distinct prime numbers.

#### Examples

##### Example 1

- **Input:**
```text
n = 30
```
- **Output:**
```text
true
```
- **Explanation:** 30 = 2 * 3 * 5 so n is product of 3 distinct prime numbers.

##### Example 2

- **Input:**
```text
n = 60
```
- **Output:**
```text
false
```
- **Explanation:** 60 = 2 * 2 * 3 * 5 so n is product of 4 prime numbers.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(sqrt(n))
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-25 15:58:30
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public boolean isSphenicNo(int n) {
        // code here
        if(n == 1) return false;
        int cnt = 0;
        HashMap<Integer, Integer> hm = new HashMap<>();
        for(int i = 2; i <= n / i; i++) {
            while(n % i == 0) {
                hm.put(i, hm.getOrDefault(i, 0) + 1);
                n /= i;
                if(hm.size() > 3) return false;
            }
        }
        if(n > 1) hm.put(n, hm.getOrDefault(n, 0) + 1);
        if(hm.size() != 3) return false;
        for(int key : hm.keySet()) {
            if(hm.get(key) > 1) return false;
        }
        return true;
    }
}
```

*Generated on: 10/25/2026, 3:59:56 PM*
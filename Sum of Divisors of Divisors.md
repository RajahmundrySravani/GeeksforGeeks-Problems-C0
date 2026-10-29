## 01. Sum of Divisors of Divisors

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/find-sum-of-divisors5636/1?page=2&category=Prime%20Number&sortBy=submissions)

### Problem Description

**Task:** Given a natural number N, the task is to find the sum of the divisors of all the divisors of N.
Example 1:

#### Examples

##### Example 1

- **Explanation:** Divisors of 54 = 1, 2, 3, 6, 9, 18, 27, 54. Sum of divisors of 1, 2, 3, 6, 9, 18, 27, 54 are 1, 3, 4, 12, 13, 39, 40, 120 respectively. Sum of divisors of all the divisors of 54 = 1 + 3 + 4 + 12 + 13 + 39 + 40 + 120 = 232. Example 2:

##### Example 2

- **Explanation:** Divisors of 10 are 1, 2, 5, 10 Sums of divisors of all the divisors are 1, 3, 6, 18. Overall sum = 1 + 3 + 6 + 18 = 28 Your Task: You don't need to read input or print anything. Your task is to complete the function sumOfDivisors() which takes an integer N as an input parameter and return the sum of the divisors of all the divisors of N. Expected Time Complexity: O(NloglogN)Expected Auxiliary Space: O(N)

#### Constraints

- **1.** `1 <= N <= 10⁴`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** Not found
- **Expected Auxiliary Space Complexity:** Not found

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-29 14:41:08
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    static int sumOfDivisors(int n) {
        // code here
        int GrandSum = 0;
        for(int i = 1; i <= n / i; i++) {
            if(n % i == 0) {
                GrandSum += findDivis(i);
                if(n / i != i) {
                    GrandSum += findDivis(n / i);
                }
            }
        }
        return GrandSum;
    }
    public static int findDivis(int n) {
        ArrayList<Integer> a = new ArrayList<>();
        int sum = 0;
        for(int i = 1; i <= n / i; i++) {
            if(n % i == 0) {
                a.add(i);
                if(n / i != i) {
                    a.add(n / i);
                }
            }
        }
        for(int i : a) {
            sum += i;
        }
        return sum;
    }
}
```

*Generated on: 10/29/2026, 2:41:35 PM*
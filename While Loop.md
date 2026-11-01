## 01. While Loop

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/while-loop/1?utm_source=chatgpt.com)

### Problem Description

**Task:** Given a number n, print all numbers from 0 to n in increasing order in a single line using a while loop.Examples: Input: n = 3

#### Examples

##### Example 1

- **Output:**
```text
0 1 2 3
```
- **Explanation:** Numbers from 0 to 3 in increasing order are 0 1 2 3.Input: n = 5Output: 0 1 2 3 4 5Explanation: Numbers from 0 to 5 in increasing order are 0 1 2 3 4 5.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 10:58:38
- **Status:** Correct
- **Marks:** 1

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        // code here
        for(int i = 0; i <= n; i++) {
            System.out.print(i);
            if(i != n) System.out.print(" ");
        }
    }
}
```

*Generated on: 11/1/2026, 11:12:01 AM*
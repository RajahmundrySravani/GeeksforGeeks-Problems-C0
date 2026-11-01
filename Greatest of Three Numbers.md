## 01. Greatest of Three Numbers

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/greatest-of-three-numbers2520/1?utm_source=chatgpt.com)

### Problem Description

**Task:** Given three numbers a, b and c. Find the greatest number among them.Examples:Input: a = 10, b = 3, c = 2

#### Examples

##### Example 1

- **Output:**
```text
-2
```
- **Explanation:** -2 is greatest among the three

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(1)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 10:56:03
- **Status:** Correct
- **Marks:** 1

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();

        // code here
        System.out.print(Math.max(a, Math.max(b, c)));
    }
}
```

*Generated on: 11/1/2026, 11:12:30 AM*
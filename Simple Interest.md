## 01. Simple Interest

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/simple-interest3457/1?utm_source=chatgpt.com)

### Problem Description

**Task:** Given three integers p, r and t, denoting Principal, Rate of Interest and Time period respectively. Calculate and print the Simple Interest.

#### Examples

##### Example 1

- **Input:**
```text
p = 100, r = 20, t = 2
```
- **Output:**
```text
40.00
```
- **Explanation:** The simple interest on 100 at a rate of 20% across 2 time periods is 40.

##### Example 2

- **Input:**
```text
p = 999, r = 9, t = 9
```
- **Output:**
```text
809.19
```
- **Explanation:** The simple interest on 999 at a rate of 9% across 9 time periods is 809.19

#### Constraints

- **1.** `1 ≤ p ≤ 10⁵¹ ≤ r, t ≤ 100`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(1)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 10:54:32
- **Status:** Correct
- **Marks:** 1

```java
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int p = sc.nextInt();
        int r = sc.nextInt();
        int t = sc.nextInt();

        // code here
        double si = (double) p * r * t / 100.0;
        System.out.printf("%.2f\n", si);
    }
}
```

*Generated on: 11/1/2026, 11:12:48 AM*
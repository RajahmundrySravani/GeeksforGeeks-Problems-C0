## 01. Length of the Last Word

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/length-of-last-word5721/1)

### Problem Description

**Task:** Given a string s consisting of upper-case and lower-case alphabets along with space characters ' ', return the length of the last word present in the string.

> **Note:** The string may contain trailing spaces.

#### Examples

##### Example 1

- **Input:**
```text
s = "Geeks for Geeks"
```
- **Output:**
```text
5
```
- **Explanation:** The last word is "Geeks" of length 5.

##### Example 2

- **Input:**
```text
s = "Start Coding Here "
```
- **Output:**
```text
4
```
- **Explanation:** The last word is "Here" of length 4.

#### Constraints

- **1.** `1 ≤ |s| ≤ 100|s| denotes the length of the string s.`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-29 07:20:47
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int lastWordLen(String s) {
        // code here
        String[] a = s.split(" ");
        return a[a.length - 1].length();
    }
}
```

*Generated on: 29/9/2026, 7:21:13 am*
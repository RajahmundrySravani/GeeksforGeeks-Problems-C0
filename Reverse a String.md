## 01. Reverse a String

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/reverse-a-string/1?utm_source=chatgpt.com)

### Problem Description

**Task:** Given a string s, reverse the string.Examples:Input: s = "Geeks"

#### Examples

##### Example 1

- **Output:**
```text
"skeeG"
```

##### Example 2

- **Input:**
```text
s = "for"
```
- **Output:**
```text
"a"
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 11:07:23
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public static String reverseString(String s) {
        // code here
        char[] a = s.toCharArray();
        rev(a);
        return String.valueOf(a);
    }
    public static void rev(char[] a) {
        int n = a.length;
        int l = 0;
        int r = n - 1;
        while(l < r) {
            swap(a, l++, r--);
        }
    }
    public static void swap(char[] a, int i, int j) {
        char t = a[i];
        a[i] = a[j];
        a[j] = t;
    }
}
```

*Generated on: 11/1/2026, 11:10:27 AM*
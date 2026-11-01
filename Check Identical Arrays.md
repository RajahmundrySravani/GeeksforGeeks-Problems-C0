## 01. Check Identical Arrays

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/equals-method/1)

### Problem Description

**Task:** Given a two integer arrays a[] and b[], return true if both the arrays contain the same elements in the same order. Otherwise, return false. Examples:Input: a[] = [1, 2, 3, 4], b[] = [4, 3, 2, 1]

#### Examples

##### Example 1

- **Output:**
```text
true
```
- **Explanation:** Both arrays are same as they contain the same elements and in same order. So we print true.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 09:46:49
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public boolean checkIdentical(int a[], int b[]) {
        // code here
        if(a.length != b.length) return false;
        for(int i = 0; i < a.length; i++) {
            if(a[i] != b[i]) return false;
        }
        return true;
    }
}
```

*Generated on: 11/1/2026, 10:42:13 AM*
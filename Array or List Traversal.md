## 01. Array or List Traversal

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/array-traversal/1)

### Problem Description

**Task:** Given an array arr[] of size n that contains integers. Print the elements of the array in a single line with a space between them.Note: Don't add a new line at the end.Examples:Input: arr[] = [54, 43, 2, 1, 5]

#### Examples

##### Example 1

- **Output:**
```text
324 5 2 2
```
- **Explanation:** Just traverse and print the numbers.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-29 22:59:25
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public void arrayTraversal(int[] arr) {
        // code here
        for(int i : arr) {
            System.out.print(i + " ");
        }
    }
}
```

*Generated on: 10/29/2026, 11:00:57 PM*
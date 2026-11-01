## 01. Get Smaller in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/get-smaller-elements/1)

### Problem Description

**Task:** Given an array arr[], return all the elements which are less than a given value x. The order of returned smaller elements should be according their appearance in the input array. Examples:Input: arr[] = [54, 43, 2, 1, 5], x = 7

#### Examples

##### Example 1

- **Output:**
```text
2 2
```
- **Explanation:** 2, 2 are smaller than 3.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 09:58:57
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public ArrayList<Integer> getSmaller(int arr[], int target) {
        // code here
        ArrayList<Integer> a = new ArrayList<>();
        for(int i : arr) {
            if(i < target) a.add(i);
        }
        return a;
    }
}
```

*Generated on: 11/1/2026, 10:41:36 AM*
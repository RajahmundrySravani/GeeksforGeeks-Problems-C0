## 01. Count Odd and Even

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/count-odd-even/1)

### Problem Description

**Task:** Given an array arr[] of positive integers. The task is to return the count of the number of odd and even elements in the array.Note: Return two elements where the first one in the count of odd & second one is the count of even.Examples:Input: arr[] = [1, 2, 3, 4, 5]

#### Examples

##### Example 1

- **Output:**
```text
2 0Explanation: There are 2 odd elements (1, 1) and no even elements.
```
- **Explanation:** There are 3 odd elements (1, 3, 5) and 2 even elements (2 and 4).Input: arr[] = [1, 1]

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-29 23:13:57
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int[] countOddEven(int[] arr) {
        // Code here
        int odds = 0;
        int evens = 0;
        for(int  i : arr) {
            if(i % 2 == 0) evens++;
            else odds++;
        }
        return new int[] {odds, evens};
    }
}
```

*Generated on: 10/29/2026, 11:16:10 PM*
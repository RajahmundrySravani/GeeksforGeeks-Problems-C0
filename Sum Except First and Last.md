## 01. Sum Except First and Last

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/max-length-chain/1)

### Problem Description

**Task:** Given an array arr of numbers. Return the sum of all the elements except the first and last elements.Examples:Input: arr[] = [5, 24, 39, 60, 15, 28, 27, 40, 50, 90]

#### Examples

##### Example 1

- **Output:**
```text
283
```
- **Explanation:** The sum of all the elements except the first and last element is 283.

##### Example 2

- **Input:**
```text
arr[] = [5, 10, 1, 11]
```
- **Output:**
```text
11
```
- **Explanation:** The sum of all the elements except the first and last element is 11.

##### Example 3

- **Input:**
```text
arr[] = [5, 10]
```
- **Output:**
```text
0
```
- **Explanation:** The sum of all the elements except the first and last element is 0.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-29 23:21:01
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int sumExceptFirstLast(int[] arr) {
        // code here
        int i = 1;
        int n = arr.length - 1;
        int sum = 0;
        while(i < n) {
            sum += arr[i];
            i++;
        }
        return sum;
    }
}
```

*Generated on: 10/29/2026, 11:21:15 PM*
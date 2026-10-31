## 01. Segregate Even and Odd numbers

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/segregate-even-and-odd-numbers4629/1)

### Problem Description

**Task:** Given an array arr, write a program segregating even and odd numbers. The program should put all even numbers first in sorted order, and then odd numbers in sorted order.

> **Note:** - You don't need to return the array, you need to modify it in-place.

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [12, 34, 45, 9, 8, 90, 3]
```
- **Output:**
```text
[8, 12, 34, 90, 3, 9, 45]
```
- **Explanation:** Even numbers are 12, 34, 8 and 90. Rest are odd numbers.

##### Example 2

- **Input:**
```text
arr[] = [0, 1, 2, 3, 4]
```
- **Output:**
```text
[0, 2, 4, 1, 3]
```
- **Explanation:** 0 2 4 are even and 1 3 are odd numbers.

##### Example 3

- **Input:**
```text
arr[] = [10, 22, 4, 6]
```
- **Output:**
```text
[4, 6, 10, 22]
```
- **Explanation:** Here all elements are even, so no need of segregataion

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-31 12:20:20
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    void segregateEvenOdd(int arr[]) {
        // code here
        int i = 0;
        int n = arr.length;
        for(int j = 0 ; j < n; j++) {
            if(arr[j] % 2 == 0) {
                swap(arr, j, i);
                i++;
            }
        }
        Arrays.sort(arr, 0, i);
        Arrays.sort(arr, i, n);
        
    }
    public static void swap(int[] a, int i, int j) {
        int t = a[i];
        a[i] = a[j];
        a[j] = t;
    }
}
```

*Generated on: 10/31/2026, 12:20:46 PM*
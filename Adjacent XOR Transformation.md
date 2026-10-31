## 01. Adjacent XOR Transformation

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/game-with-nos3123/1)

### Problem Description

**Task:** Given an array arr[] of size n, transform it according to the following rule:
For every index i from 0 to n - 2, replace arr[i] with arr[i] XOR arr[i + 1].
The last element has no next element, so it remains unchanged.
Return the resulting array after performing the transformation.

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [10, 11, 1, 2, 3]
```
- **Output:**
```text
[1, 10, 3, 1, 3] At index 0, arr[0] xor arr[1] = 1. At index 1, arr[1] xor arr[2] = 10. At index 2, arr[2] xor arr[3] = 3. At index 2, arr[3] xor arr[4] = 1.At index 4, No element is left so, it will remain as it is. New Array will be [1, 10, 3, 1, 3].
```

##### Example 2

- **Input:**
```text
arr[] = [5, 9, 7, 6]
```
- **Output:**
```text
[12, 14, 1, 6] At index 0, arr[0] xor arr[1] = 12. At index 1, arr[1] xor arr[2] = 14. At index 2, arr[2] xor arr[3] = 1. At index 3, No element is left So, it will remain as it is. New Array will be [12, 14, 1, 6].
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-31 10:26:10
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public ArrayList<Integer> xorArray(int[] arr) {
        // code here
        int n = arr.length;
        ArrayList<Integer> ans = new ArrayList<>();
        for(int i = 0; i < n - 1; i++) {
            ans.add(arr[i] ^ arr[i + 1]);
        }
        ans.add(arr[n - 1]);
        return ans;
    }
}
```

*Generated on: 10/31/2026, 10:26:28 AM*
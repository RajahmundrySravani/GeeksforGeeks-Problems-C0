## 01. Fighting the Darkness

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/fighting-the-darkness3949/1)

### Problem Description

**Task:** Given an array arr[] representing the size of candles which is reduced by 1 unit each day. The room is illuminated using all the present candles. Find the maximum number of days the room will stay illuminated (at least one candle having a size greater than 0)

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [1, 1, 2]
```
- **Output:**
```text
2
```
- **Explanation:** The candle's length is reduced by 1 in first day. So, at the end of day 1: Sizes would be [0 0 1], So, at end of second day: Sizes would be [0 0 0]. This means the room was illuminated for 2 days.

##### Example 2

- **Input:**
```text
arr[] = [2, 3, 4, 2, 1]
```
- **Output:**
```text
4
```

#### Constraints

- **1.** `1 ≤ arr.size() ≤ 10⁶¹ ≤ arr[i] ≤ 10⁹`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** Not found
- **Expected Auxiliary Space Complexity:** Not found

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-31 12:01:21
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int maxDays(int arr[]) {
        // code here
        int maxi = Integer.MIN_VALUE;
        for(int i : arr) {
            maxi = Math.max(maxi, i);
        }
        return maxi;
    }
}
```

*Generated on: 10/31/2026, 12:01:40 PM*
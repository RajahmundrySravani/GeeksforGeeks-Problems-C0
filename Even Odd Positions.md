## 01. Even Odd Positions

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/find-the-fine4353/1)

### Problem Description

**Task:** Given an array of car numbers car[], an array of penalties fine[], and an integer date, find the total fine collected on that date. The fine is collected based on parity, i.e., on an even date, fines are collected from odd-numbered cars, and on an odd date, fines are collected from even-numbered cars.

#### Examples

##### Example 1

- **Input:**
```text
date = 12, car[] = [2375, 7682, 2325, 2352], fine[] = [250, 500, 350, 200]
```
- **Output:**
```text
600
```
- **Explanation:** The date is 12 (even), so we collect the fine from odd-numbered cars. The odd-numbered cars and the fines associated with them are as follows: 2375 - > 250 2325 - > 350 The sum of the fines is 250+350 = 600

##### Example 2

- **Input:**
```text
date = 8, car[] = [2222, 2223, 2224], fine[] = [200, 300, 400]
```
- **Output:**
```text
300
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-31 10:10:26
- **Status:** Correct
- **Marks:** 1

```java
class Solution {

    public long totalFine(int date, int car[], int fine[]) {
        // code here
        long collect = 0;
        int n = car.length;
        if(date % 2 == 0) {
            for(int i = 0; i < n; i++) {
                if(car[i] % 2 != 0) collect += fine[i];
            }
        }
        else {
            for(int i = 0; i < n; i++) {
                if(car[i] % 2 == 0) collect += fine[i];
            }
        }
        return collect;
    }
}
```

*Generated on: 10/31/2026, 10:10:44 AM*
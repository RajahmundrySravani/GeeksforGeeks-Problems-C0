## 01. Winner in Pairwise Army Battles

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/countries-at-war2936/1)

### Problem Description

**Task:** Two armies, A and B, have the same number of soldiers. The power of their soldiers is given by arr1[] and arr2[], where the ith soldier of Army A fights only the ith soldier of Army B.If arr1[i] > arr2[i], Army A wins the battle.If arr1[i] < arr2[i], Army B wins the battle.If arr1[i] = = arr2[i], both soldiers are eliminated.Return "A" if Army A wins more battles, "B" if Army B wins more battles, otherwise return "DRAW"Examples:Input: arr1[] = [2, 2], arr2[] = [5, 5]

#### Examples

##### Example 1

- **Output:**
```text
"B"
```
- **Explanation:** Battle 1: 2 < 5, so Army B wins. Battle 2: 2 < 5, so Army B wins. Army B wins 2 battles, while Army A wins 0 battles. Therefore, the winner is "B".

##### Example 2

- **Input:**
```text
arr1[] = [9], arr2[] = [8]
```
- **Output:**
```text
"A"
```
- **Explanation:** Battle 1: 9 > 8, so Army A wins. Army A wins 1 battle, while Army B wins 0 battles. Therefore, the winner is "A".

#### Constraints

- **1.** `1 ≤ arr1.size() ≤ 10⁶⁰ ≤ arr1[i], arr2[i] ≤ 10⁵`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 10:25:01
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public String countryAtWar(int[] arr1, int[] arr2) {
        // code here
        int wina = 0;
        int winb=  0;
        int n = arr1.length;
        for(int i = 0; i < n; i++) {
            if(arr1[i] > arr2[i]) wina++;
            else if(arr2[i] > arr1[i]) winb++;
        }
        if(wina > winb) return "A";
        if(wina < winb) return "B";
        else return "DRAW";
    }
}
```

*Generated on: 11/1/2026, 10:40:51 AM*
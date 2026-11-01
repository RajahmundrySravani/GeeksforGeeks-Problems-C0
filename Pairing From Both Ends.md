## 01. Pairing From Both Ends

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/pairing-elements/1)

### Problem Description

**Task:** Given an array arr[], form pairs by pairing the first element with the last element, the second element with the second last element, and so on. If the array has an odd number of elements, pair the middle element with itself. Return all the formed pairs in the order they are created.Examples:Input: arr[] = [1, 2, 3, 4, 5]Output: [[1, 5], [2, 4], [3, 3]]Explanation: 1 is paired with 5, 2 with 4, and the middle element 3 with itself.Input: arr[] = [4, 2, 3, 1]Output: [[4, 1], [2, 3]]Explanation: 4 is paired with 1 and 2 is paired with 3.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-11-01 09:50:43
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public ArrayList<ArrayList<Integer>> arrayOfPairs(int[] arr) {
        // code here
        ArrayList<ArrayList<Integer>> ans = new ArrayList<>();
        int l = 0;
        int n = arr.length;
        int r = n - 1;
        while(l <= r) {
            ArrayList<Integer> a = new ArrayList<>();
            a.add(arr[l++]);
            a.add(arr[r--]);
            ans.add(a);
        }
        return ans;
    }
}
```

*Generated on: 11/1/2026, 10:41:48 AM*
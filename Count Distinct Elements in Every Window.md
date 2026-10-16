## 01. Count Distinct Elements in Every Window

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/count-distinct-elements-in-every-window/1)

### Problem Description

**Task:** Given an integer array arr[] and a number k. Find the count of distinct elements in every window of size k in the array.Examples:Input: arr[] = [1, 2, 1, 3, 4, 2, 3], k = 4

#### Examples

##### Example 1

- **Output:**
```text
[1, 1, 1]Explanation: Every window of size 3 in the array [1, 1, 1, 1, 1], contains only the element 1, so the number of distinct elements in each window is 1.
```
- **Explanation:** First window is [1, 2, 1, 3], count of distinct numbers is 3. Second window is [2, 1, 3, 4] count of distinct numbers is 4. Third window is [1, 3, 4, 2] count of distinct numbers is 4. Fourth window is [3, 4, 2, 3] count of distinct numbers is 3.Input: arr[] = [4, 1, 1], k = 2

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(k)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-16 18:48:35
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    ArrayList<Integer> countDistinct(int arr[], int k) {
        // code here
        int n = arr.length;
        ArrayList<Integer> ans = new ArrayList<>();
        if(k <= 0 || k > n) return ans;
        HashMap<Integer, Integer> hm = new HashMap<>();
        for(int i = 0; i < k; i++) {
            hm.put(arr[i], hm.getOrDefault(arr[i], 0) + 1);
        }
        ans.add(hm.size());
        for(int i = k; i < n; i++) {
            int leftEle = arr[i - k];
            if(hm.get(leftEle) == 1) hm.remove(leftEle);
            else {
                hm.put(leftEle, hm.get(leftEle) - 1);
            }
            
            hm.put(arr[i], hm.getOrDefault(arr[i], 0) + 1);
            ans.add(hm.size());
        }
        return ans;
    }
}
```

*Generated on: 16/10/2026, 6:49:12 pm*
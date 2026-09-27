## 01. Two Sum - Pair with Given Sum

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/key-pair5616/1)

### Problem Description

**Task:** Given an array arr[] of integers and another integer target. Determine if there exist two distinct indices such that the sum of their elements is equal to the target.Examples:Input: arr[] = [0, -1, 2, -3, 1], target = -2

#### Examples

##### Example 1

- **Output:**
```text
false
```
- **Explanation:** No pair is possible as only one element is present in arr[]

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (5)

#### Solution 1 (Java)

- **Submitted:** 2026-09-28 00:35:53
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    boolean twoSum(int arr[], int target) {
        // code here
        
        //testing
        
        HashSet<Integer> hs = new HashSet<>();
        int n = arr.length;
        for(int i = 0; i < n; i++) {
            int x = target - arr[i];
            if(hs.contains(x)) return true;
            hs.add(arr[i]);
        }
        return false;
        
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-09-27 20:23:02
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    boolean twoSum(int arr[], int target) {
        // code here
        
        //testing
        
        HashSet<Integer> hs = new HashSet<>();
        int n = arr.length;
        for(int i = 0; i < n; i++) {
            int x = target - arr[i];
            if(hs.contains(x)) return true;
            hs.add(arr[i]);
        }
        return false;
        
    }
}
```

#### Solution 3 (Java)

- **Submitted:** 2026-09-27 20:01:21
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    boolean twoSum(int arr[], int target) {
        // code here
        
        //testing
        
        HashSet<Integer> hs = new HashSet<>();
        int n = arr.length;
        for(int i = 0; i < n; i++) {
            int x = target - arr[i];
            if(hs.contains(x)) return true;
            hs.add(arr[i]);
        }
        return false;
        
    }
}
```

#### Solution 4 (Java)

- **Submitted:** 2026-09-27 19:51:01
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    boolean twoSum(int arr[], int target) {
        // code here
        
        //testing
        
        HashSet<Integer> hs = new HashSet<>();
        int n = arr.length;
        for(int i = 0; i < n; i++) {
            int x = target - arr[i];
            if(hs.contains(x)) return true;
            hs.add(arr[i]);
        }
        return false;
        
    }
}
```

#### Solution 5 (Java)

- **Submitted:** 2026-09-27 19:50:10
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    boolean twoSum(int arr[], int target) {
        // code here
        
        //testing
        
        HashSet<Integer> hs = new HashSet<>();
        int n = arr.length;
        for(int i = 0; i < n; i++) {
            int x = target - arr[i];
            if(hs.contains(x)) return true;
            hs.add(arr[i]);
        }
        return false;
        
    }
}
```

*Generated on: 28/9/2026, 12:36:26 am*
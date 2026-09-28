## 01. Array Leaders

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/leaders-in-an-array-1587115620/1)

### Problem Description

**Task:** You are given an array arr of positive integers. Your task is to find all the leaders in the array. An element is considered a leader if it is greater than or equal to all elements to its right. The rightmost element is always a leader.Examples:Input: arr = [16, 17, 4, 3, 5, 2]

#### Examples

##### Example 1

- **Output:**
```text
[17, 5, 2]
```
- **Explanation:** Note that there is nothing greater on the right side of 17, 5 and, 2.

##### Example 2

- **Input:**
```text
arr = [10, 4, 2, 4, 1]
```
- **Output:**
```text
[10, 4, 4, 1]Explanation: Note that both of the 4s are in output, as to be a leader an equal element is also allowed on the right. sideInput: arr = [5, 10, 20, 40]Output: [40]Explanation: When an array is sorted in increasing order, only the rightmost element is leader.Input: arr = [30, 10, 10, 5]Output: [30, 10, 10, 5]Explanation: When an array is sorted in non-increasing order, all elements are leaders.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (4)

#### Solution 1 (Java)

- **Submitted:** 2026-09-28 20:06:48
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    static ArrayList<Integer> leaders(int nums[]) {
        // code here
        ArrayList<Integer> a = new ArrayList<>();
                int n = nums.length;
                int max = nums[n - 1];
                a.add(0, max);
                for(int i = n - 2; i >= 0; i--) {
                    if(nums[i] >= max) {
                        a.add(0, nums[i]);
                        max = nums[i];
                    }
                }
                return a;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-08-14 12:20:23
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    static ArrayList<Integer> leaders(int arr[]) {
        // code here
        int n = arr.length;
        ArrayList<Integer> a = new ArrayList<>();
        a.add(arr[n - 1]);
        int maxi = arr[n - 1];
        for(int i = n - 2; i >= 0; i--) {
            if(arr[i] >= maxi) {
                maxi = arr[i];
                a.add(0, arr[i]);
            }
        }
        return a;
    }
}
```

#### Solution 3 (Java)

- **Submitted:** 2025-09-24 09:03:34
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    static ArrayList<Integer> leaders(int a[]) {
        // code here
        int n = a.length;
        
        ArrayList<Integer> A = new ArrayList<>();
       // for(int  i = 0; i < n; i++) {
           // int l = 1;
            //for(int j = i + 1; j < n; j++) {
            //    if(arr[i] < arr[j]) {
             //     l = 0;
                 //   break;
              //  }
          //  }
           // if(l == 1) A.add(arr[i]);
        //}
       // return A;
       
       
       
       
       A.add(a[n - 1]);
       int max = a[n - 1];
       for(int i = n - 2; i >= 0; i--) {
           if(a[i] < a[i + 1]) continue;
          // int j = i + 1;
          else if(a[i] >= max) {
           A.add(a[i]);
           max = a[i];
          }
       }
       
       
        Collections.reverse(A);
        return A;
    }
}
```

#### Solution 4 (Java)

- **Submitted:** 2025-09-23 21:30:02
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    static ArrayList<Integer> leaders(int arr[]) {
        // code here
        int n = arr.length;
        
        ArrayList<Integer> A = new ArrayList<>();
        for(int  i = 0; i < n; i++) {
            int l = 1;
            for(int j = i + 1; j < n; j++) {
                if(arr[i] < arr[j]) {
                    l = 0;
                    break;
                }
            }
            if(l == 1) A.add(arr[i]);
        }
        return A;
    }
}
```

*Generated on: 28/9/2026, 8:08:06 pm*
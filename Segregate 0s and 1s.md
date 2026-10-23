## 01. Segregate 0s and 1s

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/segregate-0s-and-1s5106/1)

### Problem Description

**Task:** Given an array arr[] consisting of only 0's and 1's. Modify the array in-place to segregate 0s onto the left side and 1s onto the right side of the array. Examples :Input: arr[] = [0, 1, 0, 1, 0, 0, 1, 1, 1, 0]

#### Examples

##### Example 1

- **Output:**
```text
[1, 1]
```
- **Explanation:** There are no 0s in the given array, so the modified array is [1, 1]

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (4)

#### Solution 1 (C++)

- **Submitted:** 2026-10-23 11:17:43
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
  public:
    void segregate0and1(vector<int> &arr) {
        // code here
        //using two pointer 
        int start=0,end=arr.size()-1;
        
        while(start<=end)
        {
            if(arr[start]==0)
            start++;
            
            else if(arr[end]==1)
            end--;
            
            else
            {
                swap(arr[start],arr[end]);
                start++;
                end--;
            }
        }
        
        
      
    }
};
```

#### Solution 2 (C++)

- **Submitted:** 2026-10-23 00:20:50
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
  public:
    void segregate0and1(vector<int> &arr) {
        // code here
        //using two pointer 
        int start=0,end=arr.size()-1;
        
        while(start<=end)
        {
            if(arr[start]==0)
            start++;
            
            else if(arr[end]==1)
            end--;
            
            else
            {
                swap(arr[start],arr[end]);
                start++;
                end--;
            }
        }
        
        
      
    }
};
```

#### Solution 3 (C++)

- **Submitted:** 2026-10-23 00:20:08
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
  public:
    void segregate0and1(vector<int> &arr) {
        // code here
        //using two pointer 
        int start=0,end=arr.size()-1;
        
        while(start<end)
        {
            if(arr[start]==0)
            start++;
            
            else if(arr[end]==1)
            end--;
            
            else
            {
                swap(arr[start],arr[end]);
                start++;
                end--;
            }
        }
        
        
      
    }
};
```

#### Solution 4 (C++)

- **Submitted:** 2026-10-22 23:58:17
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
  public:
    void segregate0and1(vector<int> &arr) {
        // code here
        sort(arr.begin(),arr.end());
        
        // return arr;
    }
};
```

*Generated on: 23/10/2026, 11:23:40*
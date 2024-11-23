## [Find the Largest element in an array](https://www.geeksforgeeks.org/problems/largest-element-in-array4009/0?utm_source=youtube&utm_medium=collab_striver_ytdescription&utm_campaign=largest-element-in-array)

Given an array arr[]. The task is to find the largest element and return it.

### Brute Force
#### Intuition:
We can sort the array in ascending order, hence the largest element will be at the last index of the array. 

#### Approach: 
- Sort the array in ascending order.
- Print the (size of the array -1)th index.

``` cpp
class Solution {
  public:
    int largest(vector<int> &arr) {
        int n = arr.size();
        sort(arr.begin(), arr.end());
        return arr[n-1];
    }
};
```
#### Time Complexity: O(N*log(N))
#### Space Complexity: O(N)
---
### Optimal Approch 
#### Intuition:
We can maintain a max variable that will update whenever the current value is greater than the value in the max variable.  

#### Approach: 
- Create a max variable and initialize it with arr[0].
- Use a for loop and compare it with other elements of the array
- If any element is greater than the max value, update max value with the element’s value
- Print the max variable.

``` cpp
class Solution {
  public:
    int largest(vector<int> &arr) {
        int max = arr[0];
        for(int i=1; i<arr.size(); i++)
        if(max < arr[i]) max = arr[i];
        return max;
    }
};
```

#### Time Complexity: O(N)
#### Space Complexity: O(1)

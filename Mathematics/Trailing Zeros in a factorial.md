## [Trailing Zeros in a Factorial](https://leetcode.com/problems/factorial-trailing-zeroes/description/)

Given an integer n, return the number of trailing zeroes in n!.

``` cpp
class Solution {
public:
    int trailingZeroes(int n) {
        if( n == 0 || n == 1) return 0;
        int res = 0;
        for(int i=5; n/i != 0; i=i*5) 
            res = res + n/i;
        return res;       
    }
};

```
#### NOTE:
- A trailing zero is always produced by prime factors 2 and 5.
- We can easily observe that the number of 2s in prime factors is always more than or equal to the number of 5s. So if we count 5s in prime factors, we are done.
- Trailing 0s in n! = Count of 5s in prime factors of n! = floor(n/5) + floor(n/25) + floor(n/125) + ....


TC: O(log5N)

SC: O(1)

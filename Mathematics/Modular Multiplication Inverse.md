## Modular Multiplication Inverse

(X * I ) % M = 1

X and M are given find I

Condition for occurance  is x is not a multiple of m and gcd of x and m must be 1.

```cpp
int modInverse(int a, int m)
    {
        a = a%m;
        
        for(int i=1; i<m; i++)
        if((a*i)%m == 1) return i;
        
        return -1;
        
    }
```
TC: O(M)
SC: O(!)

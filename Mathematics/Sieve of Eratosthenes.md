## [Sieve of Eratosthenes](https://www.interviewbit.com/problems/prime-numbers/)

Given a number A, find all prime numbers up to A (A included).
Make sure the returned array is sorted.

```cpp
vector<int> Solution::sieve(int n) {
    vector<int> ans;
    bool prime[n+1];
    memset(prime, true, sizeof(prime));
    
    for(int i=2; i*i<=n; i++) {
        if(prime[i] == true) {
            for(int j = i*i; j<=n; j = j+i)
            prime[j] = false;
        }
    }
    
    for(int i=2; i<=n ; i++) {
        if(prime[i]) ans.push_back(i);
    }
    
    return ans;   
}
```

Time Complexity : O(N* log log N)

Auxiliary Space: O(n)

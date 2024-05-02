## [LCM of Two Numbers](https://www.geeksforgeeks.org/problems/lcm-and-gcd4516/1)

Let A and B are two number 

A*B = LCM(A,B) * GCD(A*B)

```cpp
long long Gcd(long long a, long long b) {
      if(b == 0) return a;
      return Gcd( b, a % b );
  }
    vector<long long> lcmAndGcd(long long A , long long B) {
        long long gcd = Gcd(A,B);
        long long lcm = (A * B) / gcd;
        vector<long long> ans = { lcm , gcd };
        return ans;
    }
```
Time Complexity: O(log(min(a,b))

Auxiliary Space: O(log(min(a,b))

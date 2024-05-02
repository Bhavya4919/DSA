## [GCD or HCF of Two Numbers](https://www.geeksforgeeks.org/problems/gcd-of-two-numbers3459/1)

Given two positive integers a and b, find GCD of a and b.

A rectangular floor has dimensions 28 units by 21 units, and needs to be covered by identical square tiles. What’s the maximum length of the square tile that can evenly cover the entire floor?

Find GCD(28, 21)

#### Euclidean algorithm 
```cpp
int gcd(int a, int b)
{
	if (a == 0)
	return b;
	if (b == 0)
	return a;

	if (a == b)
		return a;

	if (a > b)
		return gcd(a-b, b);
	return gcd(a, b-a);
}
```
Time Complexity: O(max(a,b))

Auxiliary Space: O(max(a,b))

#### Optimized Approch
```cpp
class Solution {
  public:
    int gcd(int a, int b) {
        if (b==0) return a;
        return gcd( b, a%b );
    }
};
```

Time Complexity: O(log(min(a,b))|


Auxiliary Space: O(log(min(a,b))

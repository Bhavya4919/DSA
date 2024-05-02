## [Prime Number](https://www.geeksforgeeks.org/problems/prime-number2314/1) 

```cpp
bool isPrime(int n)
{
	if (n <= 1)
		return false;

	for (int i = 2; i <= sqrt(n); i++)
		if (n % i == 0)
			return false;

	return true;
}
```

Time Complexity: O(sqrt(n))

Auxiliary space: O(1)

#### Efficient Approch

```cpp
int isPrime(int N) {
        if(N == 1) return false;
        if(N == 2 || N == 3) return true;
        if(N%2 == 0 || N%3 == 0) return false;
        for(int i=5; i*i<=N; i=i+6) 
            if(N%i == 0 || N%(i+2) == 0) return false;
        return true;
}
```

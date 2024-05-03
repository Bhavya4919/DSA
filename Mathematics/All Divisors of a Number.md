## All Divisors of a Number

#### NOTE
Divisors always occur in pairs
One of the divisior in every pair is smaller than or equal to sqrt(N)

```cpp
void printDivisors(int n)
{
	int i;
	for (i = 1; i * i < n; i++) {
		if (n % i == 0)
			cout<<i<<" ";
	}
	if (i - (n / i) == 1) {
		i--;
	}
	for (; i >= 1; i--) {
		if (n % i == 0)
			cout<<n / i<<" ";
	}
}
```

Find the number of divisors of a Number N

``` cpp
int countFactors(int N){
        int count = 0;
        for(int i=1; i*i<= N; i++) {
            if(N% i == 0) {
                count++;
                if(i != N/i) count++;
            }
        }
        return count;
    }
```

Time Complexity: O(sqrt(n)) 

Auxiliary Space : O(1)

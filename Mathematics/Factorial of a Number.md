## Factorial of a Number

#### Iterative Method

```cpp
unsigned int factorial(unsigned int n)
{
	int res = 1, i;
	for (i = 2; i <= n; i++)
		res *= i;
	return res;
}
```
TC: O(N)

SC: O(1)

#### Recursive Method

```cpp
unsigned int factorial(unsigned int n)
{
	if (n == 0 || n == 1)
		return 1;
	return n * factorial(n - 1);
}
```

TC: O(N)

Auxillary Space: O(N)



## Power of (X, N)

```cpp
int power(int x, unsigned int y)
{
	int temp;
	if (y == 0)
		return 1;
	temp = power(x, y / 2);
  temp = temp * temp;
	if (y % 2 == 0)
		return temp;
	else
		return x * temp;
}
```
Time Complexity: O(log n)

Auxiliary Space: O(log n), for recursive call stack

```cpp
int power(int x, unsigned int y)
{
	int res = 1; // Initialize result

	while (y > 0) {
		// If y is odd, multiply x with result
		if (y & 1)
			res = res * x;

		// y must be even now
		y = y >> 1; // y = y/2
		x = x * x; // Change x to x^2
	}

```
Time Complexity: O(log y), since in loop each time the value of y decreases by half it’s current value.

Auxiliary Space: O(1), since no extra space has been taken.

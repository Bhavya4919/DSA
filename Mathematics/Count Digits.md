## Count Digits
Given a number N, the task is to return the count of digits in this number.

``` cpp
int countDigit(long long n)
{
	if (n == 0)
		return 1;
	int count = 0;
	while (n != 0) {
		n = n / 10;
		++count;
	}
	return count;
}
```
TC: O(D)   // D is the number of digits in the number

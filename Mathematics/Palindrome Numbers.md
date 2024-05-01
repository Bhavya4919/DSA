## Palindrome Numbers

Given an integer, write a function that returns true if the given number is palindrome, else false.

``` cpp
bool checkPalindrome(int n)
{
	int reverse = 0;
	int temp = n;
	while (temp != 0) {
		reverse = (reverse * 10) + (temp % 10);
		temp = temp / 10;
	}
	return (reverse == n); 
}
```

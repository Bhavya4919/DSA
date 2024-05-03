## Prime Factors

Prime factor is the factor of the given number which is a prime number. Factors are the numbers you multiply together to get another number.

if the input number is 315, then output should be “3 3 5 7”.

``` cpp
 void printPrimeFactors(int n)
{
	if(n <= 1)
		return;
	while(n % 2 == 0){
		cout<<2<<" ";
		n = n / 2;
	}
	while(n % 3 == 0){
		cout<<3<<" ";
		n = n / 3;
	}
	for(int i=5; i*i<=n; i=i+6){
		while(n % i == 0){
			cout<<i<<" ";
			n = n / i;
		}
		while(n % (i + 2) == 0){
			cout<<(i + 2)<<" ";
			n = n / (i + 2);
		}
	}
	if(n > 3)	cout<<n<<" ";
	cout<<endl;
}
```

TC: O(sqrt(N))

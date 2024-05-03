## Exactly 3 divisors 

Given a positive integer value N. The task is to find how many numbers less than or equal to N have numbers of divisors exactly equal to 3.

A numbers will have 3 divisiors only if it is a perfect square of a prime number. 

Find the number of prime numbers below sqrt(N) and see whether there squares are with N. 

``` cpp
bool isPrime(int n) {
        if (n <= 1) return false;
        if (n == 2 || n == 3) return true;
        if (n % 2 == 0 || n % 3 == 0) return false;
        for (int i = 5; i * i <= n; i += 6) {
            if (n % i == 0 || n % (i + 2) == 0) return false;
        }
        return true;
    }
    int exactly3Divisors(int N) {
        int count = 0;
        for (int i = 2; i * i <= N; i++) {
            if (isPrime(i)) {
                    count++;
            }
        }
        return count;
    }
```

Expected Time Complexity : O(N1/2 * N1/4)

Expected Auxilliary Space :  O(1)

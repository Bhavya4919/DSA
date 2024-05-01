## [Digits in Factorial](https://www.geeksforgeeks.org/problems/count-digits-in-a-factorial3957/1)

Given an integer N. You have to find the number of digits that appear in its factorial, where factorial is defined as, factorial(N) = 1*2*3*4..*N and factorial(0) = 1.

#### Note: Number of a digits in a number can be calcualted as Floor ( LOG10(N) ) + 1

Log of product of N numbers = Sum of Log of individual numbers

``` cpp
int facDigits(int N){
        double res = 0;
        while(N > 0) {
            res += log10(N);
            N--;
        }
        return floor(res) + 1;
}
```

TC: O(N)

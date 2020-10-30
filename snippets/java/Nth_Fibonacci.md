# Finding Nth Fibonacci

Fibonacci numbers are a part of very famous fibonacci series : `0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, …….` so on.

Each number in the fibonacci series is called fibonacci number and it is obtained by the sum of previous two numbers and it is fixed that the 0th fibonacci is 0 and 1st fibonacci is 1.


```java

public static int fibonacci(int n){

        int a = 0;  //0th fibonacci
        int b = 1;  //1st fibonacci

        int i = 0;
        while (i < n) {

            int sum = a + b;
            a = b;
            b = sum;

            i++;
        }

        return a;

}
```

> Actual time requirement of an algorithm cannot be computed, so 

- We find the function of the problem size that represents the algorithm's time requirement
- When the problem size (input) increases by a certain factor, the value of the function ( that maps the relationship between the derived function and the input size) increases by the same factor, this result indicates the increase in algorithm's time requirement
- Big-O notation is used to represent an algorithm's **efficiency / complexity**

## Deriving Big-O
- Use given identities, take the biggest factor (number with higher degree), ignoring all coefficients
- Eg.
	- $n^2 + n + 1 => n^2$
	- $114514n + 10203 => n$

## Common Functions in Algorithm Analysis, Ranked by desirable outcome
1. The constant function (f(n) = c, where c is any constant, translates to O(1))
2. The logarithm function ($f(n) = \log_b n$, where b > 1, in comp-sci, default log base is 2)
3. The linear function (f(n) = n)
4. The n-log-n function ($f(n) = n\log n$)
5. The quadratic function: ($f(n) = n^2$)
6. The cubic function: ($f(n) = n^3$)
7. The exponential function: ($f(n) = b^n$, where b is a positive constant and argument n is the exponent)
	- Exponent functions have **very fast growth rate**, so it is not desirable
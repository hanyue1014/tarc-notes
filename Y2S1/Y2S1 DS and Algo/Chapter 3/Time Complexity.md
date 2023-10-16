> Usually more important than [[Space Complexity]]
> Expressed as a **factor of the problem size**
> 	- Eg. when searching a collection of data, the problem size is the number of items in the collection

## How
- Estimate the times for
	- Best case -> Minimum time required
	- Average case -> Average time required
		 - Difficult to do because require a probability distribution on the set of inputs to be defined
	- Worst case -> Maximum time required
		- Much easier than average case
		- Lead to better algorithms because focus on designing for better performance in the worst case
1. Count number of [[Primitive Operations]]
2. Derive the [[Big-O Notation]]
3. Compare growth rate between different algorithms

## Example
```java
// consider the following function
/*
 * @param n adds up number from 1 to n (eg. 1 + 2 + 3 + ... + n)
*/
public abstract int sumTo(int n);

// there can be 3 algorithms to achieve the above functionality

// Algo A
@override
public int sumTo(int n) {
	int sum = 0;
	for (int i = 1; i <= n; i++)
		sum += i;
	return sum;
}

// Algo B
@override
public int sumTo(int n) {
	int sum = 0;
	for (int i = 1; i <= n; i++) {
		for (int j = 0; j < i; j++)
			sum++;
	}
	return sum;
}

// Algo C
@override
public int sumTo(int n) {
	// PAWA OF METHS BABE (AP: Sum of n terms, a = 1, d = 1)
	return n * (n + 1) / 2;
}
```

### Algo A analysis
- Total assignments = `1 + n` (we assign sum = 0 first, then the loop loops up to n times, so when the loop run for n times the sum = sum + i is assigned for n times)
- Total arithmetic operations = `n` (n additions in the loop)
- Total operation = Total assignment + total arithmetic operation = `2n + 1`

### Algo B analysis
- Total assignments: `1 + (n * (n + 1) / 2)`
	- assign sum = 0
	- The outer loop loops up to n times
		- The inner loop loops from 1 until n (so in this inner loop, the assignment scales up 1 at a time, doing 1 for the first outer loop n, 2 times for the second outer loop, 3 time for the third...[AP can be seen here, a = 1, d = 1 (1, 2, 3, 4, ..., n)])
		- So if we wanna find number of assignments in the loop, we just add how many times the inner loop will run in the whole program, which is 1 for the first time, 2 for the second time, ..., which is AP, apply AP formula, Sum of n terms: n/2 (a + (n-1)d), a = d = 1, become (n(n+1)/2)
- Total arithmetic operation: `n * (n + 1) / 2`
	- Same for the assignment, because addition happen in the inner loop
- Total operation = Total assignment + total arithmetic = $n^2 + n + 1$
### Algo C analysis
- Total assignments = 0 (we direct return it, but in teaching notes is got assign first, I modify le)
- Total arithmetic operation = 1 (n+1, addition) + 1 (n*(...), multiplication) + 1 ((...)/2, division)
- Total return = 1
- Total primitive operation = 1 + 1 + 1 + 1 = 4

### All 3 algorithm side by side, Derive [[Big-O Notation]]

| Algo A    | Algo B           | Algo C |
| --------- | ---------------- | ------ |
| O(2n + 1) | O($n^2 + n + 1$) | O(4)   |
| = O(n)    | = O($n^2$)       | = O(1) |


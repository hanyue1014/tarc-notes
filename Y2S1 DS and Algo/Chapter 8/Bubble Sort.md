- Simplest and slowest sorting algorithm
- Compare 2 adjacent elements sequentially, swaps them if they are out of order
- Called bubble sort because the larger values gradually bubbles to the end of the array
- Best case (only first pass to sort the array)
	- O(n) number of comparison is n-1 in first pass
- Worst case (inverted array)
	- O($n^2$) maximum pass is required (first pass n - 1, second pass n - 2, etc)

## Pseudocode
```
sorted = false <- to trace if no swaps in the process, can finish early
for (pass = 1 to array length) and !sorted
	sorted = true <- assume the array is sorted
	for (index = 0 to (array length - pass))
		if (array[index] > array[index + 1])
			swap array[index] and array[index + 1]
			sorted = false <- since got swap, the array is not sorted
```
- Recursive divide and conquer strategy to sort an array
- Divide array into 2 segments separated by a single pivot value (pivot selected at random, normally middle, leftmost or rightmost element)
- Recursively sort each of the 2 segments
- When the pivot is in its final position in sorted array
	- Elements in position before pivot are less than pivot
	- Elements in position after pivot are greater than pivot
- Extremely fast in practice (faster than merge sort and does not require additional memory)
- Even if worst case occurs, performance is still acceptable for moderately large arrays
- Average case O($n\log{n}$)
- Worst case O($n^2$)
- Worst case can be avoided by careful choice of pivot
	- Some pivot selection can lead to worst case behaviour if array is already sorted or nearly sorted
	- Median of three pivot selection
		- Median of first, middle and last element

## Pseudocode (Assumes last index of each subarray is pivot)
```
partition(array, first, last): pivotIndex
	pivotIndex = last
	while (true)
		move left pointer to right until found a value greater than pivot (left pointer index cannot exceed last)
		move right pointer to left until found a value less than pivot (right pointer index cannot exceed first)
		if (leftPointer < rightPointer)
			swap element at left pointer with element at right pointer
			advance left pointer and right pointer
		else <- means normal d cuz element at left side is smaller than pivot and element at right side is greater than pivot
			break
	swap pivot with element at right pointer
	return pivotIndex = rightPointer index
end partition

quickSort(array, first, last = array length - 1)
	if (first > last) return <- exit condition
	pivotIndex = partition(array, first, last)
	quickSort(array, first, pivotIndex - 1) <- recurse on left subarray of pivot
	quickSort(array, pivotIndex + 1, last) <- recurse on right subarray of index
end quickSort
```

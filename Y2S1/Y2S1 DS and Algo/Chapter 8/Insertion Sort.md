- Partition array into sorted and unsorted region
- For every pass, take each item from unsorted region and insert it into correct order in sorted region
- Faster than bubble and selection sort, elements are shifted, no swapping occur
- Best case O(n)
- Average and Worst O($n^2$)
- Array closer to sorted order, insertion sort does less work, sort is more efficient
- Acceptable for small array sizes

## Pseudocode
```
sorted region is 0 at first, so unsorted starts from 1
for (unsorted = 1 to array length)
	currentUnsorted = array[unsorted] <- take reference first, later shift position will ovewrite the location
	look in the sorted region (which will be from 0 to unsorted - 1), as long as the element in the sorted region is bigger, shift it to right, else can stop and insert the unsorted element into position
	index = unsorted - 1
	while (index >= 0 and currentUnsorted < array[index])
		array[index + 1] = array[index] <- shift right
		index--
	array[index + 1] = currentUnsorted
```
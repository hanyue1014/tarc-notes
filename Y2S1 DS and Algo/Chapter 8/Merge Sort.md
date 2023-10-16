- Recursive standard sorting algorithm
- Give same performance regardless of initial order of array items
- Divide array into 2 half
- Keep dividing until each half only one element
- Merge the 2 half, sorting them while merging
- O($n\log{n}$) in all cases
- Disadvantage: need of a temporary array

## Pseudocode
```
mergeAndSort(array1, array2): resultArray
	resultArray length = array1 length + array2 length
	declare array1Pointer, array2Pointer, resArrayPointer
	while (array1Pointer < array1 length && array2Pointer < array2 length) <- traverse the two arrays when they both still have elements, compare them and put the smaller one in resultArray
		if (array1[array1Pointer] < array2[array2Pointer])
			resultArray[resArrayPointer++] = array1[array1Pointer++]
		else 
			resultArray[resArrayPointer++] = array2[array2Pointer++]
	copy all leftover of array1 into resultArray (if any)
	copy all leftover of array2 into resultArray (if any)
	return resultArray
end mergeAndSort

mergeSort(array)
	if (array length <= 1) return array <- base case, alrd divide till smallest
	midIndex = array length / 2
	leftArray = array[0 to midIndex]
	rightArray = array[midIndex to array length]
	leftSorted = mergeSort(leftArray)
	rightSorted = mergeSort(rightArray)
	return mergeAndSort(leftSorted, rightSorted)
end mergeSort
```
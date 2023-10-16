- Take the current element, go through the list and find the element smallest in list and swap position
- Advantage
	- Does not depend on initial arrangement of data
	- More efficient than bubble sort (one swap per pass)
- Disadvantage
	- Bad for large data

## Pseudocode (Iterative Approach)
```
for (pass = 0 to array length - 1) <- last element no need care, by the time reach there, should be no need to change it d
	find smallest element starting from pass + 1
	swap array[pass] and smallest element
```

## Pseudocode (Recursive Approach)
```
if (current < last)
	find smallest element starting from current + 1
	swap array[current] and smallest element
	recurse with current + 1, last
```
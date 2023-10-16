- Only applies to [[Sorted Lists|Sorted Lists/Arrays]]
- Repeatedly divide the list/array in half until element is found or nothing left to search

## General Idea
- Divide array in half, compare target with element at the array's mid point
- if match, target is found
- if target less than mid point, search left sub array
- if target more than mid point, search right sub array

## Efficiency
- Best case: O(1) desired item is the first item found
- Worst case: O(log n)
- Average case: O(log n)
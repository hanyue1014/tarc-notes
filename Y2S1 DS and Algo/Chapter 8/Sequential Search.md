- Search through list sequentially starting from the beginning

## For unsorted array
- Go through the elements one by one till found

## For sorted array
- Go through elements one by one
- If current element > element to find, confirm not found
- If current element == element to find, found

## Efficiency
- Best case O(1), search item at first location
- Worst case O(n), must traverse the whole list
- Average case O(n), traverse half the list {O(n/2) is still O(n)}

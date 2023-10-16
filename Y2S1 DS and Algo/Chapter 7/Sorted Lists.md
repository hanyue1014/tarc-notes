Topic: [[Y2S1 DS and Algo]]

- Objects is stored in a sorted order (in Java, requires class to implement the `Comparable` interface)

## Add Operation (Pseudocode)
```
declare index
while (index < size and newEntry > current element) <- finds suitable position for new entry
	index++
make room for new entry (shift all the elements after the newly found position to the right for array implementation, link to new entry and make new entry link to the original next entry for linked implementation)
size++
return true <- to indicate successful insertion
```

## Contains Operation (Pseudocode)
```
for (index = 0 to size)
	if (current element == entry to find)
		return true
	if (current element > entry to find) <- since is sorted so if we see things greater, than impossible can find d
		return false
return false
```

## Remove Operation (Pseudocode)
```
if (size == 0) return false
declare index
while (index < size and current element < entry to remove)
	index++ <- two cases, if the current element is already bigger than the entry to remove OR the current element IS the entry to remove
if (current element == entry to remove)
	remove gap to make the entry to remove kena garbage collected
	size--
	return true <- to indicate successful remove
return false <- unsuccessful remove since entry dont exist
```

- Known as Close Addressing
- Change the structure of the hash table so each location can represent multiple values
	- Each location is called a bucket
	- Buckets can be
		- List
		- Sorted list
		- Linked nodes
		- Array

## Advantages
- No need to search for empty cells
- Simple
- Efficient
- May require less number of searches to find the match should a collision happen
- Reduced complexity in deletion (no need take care about states)
- Table size do not need to be a prime number

- Locate an alternate location within the hash table
- New location must be open and available

## Linear Probing
- Adding
	- Search hash table sequentially for vacant cells
	- Increment index until available cell is found
	- If collision happen at location k, look at k + 1, k + 2, ... until an open and available location is found
	- When probing reach end of table, continues at the beginning
	- Actual sequence
		- Search probe sequence
		- Note first available slot
		- Use available slot if key is not found (the entry has not been inserted before)
- Retrieval
	- Find the index, compare with the key, if equal, return, else probe forward linearly until found
	- Stop search when key is found or null is reached
- Removal
	- Need use different states to distinguish the locations
		- Occupied
			- Location contains an entry
		- Empty
			- Location never been used, set with null
		- Available
			- Use some way to tell the location previously holds a entry, but currently does not
			- Because when probing, if a null is encountered, the chain will be broken cuz assuming null means uninitialised, then there is no need to probe forward since if got collision when the entry was inserted, the probe will continue
	- Search probe sequence
	- If key is found, mark location as available
- Advantage
	- Can reach every location in the hash table
		- Guarantees success of add operation if hash table is not full
- Disadvantage
	- Can cause primary clustering
		- A group of consecutive table locations are occupied
		- Tendency for a collision resolution scheme like linear probing to create long runs of filled slots near the hash position of keys
	- Primary clusters can combine and form large clusters
		- Can cause decrease in hash table efficiency

## Quadratic Probing
- Avoid primary clustering by changing the probe sequence
	- Search key, step is square of the step number
	- $k, k + 1^2, k + 2^2, k + 3^2, ..., k + n^2$
- Guarantees successful add operation if table is at most half full and table size is prime number
- Advantage
	- Eliminate primary clustering
- Disadvantage
	- Increased compute effort
	- Can cause secondary clustering
		- Tendency for a collision scheme like quadratic probing to create long runs of filled slots away from the hash position of the keys
		- All collision follow the same probing sequence

## Double Hashing
- Probably the better choice among the open addressing schemes
- Use 2 hash functions
- Search the hash table starting from location that the first hash function determines
- If collision occur, consider every nth location from original hash index, n is determined from a second hash function
- Second hash function should
	- Differ from the first hash function
	- Depend on search key
	- Return nonzero value
- Eg
	- HashFunc1: hashCode % size
	- HashFunc2: 5 - hashCode % 5
- Advantage
	- Reach every location in hash table if table size is prime
	- Avoid both primary and secondary clustering

## Problems of Open Addressing
- Frequent addition and removal cause every location in hash table to reference a current entry (occupied) or a former entry (available)
	- A hash table might have no location that contains null
	- Approach to search probe sequence will not work since every unsuccessful search only can end after considering every location in the hash table
- Solutions
	- [[Rehashing]]
	- [[Separate Chaining]]
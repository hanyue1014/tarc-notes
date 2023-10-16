- Maps the search key of an entry to a location that will contain the item
	- Search key can be either a primitive type or an instance of a class
- Primary functions
	- Return hash index of an entry in the hash table
		- Hash table: an array that contains the entries assigned by a hash function
- Perfect hash function maps each search key into a different integer suitable as an index to the hash table

## Steps
- Convert search key into integer [[Hash Codes]]
- Compress the hash code into the range of indices for the hash table (hash index)
	- Compress the hashCode given into hash index so it fits in the table
	- `hashCode % size`
	- If result < 0, add size to it to make it positive

## Characteristics of Good Hash Function
- Minimise collisions
- Distribute entries uniformly throughout the hash table
- Fast to compute

## Collision
- Happens when two keys give the same hash index when go through a hash function
- Solutions
	- Before the two below, package the entry with its search key, make them a pair with key and value
	- Use another location ([[Open Addressing]])
	- Change structure of hash table so each location can take multiple values ([[Separate Chaining]])

## Separate Chaining vs Open Addressing
- Separate Chaining > Open Addressing
	- Provide faster dictionary operation on average
	- Can use smaller hash table
	- Needs less frequent rehashing
- Open Addressing > Separate Chaining
	- Use less memory if both approach have same size array
		- Separate chaining use additional memory to maintain linked chains

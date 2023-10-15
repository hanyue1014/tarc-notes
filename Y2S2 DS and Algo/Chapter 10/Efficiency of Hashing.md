- Resolve collision takes time
	- So time complexity can be slower than O(1)
- As hash table filled up, collision occur more often, decreasing performance even further
- Collision resolution takes more time than evaluating hash function
	- Prime contributor to the cost of hashing

## Load Factor $\lambda$
- Used to express cost of hashing, by measuring how full a hash table is
- $\lambda = \dfrac{n}{l}$, where n is number of entries in dictionary and l is number of locations in hash table
- Restricting size improves performance of hashing
- Performance of hashing degrades as load factor increases, especially for [[Open Addressing]], since every operation require a search of probe sequence
- Maximum value
	- [[Open Addressing]] => 1 (hash table is full)
		- To maintain reasonable efficiency, keep $\lambda < 0.5$
	- [[Separate Chaining]] => no maximum value since hash table can technically never be full
		- Load factor is calculated differently as technically separate chaining has infinite number of locations
		- $\lambda = \dfrac{d}{c}$, where d is number of dictionary entries and c = number of chains (each location counted as one chain)
		- To maintain reasonable efficiency, keep $\lambda < 1$
- If load factor is too high to maintain the efficiency, must rehash the table
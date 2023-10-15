- Every object in java has a function called `hashCode`
	- Returns an integer hash code
	- Default implementation in java for every class is to return the memory address of the object
		- Not good for hashing because every objects will have very different hash codes
- If class's instance are to be used as search keys, `hashCode` should be overriden with suitable implementations

## Contracts for overriding hashCode
- If a class overrides the `equals` method, it should override `hashCode`
- If `equals` method considers two objects equal, the `hashCode` should return the same value for both objects
- Multiple calls to the `hashCode` of the same object should return the same hash code
- An object's hash code can be different when ran on the same program at different execution

## hashCode for Strings
- Add up each character's unicode value (nah)
- Multiply each character's unicode value with the character's position in the string then sum the products (hmmm mkay)
- Horner's method (wow)
```java
int hashCode(String s) {
	int hash = 0;
	for (int i = 0; i < s.length) {
		hash = g * hash + s.charAt(i); // where g is a random positive constant
	}
	return hash;
}
```

## hashCode for Primitives
- Manipulate internal binary representations
- Folding method
	- Break key into groups of digits then combine the groups using either addition or bitwise operator like XOR
	- Number of digits in each group should correspond to the size of the array
```
take: 
Key = 1111222233334444
Table size = 1009 (4 digits)
Since table size is 4 digits, the key should be separated into groups of 4 digits
1111, 2222, 3333, 4444
Add them tgt to get hashCode: 11110
Modulus with table size to get hashIndex: 11110 % 1009 = 11
```
## What
- Written in natural language
- Independent of any programming language (generic in nature)
- Collection ADT Specs: don't include implementation details

## What is included
- ADT Title
	- EG. List
- Description of the logical properties of the data type
	- EG. A list is used to store a group of objects. It will grow its size to accommodate the new elements and it will shrink its size when the elements are removed. It also allows retrieval of the elements by their index.
- Operation descriptions
	- Operation Header
		- return type (if any), operation name, parameter (if any)
		- `type name(param)`
		- EG. `T remove(Integer index)`
	- Brief description
		- What the operation does
		- EG. removes the element at the index
	- Precondition (if any)
		- Statement specifying condition that must be true before operation invoked
		- EG. index must be greater than 0 and less than the size of the list
	- Postcondition
		- Statement that is true after operation is completed
		- EG. the element at index is removed from the list and the elements that come after the list will be shifted left <- this i not too sure shifted left can use or not, but yinggai shi can eh
	- What is returned (if any)
		- EG. returns the element that is removed from the list

## Purpose
- Document the specifications of a new data structure in a **standard way** and is **generic**
- Allow this specification to be reused and implemented with any programming language 

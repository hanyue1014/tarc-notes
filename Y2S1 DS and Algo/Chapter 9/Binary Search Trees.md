- A search tree that organises its data so search is more efficient
- Contains `Comparable` objects
- Node's data is greater than every data in node's left subtree
- Node's data is less than every data in node's right subtree
- Efficiency depends on number of comparisons that a successful search requires (number of nodes along the path from root to the node searching for)
	- Height of a tree directly affects the length of the longest path from the root to a leaf, affects the efficiency of a worst case search

## Searching in BST
- Like [[Binary Search]] on sorted arrays
- Due to tree structure, searching is easier represented by a recursive algorithm
```
if (binarySearchTree is empty) return false
else if (object == current root) return true
else if (object < current root) return search(left subtree, desired Object) // use left node as root of left subtree
else return search(right subtree, desired object) // use right node as root of right subtree since if not equal and not less than then only can be greater than, search right side
```

## Adding Entry to BST
```
if (bst empty) root = new entry
else
	if (root == new entry) root = new entry
	else if (new entry < root)
		if (root.left != null)
			add(root.left, new entry)
		else
			root.left = new entry
	else if (new entry > root)
		if (root.right != null)
			add(root.right, new entry)
		else
			root.right = new entry
```
- If duplicates are allowed, place the duplicate as the [[Inorder Successor]]

## Removing entry
- 3 cases
	- Node has no children (most simple)
	- Node has one child
	- Node has 2 child

### Node has no child
- if node is left of parent, set parent's left reference to null
- if node is right of parent, set parent's right reference to null

### Node has one child
- Directly replace the node with the child

### Node has 2 child
- School way
	- Find the rightmost node (ignoring whether they have left subtree or not) of left subtree to replace the node
	- Delete the rightmost node of left subtree
- Alternative way
	- Find the [[Inorder Successor]] to replace the node
	- Delete the Inorder Successor

## Importance of Balance
- Completely balanced
	- Subtree of each node has exactly same height
- Height balanced
	- Subtree of each node in tree differ in height by no more than 1
- Balance of tree affects performance of the search process

> root left right
- Can be considered as a depth first traversal

## Steps
1. Visit root
2. Visit all nodes in left subtree
3. Visit all nodes in right subtree

## Preorder Iterator
```java
class PreItr implements Iterator<T> {
	QueueInterface<T> queue = new ArrayQueue<T>();
	
	// populate the queue when iterator is constructed so when next is called, directly get from the queue jiu can d
	public PreorderIterator() { preorder(root); }
	private void preorder(Node treeNode) {
		if (treeNode != null) {
			queue.enqueue(treeNode.value);
			preorder(treeNode.left);
			preorder(treeNode.right);
		}
	}
	public boolean hasNext() { return !queue.isEmpty(); }
	public T next() { return queue.isEmpty() ? null : queue.dequeue(); }
}
```
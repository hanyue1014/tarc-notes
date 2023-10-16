> left root right

## Steps
1. Visit all nodes in the root's left subtree
2. Visit root
3. Visit all nodes in root's right subtree

## Inorder Iterator
```java
class InItr implements Iterator<T> {
	QueueInterface<T> queue = new ArrayQueue<T>();
	
	// populate the queue when iterator is constructed so when next is called, directly get from the queue jiu can d
	public InorderIterator() { inorder(root); }
	private void inorder(Node treeNode) {
		if (treeNode != null) {
			inorder(treeNode.left);
			queue.enqueue(treeNode.value);
			inorder(treeNode.right);
		}
	}
	public boolean hasNext() { return !queue.isEmpty(); }
	public T next() { return queue.isEmpty() ? null : queue.dequeue(); }
}
```

> left right root

## Steps
1. Visit all nodes in the root's left subtree
2. Visit all nodes in the root's right subtree
3. Visit root

## Postorder Iterator
```java
class PostItr implements Iterator<T> {
	QueueInterface<T> queue = new ArrayQueue<T>();
	
	// populate the queue when iterator is constructed so when next is called, directly get from the queue jiu can d
	public PostorderIterator() { postorder(root); }
	private void postorder(Node treeNode) {
		if (treeNode != null) {
			postorder(treeNode.left);
			postorder(treeNode.right);
			queue.enqueue(treeNode.value);
		}
	}
	public boolean hasNext() { return !queue.isEmpty(); }
	public T next() { return queue.isEmpty() ? null : queue.dequeue(); }
}
```
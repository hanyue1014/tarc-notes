- Implemented with both head and tail references
- Item enqueued to back (tail reference) and dequeued from front (head reference)
- Traversal rarely needed
- Can be implemented with only reference to back (tail) (circular linked queue)
	- tail's next links to the frontmost node
	- When want dequeue (get front reference), use tail.next
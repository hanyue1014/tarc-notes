- Items can be added/removed anywhere
- Can be implemented with only a head reference or both head and tail references
- Traversing is needed for most operations

## Traversing LinkedList
- Use temporary reference to the currentNode
```java
currentNode = head;
while (currentNode != null) {
	doSomething.with(currentNode);
	currentNode = currentNode.next;
}
```

## Add Operation
```java
// kaki use while loop to loop until add position
currentNode = head;
head = new Node(value);
head.next = currentNode;
```

## Remove Operation
```java
// kaki use loop to loop until remove position
head.next = head.next.next;
```
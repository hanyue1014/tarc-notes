> The \<T> represents a [[Java Generic]] type

```java
// this interface is not complete, I lazy d
public interface ListInterface<T> {
	/***
	 * @param newEntry object added to the list as new entry
	 * @return true if insert successful, false if failed
	 */
	public abstract boolean add(T newEntry);
}
```
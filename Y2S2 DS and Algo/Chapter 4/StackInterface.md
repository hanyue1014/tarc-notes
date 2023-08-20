> The \<T> is a [[Java Generic]]
```java
public interface StackInterface<T> {
	public abstract boolean push(T newEntry);
	public abstract T pop();
	public abstract T peek();
	public abstract boolean isEmpty();
	public abstract void clear();
}
```

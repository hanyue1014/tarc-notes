- Used in Java interface and classes which implements [[ADT & DS#Collection ADT |Collection ADT]] to specify and constraint the type of objects stored in the collection
```java
public interface Interface<T>
public class Class<T>
```
- The identifier `<T>` can be any identifier, but usually is just a single capital letter, the T will be replaced by whatever the class data passed in
- When using, need to supply actual Class argument to replace T
```java
Interface<String> eg;
```
# Abstract Class vs Interface

## One Distinctive Difference (Litmus Test)
- **Abstract Class**: Use when you need shared state/behavior across subclasses.
- **Interface**: Use when you need to declare a capability/contract that many unrelated types can support. (Interfaces can't have properties)

### Abstract Class
- Shares attributes (state) and some behaviors, but some specifics differ.
- Can provide default method implementations.
- Can have constructors.
- Can define access modifiers (public, protected, private).
- Supports single inheritance (a class can extend only one abstract class).
- Used for core identity + shared behavior (e.g., `Animal`).
- Can contain both abstract methods (no implementation) and concrete methods (with implementation).

### Interface
- Use for capabilities/features (e.g., `Fly`, `Swim`).
- Only method signatures (no implementation, except default/static methods in some languages).
- Cannot have constructors.
- Cannot define access modifiers for members (all are public by default).
- Supports multiple inheritance (a class can implement multiple interfaces).
- Used to define a contract that unrelated classes can follow.
- Cannot have fields/attributes (except constants).

---

## Summary Table
| Feature                | Abstract Class         | Interface                |
|------------------------|-----------------------|--------------------------|
| Shared State           | Yes                   | No                       |
| Shared Behavior        | Yes                   | No (only method signatures) |
| Default Implementation | Yes                   | No (except default/static methods) |
| Constructors           | Yes                   | No                       |
| Access Modifiers       | Yes                   | No                       |
| Multiple Inheritance   | No (single)           | Yes                      |
| Fields/Attributes      | Yes                   | No (except constants)     |
| Use Case               | Core identity         | Capabilities/Features    |

# Abstract Class vs Concrete Class

## Abstract Class
- Instantiating the entity doesn't make sense as the entity would not be complete in itself.
- Use when you want shared code + must-implement rules.
- Acts as a “template” for subclasses.
 - Can contain both abstract methods (no implementation) and concrete methods (with implementation).
 - Can have fields/attributes and constructors.
 - Forces subclasses to implement certain methods.
 - Cannot be instantiated directly.

### Why Abstract Classes Have Constructors
Although you cannot instantiate an abstract class directly, its constructor is still important. When a concrete subclass is instantiated, the abstract class's constructor is called (usually via `super()`), allowing shared state or setup logic to be initialized before the subclass adds its own initialization. This ensures that all common attributes and behaviors defined in the abstract class are properly set up for every subclass instance.

## Concrete Parent Class
- Use when you have a fully working default implementation.
- Subclasses just “specialize” behavior optionally.
- The base behavior is complete and usable.
- You don’t need to force subclasses to implement anything.
- Can be instantiated directly.
- Can have fields/attributes, constructors, and fully implemented methods.
- Subclasses inherit and may override behavior, but are not required to.

---

## Summary Table
| Feature                | Abstract Class         | Concrete Class           |
|------------------------|-----------------------|--------------------------|
| Instantiable           | No                    | Yes                      |
| Shared Code            | Yes                   | Yes                      |
| Must-Implement Rules   | Yes                   | No                       |
| Abstract Methods       | Yes                   | No                       |
| Concrete Methods       | Yes                   | Yes                      |
| Fields/Attributes      | Yes                   | Yes                      |
| Constructors           | Yes                   | Yes                      |
| Use Case               | Template for subclasses| Usable as-is             |

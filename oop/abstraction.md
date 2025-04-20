
---

# 🎯 OOP Pillar: Abstraction

## 🧠 What is Abstraction?

**Abstraction** in Object-Oriented Programming is the process of defining **essential behavior** in a class without providing its full implementation. It helps developers:

- Simplify complex systems by focusing on high-level design.
- Prevent code duplication and inconsistency in class hierarchies.
- Enforce a structure where subclasses must implement specific behaviors.

---

## 🧱 Using Abstraction in Python

Python provides abstraction through the **`abc` module** with `ABC` (Abstract Base Class) and the `@abstractmethod` decorator.

### 🧪 Example:

```python
from abc import ABC, abstractmethod

class Animal(ABC):
  def __init__(self, name):
    self.name = name

  @abstractmethod
  def make_noise(self):
    pass

class Cat(Animal):
  def make_noise(self):
    print(f"{self.name} says, Meow!")

class Dog(Animal):
  def make_noise(self):
    print(f"{self.name} says, Woof!")
```

- `Animal` is an abstract class — it **cannot** be instantiated directly.
- It defines a required method `.make_noise()` without an implementation.
- Subclasses like `Cat` and `Dog` must **implement** `.make_noise()`.

### ❌ Instantiating Abstract Class:

```python
an_animal = Animal("Scruffy")
# TypeError: Can't instantiate abstract class Animal with abstract method make_noise
```

---

## ✅ Benefits of Abstraction

- **Defines consistent behavior** across all subclasses.
- **Improves code clarity** by hiding unnecessary implementation details.
- **Forces implementation** of key methods in subclasses, reducing logical errors.

Abstraction is essential for designing well-structured, maintainable, and scalable object-oriented systems.

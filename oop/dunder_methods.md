
---

# ✨ Dunder Methods in Python

## 🧠 What Are Dunder Methods?

**Dunder methods** (short for *Double UNDERscore*) are special methods in Python that begin and end with double underscores, such as `__init__()` and `__repr__()`. These methods allow customization of object behavior and are often used to enable **operator overloading**, a form of polymorphism.

---

## ➕ Operator Overloading

Python uses dunder methods behind the scenes to define how operators behave for different data types:

```python
# For an int and an int, '+' returns an int
2 + 4 == 6

# For a string and a string, '+' returns a string
"Is this " + "addition?" == "Is this addition?"

# For a list and a list, '+' returns a list
[1, 2] + [3, 4] == [1, 2, 3, 4]

```

The `+` operator acts differently depending on the object types — this is **operator overloading**.

---

## 🧪 Custom Example with Dunder Methods

```python
class Animal:
  def __init__(self, name):
    self.name = name

  def __repr__(self):
    return self.name

  def __add__(self, another_animal):
    return Animal(self.name + another_animal.name)

a1 = Animal("Horse")
a2 = Animal("Penguin")
a3 = a1 + a2

print(a1)  # Output: Horse
print(a2)  # Output: Penguin
print(a3)  # Output: HorsePenguin
```

### 🔍 Explanation:
- `__repr__()` customizes how the object is printed.
- `__add__()` defines the behavior of the `+` operator, allowing two `Animal` instances to be combined into a new one.

---

## ✅ Key Takeaways

- Dunder methods are used to define special behaviors in classes.
- They enable **operator overloading**, letting you reuse operators like `+`, `-`, etc., for custom objects.
- This feature enhances code **flexibility**, **readability**, and **polymorphism** in Python.

Understanding and using dunder methods allows developers to create more intuitive and expressive class interfaces.

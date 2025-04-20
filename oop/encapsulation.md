
---

# 🔐 OOP Pillar: Encapsulation

## 🧠 What is Encapsulation?

**Encapsulation** is the principle of **hiding an object’s internal data and behavior**, exposing only what is necessary for external interaction. It helps:

- Protect internal object state
- Enforce data integrity
- Promote modular design

---

## 🔒 Access Modifiers

Languages like Java and C++ enforce access levels using **modifiers**:
- **Public** – accessible from anywhere.
- **Protected** – accessible only within the same module or subclass.
- **Private** – accessible only within the class.

### 🐍 Python’s Approach

Python does **not** enforce strict access control but follows conventions:

| Convention      | Example        | Purpose                                           |
|----------------|----------------|---------------------------------------------------|
| Public          | `self.name`     | Fully accessible                                  |
| Protected       | `self._name`    | Developer-convention; should not be accessed directly |
| Private         | `self.__name`   | Uses **name mangling** to discourage access       |

---

## 🔧 Name Mangling in Python

Private members (`__member`) are transformed by Python to:

```python
obj._ClassName__member
```

This prevents accidental access or name clashes in subclasses, though it does **not** fully restrict access.

> ⚠️ Note: This is **different** from dunder methods like `__init__()` or `__repr__()`, which are not mangled and serve specific built-in purposes.

---

## ✅ Summary

Encapsulation in Python is achieved through naming conventions and mechanisms like **name mangling**. While not strictly enforced, it is a powerful tool for:

- Protecting class internals
- Maintaining clean, understandable interfaces
- Avoiding conflicts in inheritance hierarchies

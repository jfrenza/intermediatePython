
---

# 📘 Introduction to Object-Oriented Programming (OOP)

## 🧠 What is a Programming Paradigm?

A **programming paradigm** is a way to classify programming languages based on their features and the style of programming they support. Python, like many modern languages, supports multiple paradigms, including:

- Imperative programming
- Functional programming
- **Object-Oriented Programming (OOP)**

---

## 🧱 Focus: Object-Oriented Programming (OOP)

OOP is a paradigm that structures code around **classes** and **objects**. It allows for modeling real-world entities by bundling data and behavior together.

### 🔍 Example:
```python
class Dog:
  sound = "Woof"

  def __init__(self, name, age):
    self.name = name
    self.age = age

  def bark(self):
    print(Dog.sound)
```

In this example:
- `Dog` is a **class**
- `name` and `age` are **attributes**
- `bark()` is a **method**
- Instances of `Dog` represent **objects**

---

## 🧩 Why Use OOP?

- Organizes code more efficiently
- Promotes code reuse
- Makes programs more scalable and maintainable

---

## 🔑 The Four Pillars of OOP

We will explore the following concepts in detail:

1. **Inheritance** – Reuse behavior from existing classes  
2. **Polymorphism** – Use a common interface for different data types  
3. **Abstraction** – Hide complex implementation details  
4. **Encapsulation** – Restrict direct access to some components

---

## 📝 Final Note

Understanding and applying these OOP principles will enhance your ability to build powerful and organized Python programs. This introduction serves as a foundation for deeper exploration in future lessons.

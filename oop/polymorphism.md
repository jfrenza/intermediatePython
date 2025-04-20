
---

# 🧬 OOP Pillar: Polymorphism

## 📖 What is Polymorphism?

**Polymorphism** in Object-Oriented Programming refers to the ability to use a single method or operation across different object types. This allows for flexible and dynamic code, especially when the exact object type may not be known at runtime.

---

## 🐾 Example of Polymorphism in Python

```python
class Animal:
  def __init__(self, name):
    self.name = name

  def make_noise(self):
    print(f"{self.name} says, Grrrr")

class Cat(Animal):
  def make_noise(self):
    print(f"{self.name} says, Meow!")

class Robot:
  def make_noise(self):
    print("beep.boop...BEEEEP!!!")
```

Each class defines a `make_noise()` method, but the behavior differs based on the class.

---

## 🧪 Using Polymorphism

```python
an_animal = Animal("Bear")
my_pet = Cat("Maisy")
my_vacuum = Robot()

objects = [an_animal, my_pet, my_vacuum]

for o in objects:
  o.make_noise()
```

### 🔊 Output:
```
Bear says, Grrrr  
Maisy says, Meow!  
beep.boop...BEEEEP!!!
```

The same method name is used on different object types without needing to check their class — this is **polymorphism in action**.

---

## ✅ Benefits of Polymorphism

- **Simplifies code** by treating different objects uniformly
- **Increases flexibility** and reusability of functions
- **Supports dynamic behavior** during runtime

Polymorphism allows for cleaner, more extensible code — a key aspect of writing maintainable object-oriented programs.

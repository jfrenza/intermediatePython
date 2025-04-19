
---

# 🔍 Introduction to Scope in Python

---

## 🌐 Namespaces vs. Scope

- **Namespaces** are **containers** that map names to objects.
- **Scope** is the **rule system** that determines **which namespaces** are accessible **at a specific point** in the program.

---

## ❗ Example: Why Scope Matters

```python
def printColor():
    color = 'red'

print(color)
```

🧨 Output:
```
NameError: name 'color' is not defined
```

- Even though `color` is defined inside the function, it **cannot be accessed outside** because of **scope limitations**.

---

## 📚 Scope: The Access Rules

Python defines **four levels of scope**, which determine **where** a name can be **seen**:

1. **Built-in Scope** – Names preloaded by Python (e.g., `print`, `str`)  
2. **Global Scope** – Names defined at the top-level of a module  
3. **Enclosing Scope** – Names in enclosing functions (for nested functions)  
4. **Local Scope** – Names defined within the current function  

---

## 💡 Key Concept

- **Namespace** = *Storage* of names  
- **Scope** = *Access control* to those names

Understanding scope helps avoid runtime errors like `NameError` and ensures proper variable accessibility throughout the code.

---
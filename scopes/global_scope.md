### 🌍 Global Scope

The **global scope** in Python refers to names (variables, functions, etc.) defined at the **top level of a script or module**. These names belong to the **global namespace** and can be **accessed from anywhere** in the same file, including inside functions.

---

#### ✅ Example – Accessing a Global Variable:
```python
gravity = 9.8  # Global scope

def get_force(mass):
    return mass * gravity  # Accessing global variable

print(get_force(60))  # Output: 588.0
```

---

#### ⚠️ Limitation – Cannot Modify Directly:
While you can read a global variable inside a function, **you cannot modify it** directly without an explicit declaration. Doing so causes Python to treat the variable as **local**, resulting in an error.

```python
gravity = 9.8

def get_force(mass):
    gravity += 100  # ❌ Treated as a local variable – causes an error
    return mass * gravity

print(get_force(60))
```

**Error:** `UnboundLocalError: local variable 'gravity' referenced before assignment`

---

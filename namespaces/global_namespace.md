
---

# 🌐 Global Namespace in Python

---

## 🔹 What is the Global Namespace?

- The **global namespace** sits **one level below the built-in namespace**.
- It contains all **non-nested names** defined at the **top-level of a Python script** (e.g., variables, functions, imports).

---

## 🧾 When Is It Created?

- The global namespace is created when the **main program starts running**.
- It exists **until the interpreter terminates** (i.e., the program ends).

---

## 📁 Example

```python
import random

first_name = "Jaya"
last_name = "Bodegard"

def print_variables():
    random_number = random.randint(0, 9)
    print(first_name)
    print(last_name)
    print(random_number)
```

- Variables like `first_name`, `last_name`, and the function `print_variables()` are part of the **global namespace**.

---

## 🔍 Viewing the Global Namespace

Use the built-in function `globals()` to inspect it:

```python
print(globals())
```

- This returns a **dictionary** of all names and objects in the global namespace.
- Note: `globals()` is itself a **built-in function**, meaning it comes from the built-in namespace.

---

## 💡 Summary

- The global namespace stores all top-level definitions in a module.
- Accessible throughout the script unless shadowed by local names.
- Helpful for debugging and introspection with `globals()`.

---
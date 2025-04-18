
---

# 🧠 Built-in Namespace in Python

---

## 🔹 What is the Built-in Namespace?

- The **built-in namespace** is one of the **four main types** of namespaces in Python.
- It contains **core functions, exceptions, and objects** that are **always available** in any Python program.

---

## 🧰 Examples of Built-in Functions

Functions like:

- `print()`
- `str()`
- `len()`
- `int()`

...are part of the built-in namespace. That’s why we can use them **without importing** any module.

---

## 🕒 Lifetime of the Built-in Namespace

- Created **when the Python interpreter starts**
- Exists **until the interpreter terminates** (i.e., until the program ends)

---

## 🔍 Viewing Built-in Namespace

To inspect available built-in names, use:

```python
print(dir(__builtins__))
```

This command lists all the objects defined in Python's built-in namespace.

---

## 💡 Summary

- The **built-in namespace** is automatically loaded.
- It provides **immediate access** to essential tools for Python development.
- No need to import modules to use its contents.

---
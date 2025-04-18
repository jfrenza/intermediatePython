
---

# 🏷️ Introduction to Names and Namespaces in Python

---

## 🔠 What is a Name?

- A **name** (or **symbolic name**) in Python is an **identifier** that references an **object**.
- Example:

```python
color = "cyan"
```

Here, `color` is the name assigned to the string `"cyan"`.

---

## 📦 What is a Namespace?

- A **namespace** is a **collection of names and their corresponding objects**.
- Internally, Python maintains a **dictionary** where:
  - **Keys** = names (identifiers)
  - **Values** = referenced objects

### 🧪 Example Namespace

```python
{'color': 'cyan'}
```

When executing:

```python
print(color)
```

Python looks up `color` in the current namespace and returns `'cyan'`.

---

## 🧭 Why Namespaces Matter

- Namespaces allow Python to keep track of all the variables, functions, and objects in a program—often **hundreds or thousands**.
- They help **avoid name conflicts** and ensure that the correct value is accessed at the right time.

---

## 🧩 Types of Namespaces (To Be Explored)

1. **Built-in** – Provided by Python itself (e.g., `len`, `print`)
2. **Global** – Defined at the top-level of a module
3. **Local** – Defined inside a function
4. **Enclosing** – From outer functions in nested functions

---

Namespaces are essential for understanding variable scope and memory management in Python.

---
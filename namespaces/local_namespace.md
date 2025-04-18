
---

# 🧭 Local Namespace in Python

---

## 🔹 What Is the Local Namespace?

- The **local namespace** is created **whenever a function is called**.
- It contains **all variable names and parameters** defined **within that function**.
- It only exists **while the function is executing** and is **discarded after**.

---

## 📁 Example

```python
global_variable = 'global'

def add(num1, num2):
    nested_value = 'Inside Function'
    print(num1 + num2)
    print(locals())

add(5, 10)
```

### Output:
```
15
{'num1': 5, 'num2': 10, 'nested_value': 'Inside Function'}
```

- `locals()` reveals the local namespace inside the function.
- Includes: parameters `num1`, `num2` and local variable `nested_value`.
- **Does not include** `global_variable`, which belongs to the **global namespace**.

---

## 🔍 Viewing the Local Namespace

- Use the built-in `locals()` function **inside a function** to inspect local variables.
- If `locals()` is called **outside** a function, it behaves like `globals()`.

---

## 💡 Summary

- Local namespaces are **temporary** and **function-specific**.
- They help **isolate variables** during function execution.
- Useful for **debugging** and **introspection** using `locals()`.

---
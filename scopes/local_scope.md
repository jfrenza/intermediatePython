
---

### 🧭 Local Scope

In Python, a **local scope** is created **whenever a function is called**. Any variables defined inside that function exist **only within its local namespace**.

- **Local names are inaccessible outside the function.**
- If you try to access a locally defined variable from outside its function, Python will raise a `NameError`.
- Local variables are temporary—they exist **only during the function's execution**.

**Example:**

```python
def favorite_color(): 
  color = 'Red'

print(color)  # ❌ Error: 'color' is not defined outside the function
```

To avoid the error, place the `print()` inside the function:

```python
def favorite_color(): 
  color = 'Red'
  print(color)  # ✅ This works and prints 'Red'

favorite_color()
```

---

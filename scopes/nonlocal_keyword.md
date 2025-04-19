
---

### 🔁 The `nonlocal` Keyword

The `nonlocal` keyword in Python allows **modification of variables in an enclosing (nonlocal) scope**, specifically within **nested functions**.

By default, if you try to assign a value to a variable defined in an outer (but non-global) function, Python will treat it as **local to the inner function**, causing an error if the variable is immutable (like a string or number). To solve this, you use `nonlocal`.

#### 🔑 Purpose:
- To **modify** a variable in an **enclosing (non-global)** function scope.

---

#### ✅ Example – Without `nonlocal` (Error):
```python
def outer():
    count = 0

    def inner():
        count += 1  # ❌ Error: count is treated as local

    inner()
    print(count)

outer()
```
**Error:** `UnboundLocalError`

---

#### ✅ Example – With `nonlocal` (Correct):
```python
def outer():
    count = 0

    def inner():
        nonlocal count
        count += 1  # ✅ Now count refers to the enclosing scope

    inner()
    print(count)

outer()
```
**Output:** `1`

---

#### 🚫 Notes:
- `nonlocal` only works with variables from **enclosing scopes**, not **global** ones.
- It is useful in **closures** and **decorators**, where inner functions need to update outer variables.

---

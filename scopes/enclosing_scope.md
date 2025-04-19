
---

### 🌀 Enclosing (Nonlocal) Scope

**Enclosing scope**, also known as **nonlocal scope**, applies to **nested functions**. It allows **inner functions** to access variables defined in their **immediate outer function**.

#### 🔑 Key Points:
- A nested (inner) function **can access**, but **cannot modify**, variables from the enclosing function.
- Scope flows **downward**: nested functions can see outward variables, but outer functions **cannot** access variables defined in their nested functions.
- This rule supports the concept of **nonlocal access**, but not nonlocal mutation for **immutable objects** (e.g., strings, numbers).

#### ✅ Example – Valid Access:
```python
def outer_function():
    enclosing_value = 'Enclosing Value'

    def nested_function():
        print(enclosing_value)  # ✅ Accesses variable from outer function

    nested_function()

outer_function()
```
**Output:** `Enclosing Value`

#### ❌ Example – Invalid Upward Access:
```python
def outer_function():
    print(nested_value)  # ❌ Error: not defined yet

    def nested_function():
        nested_value = 'Nested Value'

    nested_function()

outer_function()
```
**Output:** `NameError`

#### ❌ Example – Attempt to Modify Enclosing Variable:
```python
def outer_function():
    enclosing_value = 'Enclosing Value'

    def nested_function():
        enclosing_value += ' changed'  # ❌ Error: cannot modify immutable

    nested_function()
    print(enclosing_value)

outer_function()
```
**Output:** `UnboundLocalError`

---

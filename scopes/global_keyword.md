
---

### 🔑 `global` Keyword

The `global` keyword in Python is used **inside a function** to indicate that a variable refers to the one defined in the **global scope**, not a new local variable. This allows a function to **modify a global variable** rather than creating a local copy.

---

#### ✅ Example – Using `global` to Modify a Global Variable:
```python
counter = 0  # Global variable

def increment():
    global counter  # Declare we're referring to the global 'counter'
    counter += 1

increment()
print(counter)  # Output: 1
```

Without the `global` keyword, trying to modify `counter` inside the function would result in an `UnboundLocalError` because Python assumes it's a local variable.

---

#### 🔍 Key Points:
- Use `global` only when **modifying** a global variable.
- Reading a global variable **does not require** the keyword.
- Overusing `global` can lead to **hard-to-track side effects**, so it should be used **sparingly** and with caution.
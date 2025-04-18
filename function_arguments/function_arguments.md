
---

# 🧠 Python Function Arguments: A Recap

In Python, functions can accept arguments in **three main ways**:

---

## 1. 📍 Positional Arguments

Arguments passed **in order**, based on their position in the function definition.

```python
def print_name(first_name, last_name): 
    print(first_name, last_name)

print_name('Jiho', 'Baggins')
```

🔹 `first_name` gets `'Jiho'`  
🔹 `last_name` gets `'Baggins'`

✅ **Order matters** when using positional arguments.

---

## 2. 🏷️ Keyword Arguments

Arguments are passed using **parameter names**, allowing for more flexibility.

```python
def print_name(first_name, last_name): 
    print(first_name, last_name)

print_name(last_name='Baggins', first_name='Jiho')
```

🔹 You **explicitly specify** which value goes to which parameter.  
🔹 **Order does not matter**, as long as parameter names are used correctly.

---

## 3. ⚙️ Default Arguments

Parameters can be assigned **default values** in the function definition.

```python
def print_name(first_name='Jiho', last_name='Baggins'): 
    print(first_name, last_name)

print_name()
```

🔹 If **no arguments are passed**, the defaults are used.  
🔹 You can still override them by providing values.

---

## 🧩 Summary Table

| Argument Type       | Order Matters? | Can Skip When Calling? | Uses Names?       |
|---------------------|----------------|-------------------------|-------------------|
| Positional          | ✅ Yes          | ❌ No                   | ❌ No              |
| Keyword             | ❌ No           | ❌ No                   | ✅ Yes             |
| Default             | ✅/❌ Depends   | ✅ Yes (if default set) | ✅ Optional        |

---

Use these argument types strategically for clarity, flexibility, and functionality in your Python functions.

---
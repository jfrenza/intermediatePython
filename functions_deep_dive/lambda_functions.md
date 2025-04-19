
---

# 🔹 Lambda Functions in Python

In Python, a **lambda function** is a small, anonymous function created using the `lambda` keyword. It is used when you need a simple function for a short period and don't want to formally define it with `def`.

---

## 🧠 Syntax

The general syntax of a lambda function is:

```python
lambda arguments: expression
```

- It can take any number of arguments (including none)
- It **must** contain a single expression (not multiple lines)
- The result of the expression is **automatically returned**

---

## ✅ Basic Examples

### 1. No Arguments

```python
greet = lambda: "Hello!"
print(greet())  # Output: Hello!
```

---

### 2. Single Argument

```python
double = lambda x: x * 2
print(double(4))  # Output: 8
```

---

### 3. Multiple Arguments

```python
add = lambda a, b: a + b
print(add(3, 5))  # Output: 8
```

---

### 4. Conditional Expression

```python
max_value = lambda x, y: x if x > y else y
print(max_value(10, 7))  # Output: 10
```

---

## ⚠️ Notes and Limitations

- Lambda functions are **limited to a single expression** — no multiple statements or complex logic.
- They are useful for quick, one-time tasks, but for reusable or complex functions, prefer using `def`.

---

## 📝 Conclusion

Lambda functions are a concise way to write simple, unnamed functions in Python. They’re ideal for short operations where defining a full function would be unnecessary.

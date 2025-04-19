
---

# 📚 Python Decorators

A **decorator** in Python is a design pattern that allows you to modify or extend the behavior of a function or method without modifying its actual code. This is useful for adding reusable functionality to different functions.

---

## 📌 Key Concepts

- **Functions as First-Class Objects**:  
  In Python, functions can be passed as arguments, returned from other functions, and assigned to variables, which is a key feature that makes decorators possible.

- **What is a Decorator?**:  
  A decorator is a function that takes another function as an argument and returns a new function that typically extends or modifies the behavior of the original function.

---

## 📂 Decorator Syntax

A decorator is applied using the `@decorator_name` syntax directly above the function definition.

### Example:

```python
def my_decorator(func):
    def wrapper():
        print("Before function call")
        func()
        print("After function call")
    return wrapper

@my_decorator
def say_hello():
    print("Hello!")

say_hello()
```

**Output:**
```
Before function call
Hello!
After function call
```

### How it Works:
- `my_decorator` takes the `say_hello` function as an argument.
- The `wrapper` function inside `my_decorator` adds behavior before and after `say_hello()` is executed.
- `@my_decorator` is shorthand for passing `say_hello` to `my_decorator`.

---

## 📂 Decorators with Arguments

When the decorated function accepts arguments, the decorator's wrapper function must handle those using `*args` and `**kwargs`.

### Example:

```python
def my_decorator(func):
    def wrapper(*args, **kwargs):
        print("Before function call")
        result = func(*args, **kwargs)
        print("After function call")
        return result
    return wrapper

@my_decorator
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")
```

**Output:**
```
Before function call
Hello, Alice!
After function call
```

---

## 📂 Common Use Cases for Decorators

1. **Logging**: Automatically log function calls and results.
2. **Authentication**: Check if a user has the correct permissions before running a function.
3. **Caching/Memoization**: Cache expensive function results to improve performance.
4. **Function Enrichment**: Add pre- or post-processing steps to a function's execution.

---

## 📂 Built-in Python Decorators

Python offers some built-in decorators that are commonly used:
- `@staticmethod`: Used to define a static method in a class.
- `@classmethod`: Defines a class method that takes the class as the first argument.
- `@property`: Allows you to define a method as a property in a class.

---

## 📌 Summary

Decorators are a powerful feature in Python, allowing functions to be extended or modified without altering their actual code. They are ideal for situations like logging, authentication, or modifying function behavior across an entire project.

By understanding and using decorators, you can keep your code clean, reusable, and maintainable while adding additional functionality with ease.

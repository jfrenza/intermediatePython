
---

# 🧠 Python Built-in Higher-Order Functions: `map()`, `filter()`, and `reduce()`

In Python, **higher-order functions** are those that either take other functions as arguments or return them. Three of the most useful built-in higher-order functions are `map()`, `filter()`, and `reduce()`. These functions are widely used for functional programming paradigms in Python.

---

## 📌 `map(function, iterable)`
The `map()` function applies a given function to all items in an iterable (like a list or a tuple). It returns an iterator that yields the results.

### **Syntax**:
```python
map(function, iterable)
```

### **Example**:
```python
# Convert all strings in a list to uppercase
words = ["apple", "banana", "cherry"]
uppercase_words = list(map(str.upper, words))

print(uppercase_words)
# Output: ['APPLE', 'BANANA', 'CHERRY']
```

### **Explanation**:
- `map()` takes a function (in this case, `str.upper`) and applies it to each element in the iterable (the list of words).
- The result is an iterator, so we convert it to a list to view the output.

---

## 📌 `filter(function, iterable)`
The `filter()` function constructs an iterator from elements of an iterable for which the function returns `True`.

### **Syntax**:
```python
filter(function, iterable)
```

### **Example**:
```python
# Filter out negative numbers from a list
numbers = [-2, 3, 0, -1, 5]
positive_numbers = list(filter(lambda x: x > 0, numbers))

print(positive_numbers)
# Output: [3, 5]
```

### **Explanation**:
- `filter()` uses the function (in this case, `lambda x: x > 0`) to test each element of the iterable (`numbers`).
- Only the elements for which the function returns `True` are kept in the resulting iterator.

---

## 📌 `reduce(function, iterable)`
The `reduce()` function, available in the `functools` module, applies a rolling computation to the items of an iterable, reducing it to a single value.

### **Syntax**:
```python
from functools import reduce
reduce(function, iterable)
```

### **Example**:
```python
from functools import reduce

# Sum all the numbers in a list
numbers = [1, 2, 3, 4]
result = reduce(lambda x, y: x + y, numbers)

print(result)
# Output: 10
```

### **Explanation**:
- `reduce()` takes a binary function (in this case, `lambda x, y: x + y`) and applies it cumulatively to the items in the iterable (`numbers`).
- The result is a single value that accumulates the result of the operation.

---

## 📝 **Key Differences**:

- **`map()`**: Transforms each element in an iterable using a function.
- **`filter()`**: Filters out elements from an iterable based on a condition.
- **`reduce()`**: Reduces an iterable to a single value by applying a binary function cumulatively.

---

## 🔄 **Conclusion**:
These functions allow you to write more concise and functional-style Python code, making your programs cleaner and more modular. They are particularly useful when working with iterables and can be combined with lambda functions for greater flexibility.

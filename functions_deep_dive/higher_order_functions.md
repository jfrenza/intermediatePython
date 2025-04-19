
---

### 🔁 Introduction to Higher-Order Functions

**Higher-order functions** are functions that **either accept other functions as arguments, return functions as values, or both**. They are made possible because in Python, **functions are first-class objects**, meaning they can be treated like any other variable.

---

### 🧩 Functions as First-Class Objects

Functions in Python can:
- Be assigned to variables
- Be passed as arguments
- Be returned by other functions
- Be stored in data structures

This flexibility allows us to build more modular and reusable code.

---

### ⚙️ Using Functions as Arguments

A higher-order function can take another function as input.  
For example:

```python
def total_bill(func, value):
    total = func(value)
    return total
```

You can pass different behavior via function arguments:

```python
def add_tax(total):
    return total + total * 0.06

def add_tip(total):
    return total + total * 0.20

print(total_bill(add_tax, 100))  # Output: 106.0
print(total_bill(add_tip, 100))  # Output: 120.0
```

This becomes more useful when you add consistent formatting or apply it to lists:

```python
def total_bills(func, list_of_bills):
    new_bills = []
    for amount in list_of_bills:
        total = func(amount)
        new_bills.append(f"Total amount owed is ${total:.2f}. Thank you! :)")
    return new_bills
```

---

### 🔄 Returning Functions from Functions

A higher-order function can also **return another function**:

```python
def make_box_volume_function(height):
    def volume(length, width):
        return length * width * height
    return volume

box_volume_10 = make_box_volume_function(10)
print(box_volume_10(3, 2))  # Output: 60
```

This technique helps encapsulate configuration and reduce repetition.

---

### ✅ Summary

- **Higher-order functions** work with other functions: they accept or return them.
- They are made possible because **functions are first-class objects**.
- They improve modularity, reusability, and readability.
- Examples include `total_bill()`, `total_bills()`, and `make_box_volume_function()`.

These concepts pave the way for using built-in tools like `map()`, `filter()`, and more.

--- 

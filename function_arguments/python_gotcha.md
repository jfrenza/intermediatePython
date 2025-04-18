
---

# 🐍 Python Gotcha: Mutable Default Arguments

## 🔍 What Is a Python Gotcha?
A **gotcha** is a behavior in a programming language that is surprising or unintuitive. In Python, a common gotcha arises when using **mutable objects as default arguments** in function definitions.

---

## 💥 The Problem

```python
def createStudent(name, age, grades=[]):
    return {
        'name': name,
        'age': age,
        'grades': grades
    }
```

### Example Usage

```python
chrisley = createStudent('Chrisley', 15)
dallas = createStudent('Dallas', 16)

def addGrade(student, grade):
    student['grades'].append(grade)
    print(student['grades'])

addGrade(chrisley, 90)
addGrade(dallas, 100)
```

### ❌ Unexpected Output:
```
[90]
[90, 100]
```

Both students **share the same list** for `grades`! This is because the default list is created only once—when the function is defined—not each time it is called.

---

## 🧠 Why It Happens

- **Mutable objects** like lists, dicts, and sets can be **modified in place**.
- In function definitions, **default values are evaluated only once**.
- Therefore, using a mutable object like `[]` will cause all function calls that rely on the default to share the same object.

---

## ✅ The Recommended Solution: Use `None`

```python
def createStudent(name, age, grades=None):
    if grades is None:
        grades = []
    return {
        'name': name,
        'age': age,
        'grades': grades
    }
```

This ensures that a **new list is created for each function call** if no grades are provided.

---

## 🔄 Corrected Example

```python
chrisley = createStudent('Chrisley', 15)
dallas = createStudent('Dallas', 16)

addGrade(chrisley, 90)
addGrade(dallas, 100)
```

### ✅ Expected Output:
```
[90]
[100]
```

---

## 📌 Key Takeaways

- Avoid using **mutable default arguments** in function definitions.
- Use `None` and a conditional to initialize mutables inside the function.
- Python gotchas are subtle, so understanding mutability is crucial.
- Safe default arguments include: `None`, integers, floats, strings, and tuples.

---

## 🧪 Quick Practice Example

```python
def update_order(new_item, current_order=None):
    if current_order is None:
        current_order = []
    current_order.append(new_item)
    return current_order

# Test
order1 = update_order({'item': 'burger', 'cost': '3.50'})
order2 = update_order({'item': 'soda', 'cost': '1.50'})
print(order2)
```

### ✅ Output:
```
[{'item': 'soda', 'cost': '1.50'}]
```

---

Always be cautious with mutable default arguments—they can introduce subtle bugs that are hard to trace.

---
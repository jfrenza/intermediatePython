
---

# 🧩 Variable Keyword Arguments in Python: `**kwargs`

In addition to handling unlimited positional arguments with `*args`, Python also allows functions to accept an **unlimited number of keyword arguments** using `**kwargs`.

---

## 🔧 What Is `**kwargs`?

- `**kwargs` collects all **keyword arguments** passed to a function into a **dictionary**.
- The name `kwargs` is a convention, but any valid variable name can be used.

---

## 🧪 Example:

```python
def arbitrary_keyword_args(**kwargs):
    print(type(kwargs))
    print(kwargs)
    print(kwargs.get('anything_goes'))

arbitrary_keyword_args(this_arg='wowzers', anything_goes=101)
```

### ✅ Output:

```
<class 'dict'>
{'this_arg': 'wowzers', 'anything_goes': 101}
101
```

---

## 🧠 Key Concepts

- `**kwargs` gathers keyword arguments into a **dictionary**.
- You can use **dictionary methods** (e.g., `.get()`, `.keys()`, `.values()`) on `kwargs`.
- Just like `*args`, the name after `**` is flexible:

```python
def arbitrary_keyword_args(**data):
    print(data)
```

---

## 🔄 Summary Table

| Syntax       | Type Collected | Stored As      | Access Method        |
|--------------|----------------|----------------|----------------------|
| `*args`      | Positional      | Tuple          | Indexing (e.g., `args[0]`) |
| `**kwargs`   | Keyword         | Dictionary     | Key access (e.g., `kwargs['key']`) |

---

Use `**kwargs` when you want to allow a function to accept any number of **named arguments**, giving your functions flexibility and extensibility.

---
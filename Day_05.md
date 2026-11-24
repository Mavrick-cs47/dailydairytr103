# Day 5 – Python Data Structures

**Date:** ____/____/______  |  **Week:** 1

## 🎯 Objective
Learn to store and manipulate collections of data.

## 📚 Topics Learned
- Lists: indexing, slicing, `append`, `remove`, `sort`
- Tuples and immutability
- Dictionaries: keys, values, `.items()`, nested dictionaries
- Sets: unique values, union, intersection
- List comprehensions and dictionary comprehensions

## 🛠️ Practical Work
- Stored a list of patient records as dictionaries
- Counted diseases using a dictionary
- Removed duplicate patient IDs using a set

```python
diseases = ["Flu", "Diabetes", "Flu", "Asthma", "Flu"]
counts = {}
for d in diseases:
    counts[d] = counts.get(d, 0) + 1
print(counts)   # {'Flu': 3, 'Diabetes': 1, 'Asthma': 1}
```

## ⚠️ Challenges & Solutions
- **Challenge:** `KeyError` when accessing a missing dictionary key.
- **Solution:** Used `.get()` with a default value.

## ✅ Outcome
Can structure and process simple datasets with Python's core collections.

## 🔜 Plan for Tomorrow
File handling, CSV reading/writing, exceptions, and virtual environments.

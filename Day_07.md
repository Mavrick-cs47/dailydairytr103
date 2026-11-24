# Day 7 – OOP Basics & Week 1 Revision

**Date:** ____/____/______  |  **Week:** 1

## 🎯 Objective
Understand classes and objects, and consolidate everything from Week 1.

## 📚 Topics Learned
- Classes, objects, attributes, and methods
- The `__init__` constructor and `self`
- Basic inheritance
- Revision of variables, loops, functions, data structures, and file handling

## 🛠️ Practical Work
- Created a `Patient` class with name, age, disease, and a method to display details
- Mini-task: a console-based patient record manager (add / view / delete) saving to CSV

```python
class Patient:
    def __init__(self, pid, name, age, disease):
        self.pid, self.name = pid, name
        self.age, self.disease = age, disease

    def info(self):
        return f"{self.pid} | {self.name} | {self.age} | {self.disease}"
```

## ⚠️ Challenges & Solutions
- **Challenge:** Forgetting `self` in method definitions.
- **Solution:** Practised until it became habit; read the error message carefully.

## ✅ Outcome
Completed the Python fundamentals week with a small working console project.

## 🔜 Plan for Tomorrow
Start Week 2 with NumPy arrays.

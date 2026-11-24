# Day 3 – Control Flow: Conditionals & Loops

**Date:** ____/____/______  |  **Week:** 1

## 🎯 Objective
Learn to make decisions and repeat tasks in code.

## 📚 Topics Learned
- `if`, `elif`, `else` statements and nested conditions
- `for` loops with `range()`
- `while` loops
- `break`, `continue`, and `pass`
- Basic pattern printing

## 🛠️ Practical Work
- Classified patients into age groups (child / adult / senior) using `if-elif-else`
- Printed multiplication tables with loops
- Wrote a number-guessing game using `while`

```python
age = 67
if age < 18:
    group = "Child"
elif age < 60:
    group = "Adult"
else:
    group = "Senior"
print(group)
```

## ⚠️ Challenges & Solutions
- **Challenge:** Infinite loop in a `while` block.
- **Solution:** Updated the loop variable inside the loop and added a `break` condition.

## ✅ Outcome
Able to control program flow and automate repetitive logic.

## 🔜 Plan for Tomorrow
Functions, modules, and lambda expressions.

# Day 4 – Functions, Modules & Lambda

**Date:** ____/____/______  |  **Week:** 1

## 🎯 Objective
Write reusable code using functions and modules.

## 📚 Topics Learned
- Defining functions with `def`, parameters, and return values
- Default and keyword arguments, `*args` and `**kwargs`
- Variable scope (local vs global)
- `lambda`, `map()`, `filter()`
- Importing built-in modules (`math`, `random`, `datetime`)
- Creating and importing my own module

## 🛠️ Practical Work
- Created a `calculate_bmi()` function and a `get_age_group()` function
- Built a `helpers.py` module and imported it into another script
- Used `datetime` to compute the difference between two dates (early practice for length of stay)

```python
from datetime import date

def length_of_stay(admit, discharge):
    return (discharge - admit).days

print(length_of_stay(date(2024, 1, 5), date(2024, 1, 12)))
```

## ⚠️ Challenges & Solutions
- **Challenge:** `ModuleNotFoundError` when importing my own file.
- **Solution:** Kept both files in the same folder and checked the file name spelling.

## ✅ Outcome
Understood how to organise code into reusable functions and modules, the same idea used later in the `utils/` folder.

## 🔜 Plan for Tomorrow
Data structures: lists, tuples, dictionaries, sets.

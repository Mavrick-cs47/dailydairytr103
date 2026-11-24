# Day 8 – Introduction to NumPy

**Date:** ____/____/______  |  **Week:** 2

## 🎯 Objective
Learn fast numerical computing with NumPy arrays.

## 📚 Topics Learned
- Why NumPy is faster than Python lists
- Creating arrays: `np.array`, `zeros`, `ones`, `arange`, `linspace`
- Array attributes: `shape`, `dtype`, `ndim`, `size`
- Indexing and slicing (1D and 2D)
- Reshaping arrays

## 🛠️ Practical Work
- Converted a list of patient ages into a NumPy array
- Practised slicing rows and columns of a 2D array
- Compared execution time of a loop vs a vectorised NumPy operation

```python
import numpy as np
ages = np.array([25, 34, 45, 67, 52])
print(ages.mean(), ages.max(), ages[ages > 40])
```

## ⚠️ Challenges & Solutions
- **Challenge:** Confusion between `shape (5,)` and `(5,1)`.
- **Solution:** Used `reshape()` and printed shapes frequently.

## ✅ Outcome
Understood arrays and vectorised operations, the foundation of Pandas.

## 🔜 Plan for Tomorrow
NumPy operations, broadcasting, and random number generation.

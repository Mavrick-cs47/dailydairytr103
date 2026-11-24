# Day 12 – Selecting & Filtering Data

**Date:** ____/____/______  |  **Week:** 2

## 🎯 Objective
Extract exactly the rows and columns needed for analysis.

## 📚 Topics Learned
- Column selection (single and multiple)
- `loc` (label based) and `iloc` (position based)
- Boolean filtering with `&`, `|`, `~`
- `isin()`, `between()`, `str.contains()`
- `query()` method
- Sorting with `sort_values()`

## 🛠️ Practical Work
- Filtered patients by department, gender, and age range
- Found the top 10 most expensive treatments
- Combined multiple conditions (e.g. Cardiology patients over 50 who are still admitted)

```python
subset = df[(df["Department"] == "Cardiology") & (df["Age"].between(50, 80))]
top10 = df.sort_values("Treatment_Cost", ascending=False).head(10)
```

## ⚠️ Challenges & Solutions
- **Challenge:** `ValueError` using `and` instead of `&`.
- **Solution:** Used `&` with each condition in parentheses.

## ✅ Outcome
This is the same logic I later wrapped into `utils/filters.py` for the dashboard sidebar.

## 🔜 Plan for Tomorrow
Data cleaning: missing values, duplicates, and data types.

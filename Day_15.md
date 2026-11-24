# Day 15 – GroupBy & Aggregation

**Date:** ____/____/______  |  **Week:** 3

## 🎯 Objective
Summarise data by categories to answer business questions.

## 📚 Topics Learned
- `groupby()` with `sum`, `mean`, `count`, `nunique`
- Multiple aggregations using `.agg()`
- Named aggregation syntax
- `reset_index()` and `sort_values()` on results

## 🛠️ Practical Work
- Revenue by department
- Average length of stay by disease
- Patient count and average cost per doctor (the base of the Doctor Performance page)

```python
dept = (df.groupby("Department")
          .agg(Patients=("Patient_ID", "count"),
               Revenue=("Treatment_Cost", "sum"),
               Avg_Stay=("Length_of_Stay", "mean"))
          .reset_index())
```

## ⚠️ Challenges & Solutions
- **Challenge:** Column names became a MultiIndex after `.agg()`.
- **Solution:** Switched to named aggregation for clean column names.

## ✅ Outcome
Can answer questions like "which department earns the most?" in a few lines.

## 🔜 Plan for Tomorrow
Merging, pivot tables, and time-based analysis.

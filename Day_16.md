# Day 16 – Merge, Pivot Tables & Time-Series Analysis

**Date:** ____/____/______  |  **Week:** 3

## 🎯 Objective
Combine tables and analyse trends over time.

## 📚 Topics Learned
- `merge()`, `concat()`, and join types
- `pivot_table()` and `crosstab()`
- Datetime accessor: `.dt.month`, `.dt.year`, `.dt.to_period("M")`
- Resampling by month

## 🛠️ Practical Work
- Created a monthly admissions and revenue table
- Built a Department × Month pivot table
- Cross-tabulated Gender vs Disease

```python
df["Month"] = df["Admission_Date"].dt.to_period("M").astype(str)
monthly = df.groupby("Month").agg(Patients=("Patient_ID", "count"),
                                  Revenue=("Treatment_Cost", "sum"))
pivot = df.pivot_table(index="Department", columns="Month",
                       values="Treatment_Cost", aggfunc="sum")
```

## ⚠️ Challenges & Solutions
- **Challenge:** Months sorting alphabetically instead of chronologically.
- **Solution:** Used `YYYY-MM` period strings so they sort correctly.

## ✅ Outcome
Ready to build monthly and department reports.

## 🔜 Plan for Tomorrow
Exploratory Data Analysis and `eda.py`.

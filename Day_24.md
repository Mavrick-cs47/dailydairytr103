# Day 24 – Dynamic Filtering System

**Date:** ____/____/______  |  **Week:** 4

## 🎯 Objective
Build one reusable filter panel for all pages.

## 📚 Topics Learned
- Designing filters: department, doctor, gender, disease, age range, status, insurance, date range
- Single-pass filtering with a combined boolean mask
- Handling empty selections and edge cases
- Showing a "no data" warning gracefully

## 🛠️ Practical Work
- Wrote `utils/filters.py` with `render_sidebar_filters(df)` and `apply_filters(df, selections)`
- Added a live "records matching" counter in the sidebar

```python
mask = pd.Series(True, index=df.index)
if depts:
    mask &= df["Department"].isin(depts)
mask &= df["Age"].between(age_min, age_max)
filtered = df[mask]
```

## ⚠️ Challenges & Solutions
- **Challenge:** Repeated filtering created slow, chained DataFrames.
- **Solution:** Built one combined mask and filtered once.

## ✅ Outcome
Every page can now share the same, fast filter logic.

## 🔜 Plan for Tomorrow
KPI calculator and custom styling.

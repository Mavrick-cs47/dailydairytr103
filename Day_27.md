# Day 27 – Multipage App: Patients, Doctors & Departments

**Date:** ____/____/______  |  **Week:** 5

## 🎯 Objective
Expand the dashboard into a multipage application.

## 📚 Topics Learned
- Streamlit's `pages/` folder convention
- Reusing the loader, filters, and helpers on every page
- Designing each page around a clear question

## 🛠️ Practical Work
- `pages/Patients.py`: age, gender, and disease distribution
- `pages/Doctors.py`: workload, average cost, and a performance summary table
- `pages/Departments.py`: patient load, revenue, average stay, and staffing
- Confirmed filters apply consistently across all pages

```python
df = load_data()
filtered = apply_filters(df, render_sidebar_filters(df))
page_header("Doctor Performance", "Workload and revenue by doctor")
```

## ⚠️ Challenges & Solutions
- **Challenge:** Filters reset when switching pages.
- **Solution:** Used widget keys so selections persist through session state.

## ✅ Outcome
Four analytics pages working with shared, consistent logic.

## 🔜 Plan for Tomorrow
Patient Search and CSV export.

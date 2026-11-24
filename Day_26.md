# Day 26 – Chart Helper & Executive Overview Page

**Date:** ____/____/______  |  **Week:** 4

## 🎯 Objective
Centralise chart creation and finish the main page.

## 📚 Topics Learned
- Writing reusable chart functions that take a DataFrame and return a figure
- Keeping colours, fonts, and templates consistent via `config.py`
- Composing a page: header → filters → KPI row → charts grid

## 🛠️ Practical Work
- Wrote `utils/chart_helper.py` (bar, line, donut, histogram, box)
- Built `app.py` as the Overview page: KPIs, monthly trend, revenue by department, top diseases, status split
- Added `use_container_width=True` for responsive charts

```python
def revenue_by_department(df):
    data = df.groupby("Department", observed=True)["Treatment_Cost"].sum().reset_index()
    return px.bar(data, x="Department", y="Treatment_Cost", title="Revenue by Department")
```

## ⚠️ Challenges & Solutions
- **Challenge:** Warning from `groupby` on category columns.
- **Solution:** Passed `observed=True`.

## ✅ Outcome
A complete, interactive Executive Overview page.

## 🔜 Plan for Tomorrow
Multipage setup: Patients, Doctors, Departments.

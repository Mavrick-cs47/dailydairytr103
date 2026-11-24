# Day 22 – Streamlit Widgets, Sidebar & Layout

**Date:** ____/____/______  |  **Week:** 4

## 🎯 Objective
Add user interaction and structure the page layout.

## 📚 Topics Learned
- Input widgets: `selectbox`, `multiselect`, `slider`, `date_input`, `text_input`, `radio`
- `st.sidebar` for filters
- Layout: `st.columns`, `st.tabs`, `st.expander`
- `st.metric` for KPI numbers
- Session state basics

## 🛠️ Practical Work
- Added a department multiselect and age slider to the sidebar
- Displayed four `st.metric` KPIs in columns
- Used tabs to separate charts from raw data

```python
dept = st.sidebar.multiselect("Department", df["Department"].unique())
age = st.sidebar.slider("Age", 0, 100, (0, 100))
col1, col2 = st.columns(2)
col1.metric("Patients", len(df))
```

## ⚠️ Challenges & Solutions
- **Challenge:** Empty selection made the dashboard blank.
- **Solution:** Treated "nothing selected" as "select all".

## ✅ Outcome
The dashboard now responds to user input.

## 🔜 Plan for Tomorrow
Caching and the shared data-loading layer.

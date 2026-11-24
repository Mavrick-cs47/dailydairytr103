# Day 25 – KPI Calculations & Custom Styling

**Date:** ____/____/______  |  **Week:** 4

## 🎯 Objective
Calculate hospital KPIs and give the app a professional look.

## 📚 Topics Learned
- Defining KPIs: total patients, total revenue, average stay, bed occupancy rate
- Bed occupancy = currently admitted patients / total bed capacity
- Injecting custom CSS with `st.markdown(..., unsafe_allow_html=True)`
- Designing KPI cards with icons and hover effects

## 🛠️ Practical Work
- Wrote `utils/kpi_calculator.py` with one function per KPI
- Wrote `utils/styling.py` with the CSS theme, `kpi_card()`, and `page_header()`
- Added a sidebar logo with a fallback icon badge

```python
def bed_occupancy(df, capacity):
    admitted = (df["Status"] == "Admitted").sum()
    return round(admitted / capacity * 100, 1)
```

## ⚠️ Challenges & Solutions
- **Challenge:** Streamlit's default style overrode my CSS.
- **Solution:** Used more specific selectors and tested in the browser inspector.

## ✅ Outcome
The dashboard looks like a real hospital product, not a plain script.

## 🔜 Plan for Tomorrow
Reusable chart helpers and the Overview page.

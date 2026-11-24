# Day 19 – Plotly Express: Bar & Line Charts

**Date:** ____/____/______  |  **Week:** 3

## 🎯 Objective
Learn to create interactive charts with Plotly Express.

## 📚 Topics Learned
- Why interactive charts beat static charts
- `px.bar()` and `px.line()`
- Axis labels, titles, colour sequences, and hover data
- Sorting data before plotting
- Showing charts with `fig.show()`

## 🛠️ Practical Work
- Bar chart: revenue by department
- Line chart: monthly patient admissions
- Horizontal bar chart: top 10 diseases

```python
import plotly.express as px
fig = px.bar(dept, x="Department", y="Revenue",
             color="Department", title="Revenue by Department")
fig.show()
```

## ⚠️ Challenges & Solutions
- **Challenge:** Overlapping labels on the x-axis.
- **Solution:** Used horizontal bars and rotated tick labels.

## ✅ Outcome
Produced my first interactive charts from the hospital data.

## 🔜 Plan for Tomorrow
More chart types: pie, histogram, box, scatter, heatmap.

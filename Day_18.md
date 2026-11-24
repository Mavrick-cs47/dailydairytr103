# Day 18 – Building the Synthetic Dataset Generator

**Date:** ____/____/______  |  **Week:** 3

## 🎯 Objective
Create a realistic, large hospital dataset using code.

## 📚 Topics Learned
- Designing a data schema: Patient_ID, Name, Age, Gender, Disease, Department, Doctor, Admission/Discharge Date, Treatment_Cost, Status, Insurance
- Weighted random choices with NumPy
- Mapping diseases to departments and doctors
- Generating random date ranges
- Making cost realistic by department and stay length

## 🛠️ Practical Work
- Wrote `scripts/generate_hospital_data.py`
- Saved output to `data/raw/hospital_data.csv`
- Verified output with `head()`, `info()`, and `describe()`

```python
np.random.seed(42)
n = 10000
df = pd.DataFrame({
    "Patient_ID": np.arange(1, n + 1),
    "Age": np.random.randint(1, 90, n),
    "Gender": np.random.choice(["Male", "Female"], n),
})
```

## ⚠️ Challenges & Solutions
- **Challenge:** Doctors appearing in the wrong departments.
- **Solution:** Created a department → doctors dictionary and sampled from it.

## ✅ Outcome
A reproducible raw dataset, plus the full pipeline: generate → clean → analyse.

## 🔜 Plan for Tomorrow
Start visualisation with Plotly Express.

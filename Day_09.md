# Day 9 – NumPy Operations, Broadcasting & Random Data

**Date:** ____/____/______  |  **Week:** 2

## 🎯 Objective
Perform mathematical operations and generate random data with NumPy.

## 📚 Topics Learned
- Element-wise arithmetic and aggregate functions (`sum`, `mean`, `median`, `std`)
- Boolean masking and `np.where`
- Broadcasting rules
- Random module: `np.random.seed`, `randint`, `choice`, `normal`
- `np.unique`, `np.sort`, `np.argsort`

## 🛠️ Practical Work
- Generated random patient ages and treatment costs
- Used `np.random.choice` with probabilities to simulate genders and diseases (idea later used in `generate_hospital_data.py`)
- Used `np.where` to label patients as "Senior" or "Non-senior"

```python
np.random.seed(42)
ages = np.random.randint(1, 90, size=1000)
costs = np.random.normal(15000, 5000, size=1000).round(2)
labels = np.where(ages >= 60, "Senior", "Non-senior")
```

## ⚠️ Challenges & Solutions
- **Challenge:** Different results each run.
- **Solution:** Set `np.random.seed()` for reproducibility.

## ✅ Outcome
Learned to simulate realistic data, which became the basis of my synthetic hospital dataset.

## 🔜 Plan for Tomorrow
Pandas: Series and DataFrames.

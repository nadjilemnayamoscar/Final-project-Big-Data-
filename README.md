# Final-project-Big-Data-



# 🦟 Malaria Trends in Rwanda – Big Data Analytics Capstone

Capstone project for **INSY 8413 – Introduction to Big Data Analytics**  
👤 **Nadjilem Nayam Oscar**  
📅 Academic Year: 2024–2025, Semester III  
🎓 Adventist University of Central Africa (AUCA)  
👨‍🏫 Instructor: Eric Maniraguha

---

## 📌 Project Overview

This project analyzes malaria incidence and mortality in Rwanda using real-world health data from the **World Health Organization (WHO)**. It covers the full data workflow: cleaning, exploration, visualization, and dashboard creation.

---

## 🧠 Problem Statement

> How have malaria incidence and mortality rates evolved in Rwanda, and how can data analytics help support better intervention strategies?

---

## 📂 Dataset Information

- **Source:** [WHO Global Health Observatory](https://www.who.int/data/gho/data/themes/malaria)
- **File:** `malaria_indicators_rwa.csv`
- **Format:** CSV (Structured)
- **Rows:** 130
- **Fields:**
  - `Indicator`: Type of malaria metric (e.g., incidence, mortality)
  - `Year`: Year of observation
  - `Country`: Rwanda
  - `NumericValue`: Actual data value
  - `LowBound`: Lower confidence interval
  - `HighBound`: Upper confidence interval

---

## 🔧 Step 1: Data Cleaning (Python)

Performed in **Google Colab** using `pandas`.

Tasks:
- Removed metadata rows
```python
    # Remove the first row (metadata)
    df = df.iloc[1:].copy()
```
- Renamed columns for clarity
```python

    df = df.rename(columns={
    'GHO (DISPLAY)': 'Indicator',
    'YEAR (DISPLAY)': 'Year',
    'COUNTRY (DISPLAY)': 'Country',
    'Numeric': 'NumericValue',
    'Low': 'LowBound',
    'High': 'HighBound'
})

```

- Converted numeric fields (`Year`, `NumericValue`, `LowBound`, `HighBound`)
  ```pthon
  # Convert columns to proper numeric types
df['Year'] = pd.to_numeric(df['Year'], errors='coerce')
df['NumericValue'] = pd.to_numeric(df['NumericValue'], errors='coerce')
df['LowBound'] = pd.to_numeric(df['LowBound'], error='cos='coerce')
df['HighBound'] = pd.to_numeric(df['HighBound'], errorserce')
  ```
- Dropped or handled missing values
- Filtered specific indicators (incidence & mortality)

---

## 📊 Step 2: Exploratory Data Analysis (Python)

Used `matplotlib` and `seaborn` to analyze trends:
- Line chart of malaria incidence over time
- Line chart of mortality rate over time
- Observed a decline in mortality, variable incidence

---

## 📈 Step 3: Power BI Dashboard

Built an interactive dashboard in **Power BI Desktop** using `cleaned_malaria_data.csv`.

### 💡 Dashboard Features:
- **Line Chart:** Incidence and mortality over years
- **Bar Chart:** Indicator comparison by year
- **Slicers:** Filter by year and indicator
- **KPI Cards:** Summary statistics
- **Tooltips:** Show `LowBound` and `HighBound`

---

## ✨ Step 4: Innovation

- Custom tooltips with confidence intervals
- Dynamic filters for interactivity
- Clean design with clear titles, legends, and layout

---

## 🧠 Key Insights

- Malaria incidence varies over years with spikes and dips
- Mortality rate has generally declined
- Confidence intervals show uncertainty in data collection
- Rwanda shows improvement but still needs targeted interventions

---

## 📁 Repository Structure

```

malaria-trends-rwanda/
├── data/
│   └── cleaned\_malaria\_data.csv
├── notebooks/
│   └── malaria\_analysis.ipynb
├── dashboard/
│   └── malaria\_dashboard.pbix
├── docs/
│   └── README.md
└── presentation/
└── malaria\_presentation.pptx

```

---

## ▶️ How to Run

1. Open `malaria_analysis.ipynb` in Google Colab
2. Explore and clean the data
3. Open `malaria_dashboard.pbix` in Power BI Desktop
4. Filter using slicers and explore visuals

---

## 📬 Contact

**Name:** Nadjilem Nayam Oscar  
**Email:** nadjilem.n.oscar@example.com  
**Instructor:** eric.maniraguha@auca.ac.rw

---

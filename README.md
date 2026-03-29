# 📊 Insurance Risk and Claims Analysis

A Power BI dashboard project analyzing car insurance data to understand 
who makes claims, how much they cost, and what risk factors drive higher claims.

---

## 🎯 Objective

- Analyze car insurance claims across **37,542 policyholders**
- Identify high-risk customer segments by age, education, car make, and location
- Build an interactive Power BI dashboard with dynamic DAX measures
- Help insurance companies make smarter decisions on pricing and risk management

---

## 📊 Dataset

- **File:** `insurance-policies-dataset.xlsx`
- **Features:** Age, Gender, Car Make, Car Use, Claim Amount, 
Location Zone, Education, Marital Status, Kids Driving, Car Year
- **Target:** Claim Amount & Claim Frequency

---

## 🛠️ Tool Used

| Category | Tool |
|---|---|
| Dashboard | Microsoft Power BI |
| Data Format | Excel (.xlsx) |
| Formulas | DAX (Data Analysis Expressions) |
| Presentation | PowerPoint |

---

## 📈 Key Metrics

| Metric | Value |
|---|---|
| Total Policies | 37,542 |
| Total Claim Amount | $187.8M |
| Avg Claim Frequency | 0.51 |
| Avg Claim Amount | $5,000 |
| Male Policyholders | 18,700 |
| Female Policyholders | 18,800 |

---

## 🔍 Key Findings

- **Ford ($16.6M) and Chevrolet ($14.8M)** have the highest claims among all car brands
- **80% of all claims** come from private cars — only 20% from commercial vehicles
- **Age group 26–65** makes the most claims — middle-aged drivers are the highest risk group
- **Single people with High School education** have the highest claims at **$40.2M** — nearly 4x more than married ones ($5.2M)
- **Location does not affect risk** — all 5 coverage zones contribute equally (~20% each)
- **Cars made between 2000–2017** show the highest claim amounts
- Customers with **no kids driving** have the most claims ($134M)

---

## ⚡ DAX Measures Used

| Measure | Formula | Purpose |
|---|---|---|
| Age | `DATEDIFF(BirthDate, TODAY(), YEAR)` | Calculates policyholder age |
| Age Group | `SWITCH(TRUE(), Age>=15 && Age<=25, '15-25', ...)` | Groups into 6 age buckets |
| Total Policies | `COUNT(ID)` | Counts total policies |
| Total Claim Amount | `SUM(Claim Amount)` | Adds all claim amounts |
| Avg Claim Amount | `AVERAGE(Claim Amount)` | Average per policy |
| Male Count | `CALCULATE(COUNT([ID]), Gender='Male')` | Male policyholder count |
| Female Count | `CALCULATE(COUNT([ID]), Gender='Female')` | Female policyholder count |

> ⚡ A `[select measure]` toggle switch lets you switch between Total Claim Amount and Total Policies across all visuals.

---

## 📁 Project Structure
```
insurance-risk-claims-analysis/
├── insurance-risk-claims-analysis.pbix     # Power BI dashboard file
├── insurance-policies-dataset.xlsx         # Dataset
├── insurance-risk-claims-analysis.pptx     # Project presentation
└── README.md                               # Project documentation
```

---

## 🌍 Real World Impact

- Helps insurance companies identify **high-risk customer segments**
- Enables **smarter pricing and coverage decisions**
- Provides a clear visual picture of **where claims are coming from**

---

## 👤 Author

**Dhanushree N**
Power BI Dashboard Project | Insurance Analytics | 2026
```

# 🏠 **CIVIL 763 – Smart Infrastructure Analysis**

### **Project Title:** *Practical Insights from New Zealand Residential Property Data*  
*Exploring affordability and housing characteristics under a fixed NZD 780 000 budget*

**Course:** CIVIL 763 Smart Infrastructure Analysis  
**Project Type:** Individual Data Analytics Project  
**Student:** Yuetian Doris Zhao  
**UPI:** yzbhb887  
**Date:** October 2025

---

## 📊 Dataset and Data Sources

This project integrates multiple national datasets to explore affordability, housing characteristics, and long-term price growth across New Zealand.

| Source | Description | Access |
|--------|-------------|--------|
| **Property IQ New Zealand, CoreLogic NZ, & Quotable Value NZ (2010)** | *Residential Property Sales Statistics* — Base dataset describing all property transactions between 1990–2024. Includes sale prices, floor area, land area, building age, and house type. | https://auckland.primo.exlibrisgroup.com (UoA Library access) |
| **Reserve Bank of New Zealand (RBNZ, 2025)** | *New Residential Mortgage Standard Interest Rates (B20)* — National 1-year mortgage rate time series used to estimate elasticity. | https://www.rbnz.govt.nz/statistics/series/exchange-and-interest-rates/new-residential-mortgage-standard-interest-rates |
| **Stats NZ Data Service (2025a)** | *Regional Council 2025 – clipped [Shapefile]* — New Zealand’s 16 Regional Council boundaries. | https://datafinder.stats.govt.nz/data/ |
| **Stats NZ Data Service (2025b)** | *Territorial Authority 2025 – clipped [Shapefile]* — 67 city and district councils. | https://datafinder.stats.govt.nz/data/ |

All external shapefiles are licensed under **CC BY 4.0**.

The cleaned dataset is named:

**`Combined_Residential_Property_Sale_Stats.csv`** (~3.5 million rows, 1990–2024)

---

## 🗂️ Folder Structure

| File / Folder | Description |
|----------------|-------------|
| **1. README.md** | Project overview, data sources, dependencies, reproducibility. |
| **2. Code_Doris Zhao.ipynb** | Main notebook with analysis (Patterns 1–3). |
| **3. Presentation_Slide_Buy_Smart_Doris Zhao.pdf** | Final 7-min presentation slides. |
| **CSTDAT8700_Output1_20250717.csv** | Primary raw dataset (~3.5M rows × 56 columns). |
| **CSTDAT8700_Output2_20250717.csv** | Supplementary dataset (~1.7M rows × 6 columns). |
| **hb3.xlsx** | RBNZ mortgage dataset. |
| **regional-council-2025-clipped.\*** | Stats NZ regional council shapefiles. |
| **territorial-authority-2025-clipped.\*** | Stats NZ territorial authority shapefiles. |
> *Note: Original datasets are not included in this repository due to size limits; download links are provided instead.*


### 📁 Automatically Generated During Notebook Execution

| Generated File | Purpose |
|----------------|----------|
| **Combined_Residential_Property_Sale_Stats.csv** | Cleaned & merged dataset (auto generated). |
| **Combined_Residential_Property_Sale_Stats_Summary.txt** | Log file summarising join output, missing values, dropped columns. |

> *Note: These appear automatically when you click **"Run All"** in the Jupyter Notebook.  


---

## ⚙️ Required Python Environment

Compatible with Python **3.10+**.

```txt
# Dependencies
pandas==2.2.2
numpy==1.26.4
matplotlib==3.9.0
seaborn==0.13.2
scikit-learn==1.5.1
plotly==5.24.0
geopandas==0.14.3
folium==0.17.0
```


---

## 📈 Analytical Overview by Pattern

### 🟦 Pattern 1 — Mortgage Rates and House Prices (1990–2024)

**Objective:**  
Assess how NZ’s 1-year mortgage rate affects national house prices.

**Method:**  
Log–log regression (elasticity estimation).

**Findings:**

- Elasticity ≈ **–1.41%**  
- A 1% increase in mortgage rate → ~1.4% decrease in price  
- Rates affect **affordability** more than **valuation**

---

### 🟧 Pattern 2 — Typical Home Characteristics by City (2018–2024)

**Objective:**  
Determine what NZD 780 000 can afford in Auckland, Wellington, and Dunedin.

**Method:**  
±2% price band filtering + **KNN** matching (k = 10–50)

**Findings:**

- **Auckland:** ~92 m² floor, ~104 m² land  
- **Wellington:** ~123 m² floor, ~551 m² land  
- **Dunedin:** ~180 m² floor, ~629 m² land  
- Strong differences in lifestyle and affordability across cities

---

### 🟩 Pattern 3 — Price Projection & Volatility (1995–2024 → 2035)

**Objective:**  
Forecast typical home price growth and volatility.

**Method:**  
CAGR + log-linear modelling + log-return volatility (σ)

**Findings:**

- **Auckland:** CAGR 4.36%  
- **Wellington:** CAGR 5.48%  
- **Dunedin:** CAGR 5.52% (highest)  
- Regional centres outperform Auckland long term

---

## 🧠 Advanced Analytics Components

| Technique | Purpose | Used In |
|----------|----------|---------|
| Log–log regression | Elasticity estimation | Pattern 1 |
| KNN | Comparable home identification | Pattern 2 |
| CAGR | Long-term appreciation | Pattern 3 |
| HGBR | Non-linear model enhancement | Pattern 3 |
| Log-return volatility | Uncertainty bands | Pattern 3 |

---

## 💡 Limitations and Future Potential

### Limitations
- Auckland early-year data incomplete  
- Only 3 cities analysed  
- Median focus hides neighbourhood-level variability  

### Future Extensions
- Extend to suburbs, wards, school zones  
- Explore alternative budgets (600k, 1M)  
- Include more features (condition, school ratings)  
- Use ML models (Random Forest, XGBoost) for forecasting  

---

## 🔗 References

Property IQ New Zealand, CoreLogic NZ, & QV NZ. (2010). *Residential Property Sales Statistics.*

Reserve Bank of New Zealand (RBNZ). (2025). *New residential mortgage standard interest rates (B20).*

Stats NZ. (2025a). *Regional Council 2025 – clipped*.

Stats NZ. (2025b). *Territorial Authority 2025 – clipped*.

---

© 2025 Yuetian Doris Zhao | University of Auckland  
*This project demonstrates data-driven insights into New Zealand’s housing market.*


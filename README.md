# 🏠 CIVIL 763 – Smart Infrastructure Analytics  
## New Zealand Property Data Analysis (Final Project)

This repository contains my final project for **CIVIL 763 – Smart Infrastructure Analytics**.  
Using nationwide housing data, I analysed affordability, home characteristics, and long-term price growth to help young professionals understand what they can realistically afford across New Zealand.  
This project demonstrates how data analytics and smart-infrastructure thinking can be used to inform real financial and housing decisions.

---

## 📘 Project Overview  
This project applies large-scale property transaction data (1990–2024) to explore housing affordability and long-term regional differences across New Zealand.  
The analysis focuses on homes within a target budget of **NZD 780,000**, reflecting the typical situation of young professionals entering the housing market.

The investigation consists of three core analytical components:

### **1. Affordability Under a Fixed Budget**  
Identifies what buyers can afford in Auckland, Wellington, and Dunedin based on recent property sales.

### **2. Housing Characteristics (KNN Similarity Analysis)**  
Examines the typical floor area, land size, dwelling type, and age of homes priced near the budget.  
A K-Nearest Neighbours model is used to find comparable properties within each city.

### **3. Long-Term Price Growth & Volatility**  
Computes CAGR (1995–2024) and log-return volatility to project typical home prices to 2035.  
These insights help illustrate long-run differences between regions and expected market variability.

---

## 📁 Files Included in This Repository  
| File | Description |
|------|-------------|
| **CodeDoris_20251018_041627.html** | Full analysis notebook exported to HTML, covering Patterns 1–3. |
| **hb3.xlsx** | RBNZ mortgage dataset used in interest-rate analysis. |

⚠️ **Note:**  
Large raw datasets (1.8GB and 127MB) are **not included** due to GitHub file-size limits.  
They can be accessed via the **University of Auckland Library** and **Stats NZ Data Service**.

---

## 🛠 Tools & Libraries  
- Python (Pandas, NumPy, Scikit-learn)  
- GeoPandas, Shapely  
- Matplotlib, Plotly  
- Jupyter Notebook  

---

## 📊 Key Analytical Techniques  
- Log–log regression for mortgage-rate elasticity  
- K-Nearest Neighbours for housing similarity  
- CAGR + volatility modelling for long-term projections  
- Geospatial boundary integration for regional comparison  

---

## 📩 Author  
**Yuetian Doris Zhao**  
University of Auckland – CIVIL 763 Final Project (2025)



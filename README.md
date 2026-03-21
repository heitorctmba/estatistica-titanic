# Titanic — Statistical Analysis of Survival

Project for the **Descriptive Statistics** course of the MBA in Data Science.

## Objective

Analyze the profile of Titanic passengers and identify survival patterns associated with class, sex, and age group, focusing on fare distribution and demographic inequalities. Original fares in £1912 are adjusted to £2024 through chained inflation correction.

## Data

| File | Source | Description |
|---|---|---|
| `titanic.csv` | Professor | Main dataset: passengers, fares, and survival outcome |
| `99_extras/titanic/a-millennium-of-macroeconomic-data-for-the-uk.xlsx` | Bank of England | UK composite price index 1209–2016. Used to adjust fares from 1912 to 2016 |

External sources:
- [Bank of England — A Millennium of Macroeconomic Data for the UK (v3.1)](https://www.bankofengland.co.uk/statistics/research-datasets): tab *A47. Wages and prices*, column H (index normalized to 100 in 2016)
- [World Bank — Consumer Price Index, GBR (FP.CPI.TOTL)](https://api.worldbank.org/v2/country/GBR/indicator/FP.CPI.TOTL): public API, no authentication. Extends the correction from 2016 to 2024

## Notebook Structure

1. **Imports**
2. **Loading and Preparation** — dataset loading, age group variable creation, and inflation adjustment of fares (BoE + World Bank)
3. **Exploratory Analysis** — adjusted fare distribution, analysis by class and qualitative variables (sex, class, age group)
4. **Summary and Conclusions** — descriptive tables with fares in £1912 and £2024

## Key Findings

- **Overall survival rate: 38.6%** — more than 6 out of 10 passengers did not survive
- 1st class passengers had a survival rate of **64.5%**, compared to **24.4%** in 3rd class
- Women survived at a rate of **74.2%**, compared to **19.4%** for men
- Survivors paid an average fare **2.1x higher** than non-survivors
- 1st class generated most of the revenue with less than 25% of passengers and had the highest survival rate; 3rd class had the lowest revenue, more than half of the passengers, and the worst survival rate
- The median 3rd class fare is equivalent to approximately **£900 in 2024**; the median 1st class fare exceeds **£6,900** and the average surpasses **£9,600**

## Requirements

```
pandas
matplotlib
scipy
numpy
requests
openpyxl
```

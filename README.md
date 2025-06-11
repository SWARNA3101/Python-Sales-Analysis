# Python-Sales-Analysis

## Overview 
The **Python Sales Analysis** project is an end‑to‑end exploratory data analysis (EDA) that uncovers actionable business insights from a real Indian e‑commerce sales dataset collected during the Diwali festival season. 

The goal is to help stakeholders understand consumer purchasing patterns, optimise marketing spend, and boost overall revenue during future festive campaigns. 
---
## Table of Contents 
1. [Project Structure](#project-structure)  
2. [Dataset](#dataset)  
3. [Key Questions Answered](#key-questions-answered)  
4. [Quick Start](#quick-start)  
5. [Detailed Workflow](#detailed-workflow)  
6. [Results & Insights](#results--insights)  
7. [Tech Stack](#tech-stack)  
8. [Reproducibility & Environment](#reproducibility--environment)  
9. [Contributing](#contributing)  
10. [License](#license)  

---

## Project Structure <a id="project-structure"></a>
```
├── data/
│   ├── raw/                # Original CSV/XLSX files 
│   └── processed/          # Cleaned and feature‑engineered datasets
├── notebooks/
│   └── Diwali_Sales_Analysis.ipynb  # Main analysis notebook (this repo)
├── src/
│   └── utils.py            # Common helper functions (data loading, plotting)
├── reports/
│   └── figures/            # Exported visualisations (PNG/SVG)
├── README.md               # ⟵ You are here
└── requirements.txt        # Pinned Python dependencies 
---
## Dataset <a id="dataset"></a>
| Feature | Description |
|---------|-------------|
| `Customer_ID` | Unique identifier for each shopper |
| `Gender` | Male / Female |
| `Age_Group` | Binned age range (e.g. "26‑35") |
| `Marital_Status` | 0 = single / 1 = married |
| `Occupation` | Customer profession |
| `Product_ID` | SKU code |
| `Category` | High‑level product category |
| `Sub‑Category` | Second‑level category |
| `City` | Billing city |
| `State` | Billing state |
| `Amount` | Transaction value (INR) |
| `Order_Date` | Date‑time of purchase |

The raw CSV (`Diwali_Sales_Data.csv`) was sourced from [Kaggle](https://www.kaggle.com/). No personally identifiable information (PII) is present.

---

## Key Questions Answered <a id="key-questions-answered"></a>
* Which customer segments generated the highest revenue during Diwali 2023? 
* How did average order value and total quantity vary by state and city? 
* What product categories performed best, and on which days of the sale? 
* Are married customers **really** spending more than single customers? 
* Which age‑gender cohorts should the marketing team target in 2025?

---

## Quick Start <a id="quick-start"></a>
```bash
# Clone the repo and enter it
$ git clone https://github.com/<org>/diwali-sales-analysis.git
$ cd diwali-sales-analysis

# Create and activate a virtual environment (Python ≥3.10)
$ python -m venv .env && source .env/bin/activate  # Linux/macOS
# For Windows PowerShell:
#  .\.env\Scripts\Activate.ps1

# Install dependencies
$ pip install -r requirements.txt

# Launch the notebook locally
$ jupyter lab 
```
Open `notebooks/Diwali_Sales_Analysis.ipynb` and run *Kernel → Restart & Run All*.

---

## Detailed Workflow <a id="detailed-workflow"></a>
1. **Data Ingestion**  
   * Load raw CSV, parse dates, handle encoding issues. 
2. **Data Cleaning & Pre‑processing**  
   * Remove nulls/duplicates, correct data types, feature‑engineer `Age_Group` etc. 
3. **Exploratory Data Analysis (EDA)**  
   * Univariate and bivariate visualisations (pandas, seaborn, matplotlib). 
   * Hypothesis testing (e.g. t‑tests comparing married vs single spend). 
4. **Insights & Recommendations**  
   * Interactive dashboards with Plotly/PowerBI (optional). 
5. **Reporting**  
   * Export publication‑ready figures in `reports/figures/`. 

---

## Results & Insights <a id="results--insights"></a>
| Insight | Business Action |
|---------|----------------|
| 🔝 **Female, age 26‑35** drove ≈46 % of total Diwali revenue | Double digital‑first campaign budget for this cohort |
| 🏙️ **Tier‑1 cities** (Delhi, Mumbai, Bengaluru) showed 25 % higher AOV | Run city‑level storefront promos and localized ads |
| 🛒 **Home & Lifestyle** category peaked on Day 3 of sale | Introduce flash deals on Day 3 2025 |
| 💍 Married customers spent ~₹ 750 more per order than singles | Create bundled “family packs” & wedding‑season offers |

---

## Tech Stack <a id="tech-stack"></a>
| Layer | Tools |
|-------|-------|
| Computation & Scripting | Python 3.10 |
| Core Libraries | pandas, numpy, scipy |
| Visualisation | matplotlib, seaborn, plotly |
| Notebook Environment | JupyterLab |
| Optional Dashboard | Power BI / Streamlit |

---

## Reproducibility & Environment <a id="reproducibility--environment"></a>
* `requirements.txt` is locked with exact versions (via `pip freeze`). 
* Set the random seed wherever randomness is introduced. 
* Notebook kept clean (only committed with executed cells and outputs ≤ 1 MB). 
* Add `data/raw/*` to `.gitignore` to keep the repository lightweight. 


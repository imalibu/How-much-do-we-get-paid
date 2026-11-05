# Story 4: How Much Do We Get Paid?
### Evaluating Nominal Salary vs. Real Purchasing Power for Data Practitioners

An empirical analysis and visual storytelling project assessing compensation across core data roles in the United States, adjusted for statutory state individual income taxes and localized cost of living via Bureau of Economic Analysis (BEA) Regional Price Parities (RPP).

---

## 📌 Project Overview

The term **"Data Practitioner"** covers a diverse spectrum of specialized technical roles. While headline compensation numbers in coastal technology hubs appear substantially higher, nominal gross wages fail to reflect actual take-home purchasing power. 

This project normalizes compensation across 10 major state labor markets by applying:
1. **State Income Tax Liabilities:** Effective state-level tax brackets.
2. **Cost of Living Indexing:** Regional Price Parities (RPP) benchmarked to the national baseline ($US = 100.0$).

### Core Roles Analyzed
* **Data Analyst**
* **Business Analyst**
* **Data Scientist**
* **Data Engineer**
* **Data Architect**

---

## 📊 Data Sources & Methodology

| Domain | Primary Source | Benchmark Metric / Classification |
| :--- | :--- | :--- |
| **Salary Data** | U.S. Bureau of Labor Statistics (BLS) OEWS | Standard SOC codes: `15-2051` (Data Scientists), `15-1251` (Engineers), `13-1111` (Analysts) |
| **Cost of Living (COL)** | U.S. Bureau of Economic Analysis (BEA) | Regional Price Parities (RPP) by State (Baseline = 100.0) |
| **State Taxation** | Tax Foundation | Effective State Individual Income Tax Rates ($100k–$200k bracket) |

### Normalization Formula
$$\text{Net Salary} = \text{Gross Salary} - (\text{Gross Salary} \times \text{State Tax Rate})$$

$$\text{Real Adjusted Salary} = \left( \frac{\text{Net Salary}}{\text{RPP Index}} \right) \times 100$$

---

## 📈 Key Visualizations Included

1. **Nominal Gross vs. Real Purchasing Power:** Horizontal comparative bar chart highlighting salary erosion across major tech states.
2. **Real Adjusted Salary Heatmap:** Role-by-state matrix ranking real retained earnings across all five practitioner classifications.
3. **Compensation Decomposition Waterfall:** Stacked breakdown isolating state tax deductions vs. price parity purchasing drag.
4. **Role Dispersion & Variance:** Box-and-whisker + strip plot detailing the spread of purchasing power within each specialization.
5. **Macro Friction Quadrant:** Scatter plot mapping state income tax rates directly against regional price parities with real compensation bubble sizing.

---

## 💡 Key Analytical Findings

* **The Coastal Nominal Mirage:** California and New York offer the highest nominal gross compensation (~$151,000 and ~$147,000 for Data Scientists), but rank among the lowest in retained purchasing power (~$121,700 and ~$124,300) due to top-tier state tax brackets and RPP indices exceeding 110.
* **No-Income-Tax State Advantage:** Washington and Texas deliver higher real purchasing power than coastal markets. Washington’s 0% individual income tax offsets its higher living cost index (107.8), maintaining a real adjusted salary of ~$133,000 for Data Scientists.
* **Role Inelasticity:** Infrastructure and architecture positions (Data Engineer, Data Architect) command base salaries high enough to overcome regional price drag, whereas general analyst tiers face severe margin compression in high-tax/high-COL jurisdictions.

---

## 🚀 Repository Contents

* `index.html`: Complete standalone interactive dashboard with all 5 high-resolution visualizations embedded directly into the report.
* `README.md`: Project documentation and executive findings.

---

## 🌐 Viewing Online (GitHub Pages)

1. Open your repository on **GitHub.com** in your browser.
2. Click **Settings** (gear icon on the top menu).
3. Click **Pages** in the left sidebar menu.
4. Under **Branch**, select `main` and leave the folder set to `/(root)`, then click **Save**.
5. GitHub will provide a link to your live report at `https://<your-username>.github.io/<repo-name>/`.

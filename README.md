# Toronto Raptors: Statistical Analysis of Championship Decline (2018–2025)
### Power BI Dashboard + Python Analysis

**Tools:** Python (pandas, matplotlib, seaborn, scikit-learn) · Power BI · Google Colab · Excel (pivotables)
**Dataset:** 7 seasons of Raptors team and player stats (2018–2025) via Basketball-Reference.com

This project analyzes the Toronto Raptors' trajectory from their 2019 NBA Championship through the current rebuild era — using Power BI for interactive visualization and Python for regression and correlation analysis to identify what drove the team's rise and decline.

---

## 📊 Project Components

### Power BI Dashboard
**Page 1: Team Performance**
- Win percentage trend (2018–2025)
- Offensive vs. Defensive efficiency over time
- Championship season benchmarks (58 wins, 54.3% eFG%, 25.4 AST)

**Page 2: Player Analysis**
- Leading scorers by season showing roster evolution
- Usage rate vs. efficiency scatter plot highlighting Kawhi's 2019 performance
- Scoring leadership transition (Kawhi → Siakam → Barrett)

### Python Analysis Notebook
**Regression Analysis** — two models tested against win percentage:
- Model 1 (Composite Ratings — OFFrtg + DEFrtg): R² = 0.933
- Model 2 (Four Factors — eFG%, TOV%, ORB%, FT%): R² = 0.326

**Correlation Analysis** — key metrics vs. win%:
- DefRtg: -0.941 (dominant predictor)
- FT Rate: +0.568 (moderate)
- OFFrtg: +0.111 (weak)

---

## ✅ Key Insights
- **Defense explains the decline** — DefRtg correlation with win% of -0.941 means defensive performance almost perfectly predicted winning across all 7 seasons
- **The championship formula** — Elite defense (107.1 DefRtg) combined with Kawhi's efficient high-usage play (30.3 USG%, 54.6 eFG%) drove the 2019 title
- **Offense was not the problem** — OFFrtg showed weak correlation with winning; the rebuild gap is a defensive one
- **DefRtg deteriorated from 107.1 (2018–19) to 118.8 (2023–24)** — directly corresponding to the 33-win drop over the same period

---

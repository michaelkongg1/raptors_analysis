# Toronto Raptors: Statistical Analysis of Championship Decline (2018–2026)
### Power BI Dashboard + Python Analysis

**Tools:** Python (pandas, matplotlib, scikit-learn, statsmodels) · Power BI · Google Colab · Excel  
**Dataset:** 8 seasons of Raptors team and player stats (2018–2026) via Basketball-Reference.com

This project analyzes the Toronto Raptors' trajectory from their 2019 NBA Championship through the current rebuild era — using Power BI for interactive visualization and Python for regression and correlation analysis to identify what drove the team's rise and decline.

---

**Note:** This project was revised to include a proper star-schema data model 
and DAX measures, replacing an earlier version built on a single flat table.

--- 

## 📊 Project Components

### Power BI Dashboard

**Page 1: Team Performance**
- Win percentage trend (2018–2026)
- Offensive vs. Defensive efficiency over time
- Championship season benchmarks (58 wins, 54.3% eFG%, 25.4 AST)

**Page 2: Player Analysis**
- Leading scorers by season showing roster evolution
- Usage rate vs. efficiency scatter plot highlighting Kawhi's 2019 performance
- Scoring leadership transition (Kawhi → Siakam → Barrett)

### Python Analysis Notebook

**Regression Analysis** — three models tested against win percentage:
- Model 1 (Composite Ratings — OFFrtg + DEFrtg): R² = 0.933
- Model 2 (Offensive Four Factors — eFG%, TOV%, ORB%, FT rate): R² = 0.439
- Model 3 (Defensive Four Factors — opp eFG%, TOV%, DRB%, opp FT rate): R² = 0.901

**Multicollinearity Diagnostics (VIF):**
- All VIF values below 5, confirming the four factors are not redundant
- Rules out multicollinearity as the cause of Model 2's poor performance
- Offensive factors genuinely have weaker individual correlations with winning than defensive factors

**Correlation Analysis** — key metrics vs. win%:
- DefRtg: -0.922 (dominant predictor)
- def_eFG%: -0.826 (strong)
- def_RB%: +0.620 (moderate)
- off_FT rate: +0.579 (moderate)
- OFFrtg: +0.151 (very weak)

---

## ✅ Key Insights

- **Defense explains the decline** — DefRtg correlation with win% of -0.922 means defensive performance almost perfectly predicted winning across the 8 seasons
- **Defensive Four Factors (R² = 0.901) explain wins twice as well as Offensive Four Factors (R² = 0.439)** — defense is the systematic driver of winning; offense is too noisy at the granular level
- **The championship formula** — Elite defense (107.1 DefRtg) combined with Kawhi's efficient high-usage play (30.3 USG%, 54.6 eFG%) drove the 2019 title run
- **Five of the top six predictors are defensive metrics** — even composite OffRtg has only r = 0.151 with winning

---

## 🚧 Limitations

- Small sample size (n=8) limits statistical power and confidence intervals
- Analysis prioritizes narrative coherence over predictive power
- Single-team case study — findings may not generalize to other teams or eras

---

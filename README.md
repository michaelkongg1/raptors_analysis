# Toronto Raptors Performance Analysis (2018-2025)

Analysis of the Toronto Raptors' performance trajectory from their 2019 NBA Championship through their current rebuild phase. This project uses Power BI for interactive visualization and Python for statistical analysis to identify the key factors behind the team's decline.

**Key Finding:** Defense explains everything. Defensive Rating shows a -0.941 correlation with winning percentage — the team's championship success and subsequent decline can be attributed almost entirely to defensive performance, not offense.

---

## Tools & Technologies

- **Power BI Desktop** - Interactive dashboard
- **Python** - Statistical analysis (pandas, matplotlib, seaborn, scikit-learn)
- **Data Source** - Basketball-Reference.com

---

## Project Components

### Power BI Dashboard

**Page 1: Team Performance**
- Win percentage trend (2018-2025)
- Offensive vs Defensive efficiency over time
- Championship season benchmarks (58 wins, 54.3% eFG%, 25.4 AST)

**Page 2: Player Analysis**
- Leading scorers by season showing roster evolution
- Usage rate vs efficiency scatter plot highlighting Kawhi's elite 2019 performance
- Scoring leadership transition (Kawhi → Siakam → Barrett)

### Python Analysis Notebook

**Regression Analysis:**
- Model 1 (Composite Ratings): R² = 0.933
  - DefRtg coefficient: -0.0355 (defense matters more)
  - OFFrtg coefficient: +0.0232
- Model 2 (Four Factors): R² = 0.326 (limited by small sample size)

**Correlation Analysis:**
- DefRtg: -0.941 (extremely strong predictor)
- FT Rate: +0.568 (moderate, surprisingly second strongest)
- OFFrtg: +0.111 (weak — offense barely matters for this team)

---

## Key Insights

1. **Defense dominated outcomes** - The -0.941 correlation between DefRtg and Win% shows defensive performance almost perfectly predicted winning

2. **The championship formula** - Elite defense (107.1 DefRtg) + Kawhi's efficient high-usage play (30.3 USG%, 54.6 eFG%)

3. **The decline** - DefRtg deteriorated from 107.1 (2018-19) to 118.8 (2023-24), explaining the 33-win drop

4. **Free throws > shooting efficiency** - FT Rate showed stronger correlation than eFG%

---

## Data

- **Timeframe:** 7 seasons (2018-19 through 2024-25)
- **Team metrics:** Win%, OffRtg, DefRtg, NetRtg, eFG%, TOV%, ORB%, FT Rate
- **Player data:** 90 player-seasons (filtered to 18+ MPG)

---

## Limitations

- Small sample size (n=7) limits statistical confidence
- Analysis prioritizes narrative coherence over predictive power
- Single-team case study — findings may not generalize to other teams

---

## Files

- `raptors_dashboard.pbix` - Power BI dashboard
- `raptors_analysis.ipynb` - Python statistical analysis
- `raptors.xlsx` - Source data

---

## Author

**Michael Kong**  
Data Analyst | SQL | Python | Power BI  

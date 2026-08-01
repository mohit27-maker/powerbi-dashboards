# 🏏 IPL Performance & Team Strategy Analysis (2008–2024)

![IPL Analysis](https://img.shields.io/badge/Domain-Sports%20Analytics-blue)
![Tools](https://img.shields.io/badge/Tools-SQL%20%7C%20Power%20BI%20%7C%20Excel-yellow)
![Data](https://img.shields.io/badge/Data-1095%20Matches%20%7C%20260K%2B%20Deliveries-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📌 Project Overview

This project analyzes **16 years of IPL data (2008–2024)** from the perspective of a **franchise consultant** — uncovering player value, toss impact, venue patterns, and team strategy using SQL, Python, and Power BI.

Rather than just exploring cricket statistics, this project frames every finding as a **business insight** that a franchise scout or team strategist would actually use to make decisions.

---

## 🎯 Business Questions Answered

1. **Which batsmen deliver the best performance in powerplay vs death overs?**
2. **Does winning the toss actually help — and does it vary by venue?**
3. **Which bowlers perform better under finals pressure vs league stage?**
4. **Which teams rely on home advantage and which thrive away?**

---

## 🗂️ Dataset

**Source:** [Kaggle — IPL Complete Dataset 2008–2024](https://www.kaggle.com/)

| File | Rows | Columns | Description |
|------|------|---------|-------------|
| `matches.csv` | 1,095 | 20 | Match-level data — venues, toss, results |
| `deliveries.csv` | 2,60,920 | 17 | Ball-by-ball data across all matches |

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| **Google Colab** | Analysis environment |
| **Python (Pandas)** | Loading and bridging CSV data |
| **SQLite3** | In-memory SQL database for all analysis |
| **Power BI** | Interactive 3-page dashboard |
| **Power Query** | Data cleaning and transformation |

---

## 📁 Project Structure

```
IPL-Analysis-2008-2024/
│
├── IPL_SQL_Analysis.ipynb        # Google Colab notebook with all SQL queries
│
├── IPL_Analysis_2008_2024.pbix   # Power BI dashboard (3 pages)
│
├── data/
│   ├── matches.csv               # Raw match data
│   └── deliveries.csv            # Raw ball-by-ball data
│
├── query_outputs/
│   ├── query1_batting_phases.csv # Top 10 batsmen: Powerplay vs Death overs
│   ├── query2_toss_venue.csv     # Win % by toss decision per venue
│   ├── query3_bowler_economy.csv # Bowler economy: Finals vs League
│   └── query4_home_away.csv      # Team performance: Home vs Away
│
└── README.md
```

---

## 🔍 SQL Analysis (Phase 1)

All analysis was done using **SQLite3 inside Google Colab** — no external database setup required.

### Query 1 — Top 10 Batsmen: Powerplay vs Death Overs
> Identifies specialist batsmen by phase using conditional aggregation and strike rate calculation.

**Key Finding:** AB de Villiers leads death overs with a strike rate of **223.78** across 1,421 runs — making him the most valuable finisher in IPL history by both volume and efficiency. CH Gayle dominates the powerplay (2,314 runs, 138.81 SR) confirming his role as a specialist opener.

---

### Query 2 — Win % by Toss Decision per Venue
> Calculates toss-to-win conversion rate across all venues with 10+ matches.

**Key Finding:** Sawai Mansingh Stadium shows the strongest toss advantage — teams winning the toss win **67.86%** of matches there. Eden Gardens heavily favors toss winners choosing to field (63.27% win rate across 49 matches).

---

### Query 3 — Bowler Economy: Finals vs League Stage
> Compares economy rates of bowlers who appeared in 2+ finals vs their league performance.

**Key Finding:** AR Patel stands out as the best pressure bowler — economy of just **4.53 in finals** vs 7.32 in league stages. Interestingly, SL Malinga's finals economy (7.18) is higher than his league economy (7.03) — suggesting even legends can struggle under final pressure.

---

### Query 4 — Team Performance: Home vs Away
> Uses UNION ALL to calculate home and away win percentages for every franchise.

**Key Finding:** Lucknow Super Giants have the highest home win rate (**72.73%**) but drop to 38.10% away — most home-dependent team in IPL. Gujarat Titans are a rare exception — they actually perform better away (70.83%) than at home (52.38%).

---

## 📊 Power BI Dashboard (Phase 2)

The dashboard consists of **3 interactive pages:**

### Page 1 — Match Overview
- Total IPL Wins by Team (Bar Chart)
- Toss Decision Distribution (Pie Chart)
- Matches Played per Season (Line Chart)
- Venue wise Match Summary (Table)

### Page 2 — Batting Intelligence
- Powerplay vs Death Runs by Batsman (Clustered Bar Chart)
- Strike Rate: Powerplay vs Death Overs (Column Chart)
- Top 10 Batsmen Phase-wise Performance (Table)

### Page 3 — Franchise Strategy
- Home vs Away Win % by Team (Clustered Bar Chart)
- Bowler Economy: Finals vs League Stage (Bar Chart)
- Toss Impact by Venue (Table)

---

## 💡 Key Insights Summary

| # | Insight |
|---|---------|
| 1 | AB de Villiers is the greatest death overs finisher — 223.78 SR across 1,421 runs |
| 2 | 64.29% of toss winners choose to field first across all IPL seasons |
| 3 | Sawai Mansingh Stadium has the highest toss-win correlation (67.86%) |
| 4 | AR Patel's finals economy (4.53) is 38% better than his league economy |
| 5 | Gujarat Titans are the only IPL team with a better away record than home |
| 6 | Mumbai Indians and CSK maintain 50%+ win rates both home and away |

---

## 🚀 How to Run

### SQL Notebook:
1. Open `IPL_SQL_Analysis.ipynb` in Google Colab
2. Upload `matches.csv` and `deliveries.csv`
3. Run all cells in order

### Power BI Dashboard:
1. Open `IPL_Analysis_2008_2024.pbix` in Power BI Desktop
2. If data doesn't load, update the file path in **Transform Data**

---

## 👤 Author

**Mohit Sengar**  
Aspiring Data Analyst | SQL • Power BI • Excel  
📧 Connect on [LinkedIn](#)  
🐙 More projects on [GitHub](#)

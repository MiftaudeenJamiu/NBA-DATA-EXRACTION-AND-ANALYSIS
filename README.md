# 🏀 NBA Players Performance Analysis

## 📑 Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Extraction](#data-extraction)
- [Data Cleaning/Preparation](#data-cleaningpreparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis (SQL)](#data-analysis-sql)
- [Visualisation (Power BI)](#visualisation-power-bi)
- [Results/Findings](#resultsfindings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

---

## 📊 Project Overview

This end-to-end analytics project evaluates the performance of NBA players across multiple seasons and season types. It highlights data gathering, cleaning, querying, and visualisation to derive insights and strategic recommendations.

---

## 🗃️ Data Sources

- **Raw NBA Stats**: Scraped from [NBA.com/stats](https://www.nba.com/stats) using Python.
- **Structured Data**: Stored and transformed in SQL Server.
- **Final Reporting**: Visualized in Power BI.

---

## 🛠️ Tools Used

| Tool         | Purpose                             |
|--------------|-------------------------------------|
| Python       | Web scraping (`requests`, `pandas`) |
| SQL Server   | Data transformation & analysis      |
| Power BI     | Dashboard and reporting             |
| Excel        | Preliminary data inspection         |

---

## 🕸️ Data Extraction

Using Python, player statistics were scraped across different seasons:

- Points (PTS), Assists (AST), Rebounds (REB)
- Field Goals Made (FGM), 3-Pointers Made (FG3M), Free Throws Made (FTM)
- Minutes Played (MIN), Games Played (GP), Steals (STL)

📁 .[Python Notebook:](https://github.com/MiftaudeenJamiu/NBA-DATA-EXRACTION-AND-ANALYSIS/blob/8a5d3e51d365b2ab0e7aa28d9c9251960c652c90/NBA%20SQL%20queries.ssmssln)

---

## 🧹 Data Cleaning/Preparation

Cleaning was performed in SQL:

- Decoded season type URLS (e.g., `Regular%20Season`)
- Renamed ambiguous column headers for readability
- Removed irrelevant or missing records
- Standardised column data types and created a view
- 📄 [View NBA SQL Queries](https://github.com/MiftaudeenJamiu/NBA-DATA-EXRACTION-AND-ANALYSIS/blob/a066f6e0e81571bc63a0faef90699466ba6e94ce/NBA%20SQL%20queries.ssmssln)


## Exploratory Data Analysis
EDA was performed to identify:

High-scoring players over multiple years

Trends in assists, rebounds, and shooting efficiency

Impact of games played (GP) and minutes (MIN) on productivity

Performance variations between Regular Season, Playoffs, and Play-In

## Key visualisations:

Distribution of Points and Assists

Average stats per season type

Correlation matrix between performance metrics

##  🧮 Data Analysis (SQL)
The cleaned dataset was queried to answer key questions

SELECT
    player_name,
    year,
    season_type,
    GP,
    MIN,
    FG,
    "3P",
    FTM,
    PTS,
    REB,
    AST,
    STL
FROM PlayerPerfomance
ORDER BY player_name, year;
Insights from SQL queries were used as the backbone for Power BI dashboards.

## 📊 Visualization (Power BI)
Final insights were visualised using Power BI.
🔗 Interactive Dashboard:  [View here](https://github.com/MiftaudeenJamiu/NBA-DATA-EXRACTION-AND-ANALYSIS/blob/a066f6e0e81571bc63a0faef90699466ba6e94ce/NBA%20SQL%20queries.ssmssln)

Dashboard includes:

Filters for player, year, and season type

Top 10 players by points, assists, and rebounds

Season-over-season trends

Comparison of performance in Playoffs vs Regular Season.
Below are what some of the player performance looks like
![Lebron Dashboard pb](https://github.com/user-attachments/assets/c2508922-a28a-47e1-898c-b2ba4af2ad15)
![Jamal Murray Dasboard Pb](https://github.com/user-attachments/assets/03cf0eec-3942-400d-9caf-877a5393567a)
![Stephen Curry Dashboard Pb](https://github.com/user-attachments/assets/da54399c-23cc-4f25-8f8f-8f9a4999e790)
![Giannis Dashboard pb](https://github.com/user-attachments/assets/2a8b6f97-e27f-4ee0-898b-e76ec987b83c)


## 📌 Results/Findings
Performance Spikes: Many star players see significant increases in key stats during Playoffs.

Consistency is Key: Players with high GP and MIN are top contributors in most categories.

Top Performers: Identified consistent all-around players across multiple seasons.

Seasonal Patterns: The Regular Season has more variability in performance; Playoffs reflect peak effort.

##  ✅ Recommendations
Scouting: Prioritise consistent players across all metrics when selecting rosters.

Performance Bonuses: Align incentives with playoff efficiency and reliability.

Coaching Strategy: Adjust game-time based on historic playoff performances.

Statistical Monitoring: Implement tools to automatically detect performance drops early.

##  ⚠️ Limitations
Some season types were URL-encoded (e.g., Regular%20Season), requiring manual correction.

Data reflects aggregate player-level stats only — lacks game-by-game breakdown.

A few outliers in minutes and points affected the visual scale (not removed to retain data integrity).

Scraping is sensitive to Nba.com structure changes — automation may break without updates.

## 📚 References
NBA Official Stats

Stack Overflow (for web scraping & SQL)

Power BI Docs

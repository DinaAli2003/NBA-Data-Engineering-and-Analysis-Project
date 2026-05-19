# 🏀 NBA Data Engineering & Analytics Project

> *A complete data warehousing and analytics solution for historical NBA data – from raw SQLite to a star‑schema data warehouse in SQL Server, powering interactive Power BI dashboards.*





> *This project was developed as part of the **Digilians Initiative** – a collaborative program supervised by the **Ministry of Communication and Information Technology (MCIT)** and the **Egyptian Military Academy**.*
---

## 📌 Overview

This project transforms raw, transactional NBA data into a **structured, analytics‑ready data warehouse**. The original dataset (SQLite from Kaggle) was cleaned, remodeled into a **star schema**, and loaded into **SQL Server**. The final warehouse supports high‑performance analytical queries and fuels an interactive **Power BI dashboard** for game performance, team trends, draft scouting, and combine analytics.

---

## 📊 Original Dataset (Kaggle)

| Attribute | Details |
| :--- | :--- |
| **Source** | [NBA Database on Kaggle](https://www.kaggle.com/datasets/wyattowalsh/basketball) by Wyatt Walsh |
| **Time Span** | 1946–47 to present |
| **Scope** | 65,000+ games, 4,800+ players, 30 teams |
| **Contents** | Box scores for 95%+ of games, 13M+ play‑by‑play rows, draft history, combine stats, and more |
| **Format** | SQLite database (`nba.sqlite`) |

---

## 🔧 Key Components

### 🧹 Data Cleaning & Integration
- Resolved **data type inconsistencies** (strings in numeric fields, conversion failures)
- Removed **duplicate records** across all tables
- Handled **missing data** by inserting placeholder dimension records
- Fixed **missing foreign key references** – added missing team/player dimension rows to preserve fact table integrity

### 🏗️ Data Warehouse Design (Star Schema)

We converted the original transactional model into a **star / galaxy schema** for analytics:

| Fact Table | Description |
| :--- | :--- |
| `Fact_Game` | Game‑level metrics (points home/away, FG%, rebounds, assists, date, team references) |
| `Fact_Draft` | Draft history – picks linked to players and teams |
| `Fact_Combine` | Pre‑draft scouting measurements (vertical jump, sprint, percentages) |

**Dimension Tables**: `Dim_Player`, `Dim_Team`, `Dim_Date`, `Dim_Game_Info`

Relationships are **one‑to‑many** from dimensions to facts – optimized for slicing and filtering in Power BI.

### 📈 SQL Analytics (Sample Queries)
- **Game performance**: home/away win %, point differentials, close games
- **Team efficiency**: offensive/defensive rankings, clutch performance
- **Season trends**: scoring, assists, rebounds over time
- **Player combine metrics**: vertical jump, sprint speed, BMI analysis

### 📊 Power BI Dashboard Insights

| Metric | Value |
| :--- | :--- |
| Total Games Analyzed | 58,000+ |
| Total Points Scored | 12 million+ |
| Home Win % | 61.95% |
| Away Win % | 38.05% |
| Top Scoring Franchises | Celtics, Warriors, Lakers, 76ers, Knicks |
| Draft Picks Analyzed | 3,506 |
| Average Draft Position | 30.78 |
| Historical Scoring Trend | 1946–1965 (early 1950s peaks) |

---

## 📂 Repository Structure
NBA-Data-Analytics-Project/

├── Database/ # Cleaned dataset (schema only – sample rows)

├── DWH/ # SQL scripts for warehouse creation & analytical queries

├── Power BI/ # Dashboard file (.pbix) and screenshots

├── docs/ # Additional documentation (optional)

└── README.md # This file


---

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/NBA-Data-Analytics-Project.git



## 🙏 Thank You

For questions or collaboration opportunities, please reach out to the team.


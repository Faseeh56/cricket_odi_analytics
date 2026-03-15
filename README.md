## 📊 End‑to‑End ODI Cricket Analysis Using Python

This project transforms **raw ball‑by‑ball JSON data** from **3,099 ODI matches** into meaningful performance insights.  
It processes **1.6+ million deliveries**, calculates comprehensive batting and bowling statistics, builds advanced player metrics, and selects a **data‑driven All‑Time ODI XI**.

---

## 🚀 Project Highlights

- Processed **1,639,277 ball‑by‑ball deliveries**
- Analyzed **3,099 ODI matches** (2002 – present)
- Computed career stats for **2,505 batters** and **1,925 bowlers**
- Developed an **All‑Rounder Impact Score**
- Ranked **wicketkeepers** by a combined batting‑keeping score
- Generated **7+ analytical visualizations**
- Created a **data‑driven All‑Time ODI XI**

---

## 📂 Repository Structure
cricket-data-analytics/
│  
├── data/  
│ ├── raw/ # Original JSON files   
│ └── processed/ # Cleaned CSV files  
│  
├── notebooks/  
│ ├── 01_data_extraction.ipynb  
│ ├── 02_batting_analytics.ipynb  
│ ├── 03_bowling_analytics.ipynb  
│ └── 04_all_rounder_analytics.ipynb  
| └── 04_wicket_keepers_analytics.ipynb  
│  
├── output/  
│ ├── batting_stats.csv  
│ ├── bowling_stats.csv  
│ ├── allrounder_stats.csv  
│ ├── wicketkeeper_stats.csv  
│ └── Visuals/   
│  
├── README.md  
└── .gitignore  

---

## 📊 Dataset

- **Source:** [Cricsheet](https://cricsheet.org/) – ODI Internationals
- **Matches:** 3,099
- **Deliveries:** 1,639,277
- **Batters:** 2,505
- **Bowlers:** 1,925
- **Wickets:** 44,877
- **Teams:** 28
- **Super Over matches:** 9

Each delivery contains:
- Batter, bowler, non‑striker
- Runs scored (batter & total)
- Extras
- Wicket information (type, player out, fielder)
- Over and ball number

---

## ⚙️ Data Engineering Pipeline

Raw JSON match files contain nested structures for innings, overs, and deliveries.  
The extraction pipeline:

1. Parses all JSON files
2. Extracts every delivery into a flat row
3. Adds derived features: `is_four`, `is_six`, `dot_ball`, `phase` (Powerplay, Middle, Death)
4. Outputs a structured DataFrame with **21 columns**

---

## 📈 Batting Analytics

### Metrics Calculated

| Metric        | Formula                              |
|---------------|--------------------------------------|
| Innings       | `COUNT(DISTINCT match_id, inning)`   |
| Runs          | `SUM(runs_batter)`                   |
| Balls Faced   | `COUNT(*)`                           |
| Strike Rate   | `(Runs / Balls) × 100`               |
| Average       | `Runs / Dismissals`                  |
| Not Outs      | `Innings - Dismissals`                |
| Fours         | `COUNT(runs_batter = 4)`              |
| Sixes         | `COUNT(runs_batter = 6)`              |
| 50s / 100s    | Innings scores ≥ 50 / ≥ 100           |
| Highest Score | `MAX(innings score)`                  |

### Top Run‑Scorers

| Rank | Player              | Runs    |
|------|---------------------|---------|
| 1    | Virat Kohli         | 14,675  |
| 2    | Kumar Sangakkara    | 11,640  |
| 3    | Rohit Sharma        | 11,357  |
| 4    | MS Dhoni            | 10,274  |
| 5    | AB de Villiers      |  9,435  |

---

## 📉 Bowling Analytics

### Metrics Calculated

| Metric          | Formula                            |
|-----------------|------------------------------------|
| Overs           | `Balls / 6`                        |
| Economy         | `Runs Conceded / Overs`            |
| Average         | `Runs Conceded / Wickets`          |
| Strike Rate     | `Balls / Wickets`                  |
| Dot Ball %      | `(Dot Balls / Balls) × 100`        |
| 4‑wicket hauls  | `COUNT(wickets ≥ 4 in match)`      |
| 5‑wicket hauls  | `COUNT(wickets ≥ 5 in match)`      |

### Top Wicket‑Takers

| Rank | Player            | Wickets |
|------|-------------------|---------|
| 1    | Lasith Malinga    | 343     |
| 2    | Brett Lee         | 281     |
| 3    | Shakib Al Hasan   | 279     |
| 4    | James Anderson    | 268     |
| 5    | Shahid Afridi     | 259     |

---

## 📊 Advanced Analytics

### All‑Rounder Impact Score

To fairly compare all‑rounders, a balanced score was created:

Batting Impact = (Player Runs / Max Runs) × 50
Bowling Impact = (Player Wickets / Max Wickets) × 50
All‑Rounder Score = Batting Impact + Bowling Impact


**Top All‑Rounders**

| Rank | Player            | Impact Score |
|------|-------------------|--------------|
| 1    | Shakib Al Hasan   | 70.29        |
| 2    | TM Dilshan        | 58.95        |
| 3    | Mohammad Hafeez   | 54.60        |
| 4    | Shahid Afridi     | 53.78        |
| 5    | Shane Watson      | 53.52        |

### Wicketkeeper Ranking

Keepers were evaluated on a 50‑50 split between batting and keeping (catches + stumpings).

| Rank | Player            | Runs   | Dismissals | Keeper Score |
|------|-------------------|--------|------------|--------------|
| 1    | KC Sangakkara     | 11,640 | 399        | 96.83        |
| 2    | MS Dhoni          | 10,274 | 426        | 94.13        |
| 3    | Mushfiqur Rahim   |  7,096 | 263        | 61.35        |
| 4    | Q de Kock         |  7,014 | 225        | 56.54        |
| 5    | AC Gilchrist      |  4,355 | 205        | 42.76        |

---

## 🖼️ Visualizations

The project includes:
- **Top Run‑Scorers & Wicket‑Takers** – bar charts
- **Batting Average vs. Strike Rate Quadrant** – identifies elite batters
- **Bowling Economy vs. Average Quadrant** – identifies elite bowlers
- **All‑Rounder Impact Comparison**
- **Phase Analysis** – runs & wickets in Powerplay, Middle, Death overs


---

## 🏆 All‑Time ODI XI (Data‑Driven)

| Pos | Player            | Role                |
|-----|-------------------|---------------------|
| 1   | Rohit Sharma      | Opener              |
| 2   | Quinton de Kock   | Opener              |
| 3   | Virat Kohli       | Anchor              |
| 4   | AB de Villiers    | Power Middle        |
| 5   | Kumar Sangakkara  | Middle Order        |
| 6   | MS Dhoni (c/wk)   | Finisher            |
| 7   | Shakib Al Hasan   | All‑Rounder         |
| 8   | Shane Watson      | All‑Rounder         |
| 9   | Lasith Malinga    | Fast Bowler         |
| 10  | Mitchell Starc    | Fast Bowler         |
| 11  | Brett Lee         | Fast Bowler         |

---

## 🔑 Key Insights

- **Virat Kohli** is the most consistent batter (14,675 runs @ 58.47, 54 centuries).
- Only **5% of batters** fall into the elite quadrant (avg > 45, SR > 90).
- **Lasith Malinga** leads all bowlers with 343 wickets, excelling in death overs.
- **Shakib Al Hasan** is the most impactful all‑rounder; only 12 players have 5,000+ runs and 200+ wickets.
- **MS Dhoni** has the most stumpings (118) – nearly double any other keeper.
- Death overs produce **7.8 RPO** vs. Powerplay **4.8 RPO**, with double the wicket rate.

---

## 🛠️ Technologies Used

- **Python** 3.9+
- **Pandas** – data manipulation
- **NumPy** – numerical operations
- **Matplotlib & Seaborn** – visualizations
- **Jupyter Notebook** – interactive development

---

## 🔮 Future Work

- Predictive models for match outcomes
- Interactive dashboard with Power BI / Tableau
- Venue‑specific performance analysis
- Head‑to‑head player comparisons
- Real‑time cricket analytics

---

## 📬 Connect With Me

- **LinkedIn:** [Faseeh Qamar](https://linkedin.com/in/m-faseeh-qamar-8b3194358)
- **GitHub:** [Your GitHub Profile](https://github.com/Faseeh56)

---

⭐ **If you like this project, give it a star on GitHub!**  

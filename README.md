🏏 Cricket Data Analytics Project

📊 End-to-End ODI Cricket Analysis Using Python

This project presents a comprehensive cricket data analytics system built using Python.

It processes 1.6+ million ball-by-ball deliveries from 3,099 ODI matches and transforms raw JSON match data into meaningful performance insights.

The project covers data engineering, statistical analysis, advanced player metrics, and visualization to identify the greatest ODI performers of all time.

🚀 Project Highlights

✔ Processed 1,639,277 ball-by-ball deliveries

✔ Analyzed 3,099 ODI matches

✔ Computed career batting and bowling statistics

✔ Built All-Rounder Impact Score

✔ Ranked Wicketkeepers based on dismissals

✔ Generated 7+ analytical visualizations

✔ Created a data-driven All-Time ODI XI

📂 Project Structure

cricket-data-analytics/

│

├── data/

│ ├── raw_json_matches

│ └── processed_dataset.csv

│

├── notebooks/

│ ├── batting_analysis.ipynb

│ ├── bowling_analysis.ipynb

│ └── allrounder_analysis.ipynb

│

├── visualizations/

│ ├── top_run_scorers.png

│ ├── top_wicket_takers.png

│ ├── batting_quadrant_chart.png

│ └── bowling_quadrant_chart.png

│

├── docs/

│ └── project_documentation.pdf

│

└── README.md

📊 Dataset

Dataset Source: Cricsheet ODI Ball-by-Ball Data

Key dataset statistics:

Metric Value

Total Matches 3,099

Total Deliveries 1,639,277

Total Batters 2,505

Total Bowlers 1,925

Total Wickets 44,877

Each delivery contains detailed information including:

Batter

Bowler

Runs scored

Extras

Wicket type

Fielders involved

Over and ball number

⚙️ Data Engineering Pipeline

Raw JSON match files contain nested structures for innings, overs, and deliveries.

The pipeline performs:

1️⃣ JSON parsing

2️⃣ Ball-by-ball extraction

3️⃣ Feature engineering

4️⃣ Dataset structuring

Workflow

Raw JSON Match Files

↓

Python Data Extraction

↓

Data Cleaning

↓

Feature Engineering

↓

Structured Dataset

↓

Analytics & Visualization

📈 Batting Analytics

Batting metrics computed:

Total Runs

Balls Faced

Batting Average

Strike Rate

Fours

Sixes

Half Centuries

Centuries

🏏 Top Run Scorers

Rank Player Runs

1 Virat Kohli 14,675

2 Kumar Sangakkara 11,640

3 Rohit Sharma 11,357

4 MS Dhoni 10,274

5 AB de Villiers 9,435

Virat Kohli dominates ODI batting with exceptional consistency and strike rate.

📉 Bowling Analytics

Bowling performance metrics:

Wickets Taken

Runs Conceded

Economy Rate

Bowling Average

Bowling Strike Rate

🎯 Top Wicket Takers

Rank Player Wickets

1 Lasith Malinga 343

2 Brett Lee 281

3 Shakib Al Hasan 279

4 James Anderson 268

5 Shahid Afridi 259

Lasith Malinga leads the bowling charts due to his dominance in death overs.

📊 Advanced Analytics

All-Rounder Impact Score

To evaluate all-rounders fairly, a custom Impact Score was developed.

Formula:

Batting Impact = (Player Runs / Max Runs) × 50

Bowling Impact = (Player Wickets / Max Wickets) × 50

All-Rounder Score = Batting Impact + Bowling Impact

Top All-Rounders

Rank Player Impact Score

1 Shakib Al Hasan 70.29

2 Tillakaratne Dilshan 58.95

3 Mohammad Hafeez 54.60

4 Shahid Afridi 53.78

5 Shane Watson 53.52

🧤 Wicketkeeper Analysis

Wicketkeepers were evaluated based on:

Batting performance

Catches

Stumpings

Total dismissals

Top Wicketkeepers

Player Total Dismissals

MS Dhoni 426

Kumar Sangakkara 399

Quinton de Kock 225

Adam Gilchrist 205

MS Dhoni leads the charts with the highest number of stumpings.

📊 Visualizations

The project includes several analytical charts:

📈 Top Run Scorers

📉 Top Wicket Takers

📊 Batting Average vs Strike Rate Quadrant

📊 Bowling Economy vs Average Quadrant

📊 All-Rounder Impact Score Comparison

These visualizations help identify elite performers and performance patterns.

🏆 All-Time ODI XI (Data-Driven)

Based on analytical metrics, the following All-Time ODI XI was selected.

Openers

Rohit Sharma

Quinton de Kock

Top Order

Virat Kohli

AB de Villiers

Kumar Sangakkara

Middle Order

MS Dhoni (Captain & Wicketkeeper)

All-Rounders

Shakib Al Hasan

Shane Watson

Bowlers

Lasith Malinga

Mitchell Starc

Brett Lee

🔑 Key Insights

📌 Virat Kohli is the most consistent ODI batter.

📌 Lasith Malinga leads all bowlers in wickets.

📌 Shakib Al Hasan emerges as the most impactful all-rounder.

📌 Only a small percentage of batters fall into the elite performance quadrant.

📌 Death overs contribute the highest scoring rates in ODI cricket.

🛠 Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Jupyter Notebook

📌 Future Improvements

Machine learning models for match prediction

Interactive dashboards using Power BI or Tableau

Venue-based performance analysis

Player head-to-head comparisons

Real-time cricket analytics

⭐ Conclusion

This project demonstrates how data analytics techniques can be applied to sports performance analysis.

By processing over 1.6 million deliveries, the system extracts meaningful insights about player performance and identifies the greatest ODI players using a data-driven approach.

📬 Connect With Me

If you like this project or want to collaborate:

LinkedIn: Add your profile link

GitHub: Add your GitHub profile

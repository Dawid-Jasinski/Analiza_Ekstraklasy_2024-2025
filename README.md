🏆 Ekstraklasa 2024/25 – Data Analysis & Predictive Modeling
Author: Dawid Jasiński
Technologies: Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit‑Learn), Excel
Data Source: FBref.com

🔍 Project Overview
This project presents a complete analytical study of the Polish Ekstraklasa 2024/25 season.
It includes:

full data cleaning & integration from multiple FBref sheets,
exploratory data analysis (EDA),
statistical comparison of teams,
linear regression model predicting expected points (xPts),
identification of over/underperforming teams,
professional report in PL + EN.

The goal was to understand what drives success in Ekstraklasa and which variables statistically explain the number of points earned.
This project is built in the style of a real data‑analytics case study, covering the entire workflow:
problem → data → cleaning → EDA → modeling → interpretation → report.

📁 Repository Structure
├── data
│   ├── raw
│   │   └── Dane_Ekstraklasa.xlsx
│   └── processed
│       └── ekstraklasa_clean.csv
│
├── notebooks
│   ├── 01_data_cleaning.ipynb
│   ├── 02_EDA.ipynb
│   └── 03_modeling.ipynb
│
├── report
│   ├── ekstraklasa_24_25_PL.pdf
│   └── ekstraklasa_24_25_EN.pdf
│
└── README.md


🧹 1. Data Cleaning & Preparation
Raw data from FBref were spread across multiple sheets and required:

cleaning team names (removing HTML fragments),
type conversion (numeric/strings),
selecting relevant variables,
merging datasets into one consistent DataFrame.

The final dataset includes:

18 teams
28 variables (attacking, defensive, efficiency, possession, shooting, goalkeeping)

Cleaned dataset saved as:
data/processed/ekstraklasa_clean.csv

📊 2. Exploratory Data Analysis (EDA)
Key insights:
⚽ League Overview

Lech Poznań dominated offensively and maintained one of the highest possession rates.
Raków had the strongest defensive performance (fewest goals conceded).
Teams like Puszcza, Stal Mielec, Zagłębie struggled in both attack and defense.

📈 Statistical Relationships

Efficiency metrics (G/Sh, G/SoT) correlate strongest with total points.
Possession shows only moderate correlation with success.
Goal difference (GD) explains 95% of points variation.

🧬 Team Profiles
Radar charts show strong contrast between TOP4 and relegation teams — in volume, efficiency, and defensive solidity.
A case study comparing Lech vs Widzew illustrates how cumulative small advantages across many metrics translate into big point differences.

🤖 3. Predictive Modeling (Linear Regression)
The model uses standardized variables:

goals scored / conceded
possession
shots per 90
shots on target per 90
goals per shot (G/Sh)
goals per shot on target (G/SoT)

📌 Model performance:

R² = 0.95 (excellent explanatory power)
strongest positive predictor: G/SoT
strongest negative: GA (goals conceded)

The model was used to compute Expected Points (xPts) for each team.
🟥 Underperformers:
Śląsk, Radomiak, Puszcza
🟩 Overperformers:
Korona, Motor Lublin, Jagiellonia
These differences highlight tactical, mental, or structural factors not captured directly in raw statistics.

📝 4. Key Insights

Success in Ekstraklasa is driven mainly by finishing efficiency and defensive stability, not by possession alone.
Top teams combine volume, quality, and structure — bottom teams lack at least two of these elements.
Regression confirms that goal difference and efficiency metrics statistically explain table position.


🎯 5. Recommendations

Relegation teams should focus on increasing chance creation volume and improving defensive structure.
Offense should prioritize shot quality, not just volume.
Clubs underperforming xPts should analyze key game phases and late‑game situations.
Wider use of analytics (xPts, finishing quality, defensive patterns) can improve strategic decisions.


🗂 6. Reports
Full professional reports available in:

Polish → report/ekstraklasa_24_25_PL.pdf
English → report/ekstraklasa_24_25_EN.pdf


🚀 7. Technologies

Python: pandas, numpy, matplotlib, seaborn, scikit‑learn
Jupyter Notebook (analysis & modeling)
Excel (raw data inspection)

⚙️ 8. AI‑Assisted Development Notice
Some parts of the project were supported by AI‑assisted coding tools (e.g., Copilot/ChatGPT) to streamline code generation and improve workflow efficiency.
All analytical logic, data interpretation, conclusions, visualizations and the full written report were created, verified and curated by the author.

🙋 About the Author
I am a student of econometrics and data analytics, developing my portfolio for a Junior Data Analyst position.
This project was created as a complete data‑analytics case study, from data cleaning to modeling.
If you want to discuss the project or collaborate — feel free to reach out!

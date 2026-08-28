📱 Google Play Store Data Analysis

App Performance & User Engagement Dashboard — an end-to-end data analytics project covering data cleaning, exploratory data analysis (EDA), and dashboarding on the Google Play Store Apps dataset.
📖 Overview

This project analyzes 9,745 Google Play Store app listings to uncover patterns in app categories, user ratings, installs, reviews, and pricing. The workflow covers the full analytics pipeline:

Data Cleaning — handling missing values, removing redundant columns, fixing data types (Python / Pandas, Jupyter Notebook)
Exploratory Data Analysis — category trends, rating patterns, free vs. paid comparison, correlation analysis (Pandas, Matplotlib, Seaborn)
Dashboarding — an interactive Power BI report summarizing key metrics and visuals for business-style reporting
🎯 Objective

To answer questions like:

Which app categories have the most apps and the highest ratings?
Do free apps outperform paid apps in installs and engagement?
Does app price or review count actually influence its rating?
Which apps and categories dominate the Play Store in installs and reviews?
📂 Project Structure
Google-Playstore-Analysis/
│
├── data/
│   ├── Google_Playstore_Apps.csv         # Raw dataset (input)
│   └── google_playstore_cleaned.csv      # Cleaned dataset (notebook output)
│
├── notebook/
│   └── Google_Play_Store.ipynb           # Data cleaning + EDA
│
├── dashboard/
│   └── Google_Playstore_Analysis.pbix    # Power BI dashboard
│
├── images/
│   └── dashboard_screenshot.png          # Screenshot of the Power BI report
│
└── README.md
🗃️ Dataset
Source: Google Play Store Apps dataset (Kaggle)
Rows: 9,745 | Columns: 9 (App, Category, Rating, Reviews, Installs, Type, Price, Genres, Last Updated)
Size: ~9,700 apps across 33 categories
🧹 Data Cleaning Steps
Step	Description
Remove redundant column	Dropped the unused Unnamed: 0 index column
Duplicate check	Verified no fully duplicate rows exist
Missing values	Imputed 1,464 missing Rating values using category-wise mean (more accurate than a single global mean)
Data types	Converted Last Updated to proper datetime format
Feature engineering	Binned Installs into readable ranges (0–1K, 1K–10K, …, 100M–1B)
Export	Saved the cleaned dataset as google_playstore_cleaned.csv, used as the Power BI data source
📊 Key Insights
📦 FAMILY, GAME, and TOOLS are the most crowded categories by app count.
⭐ EVENTS apps have the highest average rating (4.44); DATING apps have the lowest (3.97).
💰 Free apps massively outperform paid apps in installs (~116×) and reviews (~29×) — but paid apps have a slightly higher average rating (4.25 vs 4.17).
🔗 Installs and Reviews are moderately correlated (r ≈ 0.61) — popularity and engagement move together, but not perfectly.
📉 Reviews vs Rating (r ≈ 0.06) and Price vs Rating (r ≈ -0.11) are both very weak — more reviews or a higher price doesn't guarantee a better rating.
🎭 A cluster of near-duplicate "I am Rich" apps priced at ~$399.99 stand out as pricing outliers among paid apps.
📈 Power BI Dashboard

Includes:

KPI Cards → Total Apps, Average Rating, Total Reviews, Total Installs
Top 10 Categories by Number of Apps (bar chart)
Top 10 Categories by Installs (area chart)
Reviews vs Rating (scatter chart)
Free vs Paid Apps (donut chart)
App Distribution by Category (pie chart)
(screenshot of your dashboard)<img width="1437" height="807" alt="Screenshot 2026-08-28 130346" src="https://github.com/user-attachments/assets/51dccf56-474e-426f-9b2d-7c4ff14f3a51" />
🛠️ Tools & Technologies
Python — pandas, matplotlib, seaborn
Jupyter Notebook
Power BI Desktop
👤 Author
Your Name :- Vaishnavi Arun Ujjainkar

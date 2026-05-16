# OtakuAnalytics-Filtering-the-Masterpieces
========================== A Python data science pipeline using Pandas to perform EDA, clean data noise, and engineer categorical features on a 12k+ anime dataset =========================

# Anime Insights: Exploratory Data Analysis & Feature Engineering

A Python-based data science project that performs Exploratory Data Analysis (EDA) and Feature Engineering on a comprehensive dataset of over 12,000 anime entries. The goal of this project is to build a programmatic data pipeline that cleans data noise, engineers categorical features, and extracts universally acclaimed masterpieces by filtering out statistical outliers.

## 🚀 Key Features & Logic

* Data Cleaning & Noise Reduction:** Implemented a threshold bouncer using mathematical means ($\mu_{\text{members}}$) to eliminate "lucky" high-rated entries with negligible voter counts   (outliers/noise).
* Feature Engineering:** Programmatically transformed raw numerical ratings into structured categorical segments (`Excellent`, `Good`, `Average`, `Poor`) for optimized filtering.
* Optimized Data Aggregation:** Utilized advanced Pandas slicing, sorting, and grouping methods (avoiding slow `for` loops) to analyze trends across different formats like TV, Movies, and OAs.
* **Production Export:** Developed an automated pipeline to output clean, production-ready subsets (e.g., *Top 100 Famous Masterpieces*) directly into highly portable `.csv` structures.

## 🛠️ Tech Stack

* Language:** Python 3.14+
* Environment: Jupyter Notebooks / VS Code
* Libraries:** Pandas, Numpy

## 📊 Core Pipeline Workflow

1. Calculate Global Baselines:** Compute the statistical mean for ratings and membership across the entire dataset.
2. Apply Popularity Filters:** Drop any entry falling below the average member count threshold to guarantee data relevance.
3. Sort and Slice:** Rank the remaining entries by rating to reveal universally recognized hits.
4. Export Clean Insights:** Pipe the top 100 refined data rows into an independent file for external analysis or visualization.

## 📁 Output Data
The project generates a refined `top_famous.csv` spreadsheet file tracking the highest-rated, statistically significant anime entries with columns including `name`, `genre`, `type`, `episodes`, `rating`, `members`, and `rating_category`.

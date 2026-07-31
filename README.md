MovieLens Data Analysis & Exploratory Insights

Overview
This project performs an end-to-end Exploratory Data Analysis (EDA) on the MovieLens dataset using modern data analysis tools. The primary objective is to analyze user rating behaviors, movie popularity distributions, genre dynamics, and content tagging patterns to extract meaningful business insights for recommendation engines and streaming platforms.

The analysis is optimized for high-performance data manipulation, memory efficiency, and concise query pipelines using Polars and Python.

Key Questions & Engineering Highlights
The analysis covers several key domain questions structured into distinct analytical modules:

Rating & Popularity Distribution: Evaluates rating counts per movie to understand long-tail viewer distributions and identifies top-rated titles filtered by interaction thresholds to remove bias.

Genre Dynamics & Performance: Parses multi-label genre fields to quantify unique genres, genre-specific average ratings, and volume metrics across the platform.

User Engagement & Re-Rating Patterns: Detects multi-rating behavior per user-movie pair, computing individual re-rating rates and segmenting power users.

Tagging Behavior Analysis: Measures content tagging depth per movie (min, max, and average bounds) and surfaces the overall most frequently applied user tags.

Statistical Correlation: Computes the Pearson correlation between a movie's total rating volume and its mean score to validate platform engagement biases.

Tech Stack & Methods
Language: Python 3.10+

Data Processing: Polars (DataFrame & Aggregation Engine)

Environment: Jupyter Notebook / Google Colab

Key Operations: Data Exploding, Complex Aggregations, Inner Joins, Multi-Condition Filtering, Correlation Analysis

Data Architecture & Workflow
Explode & Reshape: Unnested pipe-separated multi-label fields (e.g., genres) for precise granular group-by metrics without string matching overhead.

Aggregations & joins: Merged transactional ratings data with categorical movies metadata using key-indexed joins.

Statistical Filtering: Applied user/movie interaction thresholds (e.g., minimum 5 or 10 ratings) to preserve statistical significance in ranking tables.

How to Run
Clone the repository:

Bash
git clone https://github.com/your-username/movielens-analysis.git
cd movielens-analysis
Install dependencies:

Bash
pip install polars
Open and run the notebook:

Bash
jupyter notebook analysis.ipynb
Project Structure
Plaintext
├── data/              # MovieLens dataset files (movies.csv, ratings.csv, tags.csv)
├── analysis.ipynb     # Main analytical notebook containing queries B2-C6
└── README.md          # Project documentation and summary
Developed by Zahra Eldarova — Data & Business Analytics Project

# World_layoffs.layoffs_EDA_Project

 A comprehensive MySQL script to clean, standardize, and prepare the world_layoffs.layoffs dataset for exploratory data analysis (EDA).
This project transforms raw, redundant layoff records into a reliable, analysis-ready table by:

Removing duplicates

Standardizing data (names, industries, dates, countries)

Handling NULL/blank values

Removing unnecessary rows and columns

📁 Dataset
Source: world_layoffs.layoffs (global company layoff records, 2020–2023)

Database: MySQL 8.0+

Output table: layoffs_staging3 (clean, duplicate-free, standardized)

Characteristics:

No duplicate records

Consistent company, industry, and country names

Dates stored as DATE type

No completely empty layoff rows

Ready for EDA, visualization, or reporting (Tableau, Power BI, Python, etc.)


📊 Typical Follow-up Analyses
Total layoffs by country / industry / year

Trends over time (time-series of total_laid_off)

Top 10 companies by layoff count

Correlation between funds raised and layoff severity


🛠️ Requirements
MySQL 8.0+ (window functions required)

Database: world_layoffs

Input table: layoffs (raw)



📝 Notes & Lessons Learned
Always work on a staging table to preserve raw data.

Order of operations matters: deduplicate first, then standardize, then handle NULLs.

Self-joins are powerful for filling missing values from known records.

Trailing/leading whitespace and inconsistent naming can silently break groupings—always inspect DISTINCT values.

Date formats vary in real-world data; STR_TO_DATE with conditional logic is essential.

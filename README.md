1. 📌 Project Title & Description
# Netflix Movies Data Cleaning Project

This project involves cleaning and preprocessing the "Netflix Movies and TV Shows" dataset sourced from Kaggle. The goal is to prepare the data for analysis by handling missing values, standardizing formats, and ensuring consistency.

2. 🎯 Project Objectives
## Objectives
- Handle missing values in key columns (director, cast, country, rating)
- Standardize date and duration formats
- Normalize categorical data (e.g., country names)
- Prepare the dataset for further analysis or visualization

3. 📁 Dataset Overview
Describe the dataset:
## Dataset Description
- Source: [Netflix Movies and TV Shows on Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- Columns: show_id, type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, description, month added, and year added

4. 🛠️ Tools & Technologies
List the tools used:
## Tools & Technologies
- Excel

5. 🧪 Cleaning Steps
## Data Cleaning Steps
- Download the raw CSV file from Kaggle.
- Open Excel and import the file via File → Open → Browse or use Data → Get External Data → From Text/CSV.
Remove Duplicates
- Go to Data → Remove Duplicates.
- Select all columns or just show_id, title, and type to ensure uniqueness.
Handle Missing Values
- Use Filter to find blanks in columns like director, cast, country, rating.
- Replace missing values with "Unknown" using Find & Replace or formulas like:
=IF(A2="", "Unknown", A2)

6. 📅 Standardize Dates
- Column: date_added
- Use Text to Columns or formulas to convert inconsistent formats:
=TEXT(DATEVALUE(A2), "dd-mm-yyyy")

7. ⏱️ Split Duration
- Column: duration (e.g., "90 min", "1 Season")
- Use Text to Columns with space delimiter to split into:
- duration_value
- duration_unit

8. 🌍 Normalize Country Names
- Use Find & Replace or a lookup table to standardize country names (e.g., "United States" vs "USA").

9. 🎭 Clean Categorical Columns
- Columns: listed_in, type, rating
- Use TRIM, PROPER, and CLEAN functions to tidy text:
=PROPER(TRIM(CLEAN(A2)))

10. 🧮 Create New Columns (Optional)
- Extract year from date_added:
=YEAR(DATEVALUE(A2))
- Count number of cast members:
=LEN(A2)-LEN(SUBSTITUTE(A2,",",""))+1

11. 📤 Export Cleaned Data
- Save as a new file: File → Save As → cleaned_netflix.xlsx








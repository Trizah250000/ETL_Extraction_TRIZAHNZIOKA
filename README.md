# ETL Extract, Transform and Load 

Name: Trizah Nzioka  
Course: DSA 2040A - Data Warehousing and Mining  

---

## Description
A complete ETL pipeline using synthetic football match data.  
The project demonstrates:
- Full and Incremental Extraction
- Data Cleaning, Enrichment, and Structuring
- Loading into a structured SQLite database

---

## Tools Used
- Python
- Pandas
- SQLite (via sqlite3)
- Jupyter Notebook

---

## Dataset
Synthetic football dataset over 60 days.  
Each record contains:
- match_id, home_team, away_team
- home_score, away_score
- date, last_updated

---

## How to Run

1. Open and run `etl_extract.ipynb`:
   - Section 1: Full Extraction  
   - Section 2: Incremental Extraction  
   - Section 3: Save New Timestamp  
   - Section 4: Transform Full Data  
   - Section 5: Transform Incremental Data  

2. Then run `etl_load.ipynb`:
   - Section 1: Load Setup  
   - Section 2: Load Full Transformed Data  
   - Section 3: Load Incremental Transformed Data  
   - Section 4: Verification  

Note: `last_extraction.txt` helps track last update time for incremental runs.

---

## ETL Summary

### Extraction
- Full: Loads all data from `custom_data.csv`
- Incremental: Filters only records with `last_updated` > saved timestamp

### Transformation
Applied to both datasets:
1. Cleaning: Removed duplicate rows  
2. Structural: Standardized date columns to datetime  
3. Enrichment: Added `goal_diff = home_score - away_score`

### Load
- Loaded both transformed datasets into SQLite databases:
  - `loaded_data/full_data.db`
  - `loaded_data/incremental_data.db`
- Tables: `full_data`, `incremental_data`

---

## Output Files
- transformed_full.csv  
- transformed_incremental.csv  
- loaded_data/full_data.db  
- loaded_data/incremental_data.db

---

## Incremental Note
The process is repeatable:
- Rerun extraction to capture new updates
- Transformed and loaded files update accordingly

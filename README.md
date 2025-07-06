# ETL Extract & Transform Lab

Name: TRIZAH NZIOKA  
Course: DSA 2040A - Data Warehousing and Mining

---

## Description
This notebook demonstrates Full and Incremental Extraction and extends it with data transformation logic for analysis.

Part of a hands-on ETL pipeline using synthetic football match data.

---

## Tools Used
- Python
- Pandas
- Jupyter Notebook

---

## Dataset
A synthetic dataset of football matches over 60 days.  
Each record includes:
- match_id
- home_team, away_team
- home_score, away_score
- date, last_updated

---

## How to Run
1. Open `etl_extract.ipynb` in Jupyter Notebook or VS Code  
2. Run the cells step-by-step:
   - Section 1: Full Extraction  
   - Section 2: Incremental Extraction  
   - Section 3: Save Timestamp  
   - Section 4: Transform Full Data  
   - Section 5: Transform Incremental Data

Note: `last_extraction.txt` stores the last extraction time for incremental updates.

---

## Outputs

### Extraction
- Full Extraction: Loads entire dataset  
- Incremental Extraction: Loads only records updated since last run

### Transformation
Applies 3 transformations:
1. Cleaning – Removes duplicates  
2. Structural – Converts `date` and `last_updated` to datetime  
3. Enrichment – Adds `goal_diff = home_score - away_score`

---

## Resulting Files
- transformed_full.csv – Cleaned and enriched full dataset  
- transformed_incremental.csv – Cleaned and enriched incremental data  

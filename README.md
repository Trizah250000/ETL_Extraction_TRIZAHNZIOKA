
# ETL Extract Lab

**Name**: Trizah Nzioka

## Description
This lab demonstrates Full and Incremental Extraction using a synthetic football matches dataset.

## Tools Used
- Python
- Pandas
- Jupyter Notebook

## Dataset
A generated dataset of 60 days of football matches including:
- match_id, home_team, away_team, scores, date, last_updated

## How to Run
1. Open `etl_extract.ipynb` in Jupyter
2. Run each cell step-by-step
3. Incremental extraction uses `last_extraction.txt` to track last updates

## Outputs
- Full extraction: pulls all match records
- Incremental: pulls only matches updated since last timestamp

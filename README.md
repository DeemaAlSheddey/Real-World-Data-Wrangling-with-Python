# Real World Data Wrangling — IMDb & Netflix Movies 🎬

Udacity Data Analyst project. I gathered, assessed, cleaned, and analyzed IMDb and Netflix datasets to explore whether Netflix includes the most popular and top-rated movies from IMDb.

## What I Did
1) Gathered data from two different sources (manual download + Kaggle API).  
2) Assessed data for quality and tidiness issues.  
3) Cleaned, merged, and stored both raw and cleaned datasets.  
4) Analyzed the overlap between IMDb’s top movies and Netflix’s catalog.

## Dataset
- **IMDb Top Rated Movies:** `results_with_crew.csv` (manually downloaded from Kaggle)  
- **Netflix Titles:** `netflix_titles.csv` (programmatically downloaded using Kaggle API)  
- Combined cleaned dataset: `merged_df1_2025-10-04.csv`

## Steps (Very Short)
- Removed missing values in `writers` column.  
- Converted `date_added` in Netflix data to datetime.  
- Split multiple genres into separate rows (`explode`).  
- Separated `duration` column into `duration_value` and `duration_unit`.  
- Merged datasets on cleaned lowercase movie titles (`title_clean`).  
- Saved both raw and cleaned data versions under `date_store/`.

## Results (Quick)
- Only **826 out of 4,883 IMDb top movies** are available on Netflix — showing a limited overlap.  
- The **top 3 genres** among top-rated movies on Netflix are:  
  - 🎭 **Drama** (55%)  
  - 😂 **Comedy** (24.5%)  
  - 🔪 **Crime** (20.5%)

## How to Run
```bash
pip install pandas numpy matplotlib seaborn
jupyter notebook Data_Wrangling_Project_Starter.ipynb
# or export:
python -m nbconvert --to html Data_Wrangling_Project_Starter.ipynb

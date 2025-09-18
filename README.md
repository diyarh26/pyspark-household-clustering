# Household Clustering and Viewing Analysis with PySpark (Distributed Database Management)

This project applies **PySpark** to demographic and TV viewership data, analyzing household clusters and their content preferences.  
It was developed as part of the **Distributed Database Management** course (096224) at Technion.

## Part 1 — Static Data Analysis
- **Feature Extraction:** normalized numerical features and one-hot encoded categorical attributes.  
- **PCA Projection:** reduced features to 2D and visualized clusters with a scatter plot.  
- **K-means Clustering:** assigned each household to a cluster (seed=3).  
- **Subset Creation:**  
  - Full (all households)  
  - 3rds (every 3rd household by distance to centroid)  
  - 17ths (every 17th household)  
- **Viewing Analysis:** computed station popularity vs. global population using `diff rank`.  
- Reported **top 7 stations** per subset, enabling comparison across clusters and subset types.  

## Part 2 — Dynamic Data Analysis (Streaming)
- Used **Spark Streaming** to process live viewing events from **Kafka**.  
- Repeated subset viewing analysis (3rds subset only).  
- Processed at least 3 streaming batches.  
- Produced incremental results per batch to capture evolving preferences.  
- Compared cluster behavior over time, checking for consistent station preferences.  

## Deliverables
- `project2.ipynb` — PySpark code and analysis  
- (optional) `project2.html` — HTML export of the notebook  
- (optional) `project2.pdf` — PDF export of the notebook  

## Tools
- PySpark 3+ (Databricks)  
- Spark Streaming + Kafka  
- Python 3.10  
- Libraries: `pyspark.sql`, `pyspark.ml`, `pandas`, `matplotlib`  

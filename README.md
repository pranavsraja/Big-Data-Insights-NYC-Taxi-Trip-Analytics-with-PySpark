# Big Data Insights: NYC Taxi Trip Analytics with PySpark

This repository contains the notebook of **"NYC Taxi Trip Profitability and Zone Analysis"**, implemented using Apache Spark in Python.

---

## Project Overview

This notebook analyses NYC taxi trip records using the PySpark framework and focuses on:

- Cleaning raw trip data
- Enhancing it with profitability metrics
- Summarizing by zones
- Ranking zones based on several performance indicators
- Recording execution times for performance evaluation

---

## Dataset Details

### 1. NYC Taxi Trips Dataset  
A record of thousands of taxi trips, each including:
- Trip distance
- Passenger count
- Pickup/drop-off zones
- Total trip cost

### 2. NYC Zones Dataset  
A mapping of zone IDs to human-readable location names used to enrich trip data.

---

## Tasks Implemented

### Task 0: Read Data
- Load trip and zone data using PySpark DataFrames
- Setup reusable helper functions like `init_trips()` and `pipeline()`

### Task 1: Data Cleaning
- Removed trips with:
  - Zero distance
  - No passengers
  - Outliers in cost and distance

### Task 2: Add New Columns
- Joined trip data with zone names
- Calculated **unit profitability** (cost per distance unit)

### Task 3: Zone Summarization & Ranking
- Aggregated trip data by origin/destination zones
- Generated **top 10 zone rankings** based on:
  - Total trip volume
  - Average profitability
  - Total passenger count

### Task 4: Execution Time Benchmarking
- Recorded end-to-end and task-specific processing times
- Compared dataset size and format efficiency (S to XXL)

---

## Technologies Used

- Apache Spark (PySpark)
- Google Colab for cloud execution
- Pandas (for brief output viewing)
- `time` and `collect()` for performance benchmarking

---

## Getting Started

### Environment Requirements

- Python 3.8+
- PySpark (installed in Colab or manually via `pip install pyspark`)

### Run the Notebook

1. Open in [Google Colab](https://colab.research.google.com/)  
2. Mount your Google Drive for access to datasets  
3. Follow the notebook cells sequentially  
4. Use the provided `pipeline()` function for full execution time benchmarking

---

## Repository Structure

```
NYC-Taxi-PySpark-Analysis
 ┣ nyc_taxi.ipynb
 ┗ README.md
```

---

## Highlights

- Fully modular functions for reusability
- Optimization for large datasets
- Practical use of UDFs and DataFrame API
- Execution time profiling to inform scalability strategies

---

## Author

- **Pranav Sunil Raja**  
- GitHub: [@pranavsraja](https://github.com/pranavsraja)

---

## License

This project is intended for academic and educational use only.
# Weather Data Pipeline with Apache Airflow (Part One)

## Introduction

This lab focuses on designing and implementing an ETL pipeline to automate the process of extracting, transforming, and storing weather data on daily basis. The pipeline uses Apache Airflow to orchestrate tasks and PostgreSQL for data storage, demonstrating best practices in data engineering workflows.

---

## Architecture

![Architecture Diagram](/architecture.png)

The architecture visualizes the flow of data from the weather API to PostgreSQL through Apache Airflow, emphasizing task automation and modularity.

---

## Tools and Technologies

- **Apache Airflow**: Task orchestration and pipeline scheduling.
- **PostgreSQL**: Data storage and management.
- **OpenWeather API**: Source of weather data.
- **Docker**: Environment setup for Apache Airflow.
- **Python**: Data transformation and scripting.

---

## Setup and Usage

1. **Install Dependencies**:

   - Install Docker and set up Apache Airflow.
   - Configure PostgreSQL as the backend database.

2. **Environment Configuration**:

   - Obtain an OpenWeather API key and update the DAG file.
   - Set up PostgreSQL connections in Airflow.

3. **Run the DAG**:
   - Start the Airflow scheduler and trigger the weather pipeline DAG.

---

## Directory Structure

```
part-one/
│
├── dags/
│   ├── weather_data_dag.py
│
```

---

![Dag](/part-one/screenshots/graph.png)

## Overview

The pipeline automates the following tasks:

- **Check API Readiness**: Ensure the weather API is accessible.
- **Extract Data**: Fetch weather details (temperature, humidity, etc.) for a specified city.
- **Transform Data**: Convert temperatures to Fahrenheit and adjust timestamps.
- **Load Data**: Store the transformed data into a PostgreSQL database table.

---

## Conclusion

This lab demonstrates an end-to-end automated data pipeline, enabling efficient data ingestion and transformation for weather analysis. The solution showcases key skills in ETL process design and Airflow orchestration.

---

# Power App (Part Two)

In the `part-two` directory, we have utilized a script named `script.py` to process the original `YellowTaxiData.csv` file. The purpose of this script was to reduce the number of rows in the dataset to 100 rows. This was necessary because the original file was too large to be sent as an attachment for testing the cloud flow.

## Process

1. **Original File**: `YellowTaxiData.csv` (not included in the repository)
2. **Script Used**: `script.py`
3. **Operation**: Reduced the rows to 100
4. **New File**: `YellowTaxiData.csv` (not included in the repository)

## Purpose

The reduced file size ensures that the dataset can be easily attached and sent for testing the cloud flow without any issues related to file size limitations.

## Directory Structure

```
part-two/
│
├── script.py
├── YellowTaxiData.csv (original, gitignored)
└── YellowTaxiData.csv (reduced to 100 rows, gitignored)
```

## Conclusion

By reducing the size of the `YellowTaxiData.csv` file, we have made it feasible to test the cloud flow effectively. The `script.py` in the `part-two` directory handles this reduction process efficiently. Note that the `.csv` files are gitignored and not included in the repository due to their size.

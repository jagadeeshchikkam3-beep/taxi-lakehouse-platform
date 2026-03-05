# TaxiLake — End-to-End Lakehouse Data Platform

TaxiLake is a production-style data lakehouse platform built to process and analyze large-scale NYC taxi trip data.

The platform demonstrates modern data engineering practices including distributed processing, medallion architecture (Bronze/Silver/Gold), orchestration, and scalable analytics pipelines.

This project simulates how real-world data platforms are designed using Spark, Delta Lake, and Airflow.

---

## Architecture

The platform follows a **Lakehouse Architecture** using the Medallion pattern.

Data flows through multiple layers:

Data Source → Ingestion → Bronze Layer → Silver Layer → Gold Layer → Analytics

**Bronze Layer**

Raw ingestion of taxi trip data without modifications.

**Silver Layer**

Cleaned and standardized datasets after applying transformations.

**Gold Layer**

Business-ready aggregated datasets used for analytics and reporting.

---

## Tech Stack

| Layer          | Technology      |
| -------------- | --------------- |
| Processing     | Apache Spark    |
| Storage        | Delta Lake      |
| Orchestration  | Apache Airflow  |
| Infrastructure | Docker          |
| Language       | Python          |
| Data Format    | Parquet / Delta |

---

## Data Pipeline

1. Raw taxi trip data is ingested into the platform.
2. Data is stored in the **Bronze Layer** without modification.
3. Spark transformations clean and normalize the data into the **Silver Layer**.
4. Aggregated analytics tables are created in the **Gold Layer**.
5. These tables power analytical queries and dashboards.

---

## Project Structure

taxi-lakehouse-platform/

airflow/
    dags/

spark_jobs/
    ingestion/
    transformations/
    aggregations/

configs/

data_lake/
    bronze/
    silver/
    gold/

docker/

---

## Project Roadmap
- [ ] Week 1 — Architecture design and environment setup  
- [ ] Week 2 — Batch ingestion pipeline and Bronze layer  
- [ ] Week 3 — Data transformations and Silver layer  
- [ ] Week 4 — Gold layer analytics, optimization, and monitoring
---

## Dataset

This project uses the NYC Taxi Trip dataset which contains detailed information about taxi rides including pickup times, trip distances, fares, and payment types.

The dataset allows simulation of large-scale data engineering pipelines.

---

## Future Enhancements

* Real-time streaming pipeline using Kafka
* Data quality validation framework
* Monitoring and observability dashboards
* Performance optimization experiments

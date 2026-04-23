# Real-Time Streaming Data Platform with ML Anomaly Detection

## Overview
This project demonstrates a real-time data engineering pipeline that processes streaming data using Kafka and Spark, applies machine learning for anomaly detection, and ensures data quality for analytics.

## Architecture
Kafka → Spark Streaming → ML Model → Data Storage → Analytics

## Tech Stack
- Python, PySpark
- Kafka
- AWS (S3, Glue, Athena)
- Airflow
- Scikit-learn

## Features
- Real-time streaming pipeline
- ML-based anomaly detection
- Data validation checks
- Scalable architecture

## How to Run
```bash
python streaming/kafka_producer.py
spark-submit streaming/spark_streaming.py
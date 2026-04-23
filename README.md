# Real-Time Streaming Data Platform with ML Anomaly Detection

## Overview

This project is a real-time data pipeline built to simulate how modern systems process and analyze streaming data. The idea was to take a continuous flow of events (like transactions), process them in real time, and detect unusual patterns using machine learning.

Instead of just building a batch ETL pipeline, I wanted to focus on a system that handles data as it arrives — closer to how real production systems work.


## Why I built this

In most real-world systems, especially in finance and large-scale applications, data is generated continuously. Detecting issues or anomalies after hours or days isn’t useful — it needs to happen in real time.

This project is an attempt to bring together streaming, distributed processing, and basic ML to solve that kind of problem.


## What the system does

* Generates streaming data (simulating transactions)
* Sends data through Kafka for real-time ingestion
* Processes the stream using Spark Structured Streaming
* Applies a simple ML model (Isolation Forest) to detect anomalies
* Performs basic data validation checks
* Stores processed data for downstream analysis


## Tech Stack

* Python
* Kafka
* Spark (Structured Streaming)
* Scikit-learn (for anomaly detection)
* Airflow (for orchestration)
* AWS concepts (S3 / Glue / Athena – design-ready)

## Project Structure

```
real-time-ml-data-platform/
│
├── streaming/        # Kafka producer + Spark streaming job  
├── ml/               # Anomaly detection logic  
├── dags/             # Airflow DAG  
├── data_quality/     # Data validation checks  
├── infrastructure/   # Placeholder for infra (Terraform in future)  
├── dashboards/       # Architecture diagram & outputs  
```

## How to run

Start the Kafka producer:

```bash
python streaming/kafka_producer.py
```

Run the Spark streaming job:

```bash
spark-submit streaming/spark_streaming.py
```

## What I focused on

* Keeping the pipeline simple but realistic
* Structuring the project like a real system (not just scripts)
* Combining streaming + ML in a practical way
* Making it extensible for cloud deployment


## What can be improved

* Deploy the full pipeline on AWS (S3, Glue, Athena)
* Add a dashboard for real-time monitoring
* Introduce alerting (SNS / Slack)
* Containerize the system using Docker
* Improve the ML model with more features and tuning


## Final thoughts

This project helped me understand how different components in a real-time data system fit together — especially the interaction between streaming pipelines and ML models. It’s not meant to be perfect, but a solid foundation that can be extended into a production-grade system.

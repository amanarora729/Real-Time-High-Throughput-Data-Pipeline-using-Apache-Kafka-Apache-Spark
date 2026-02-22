# 🚀 High-Throughput Kafka & Spark Real-Time Data Pipeline

This project demonstrates an **end-to-end high-performance data engineering pipeline** capable of processing **1.2+ billion records per hour** using Apache Kafka and Apache Spark.

It simulates large-scale financial transaction streams and performs real-time aggregations using distributed streaming technologies.

---

## 🏗️ Architecture Overview

- **Kafka Producer** generates high-volume financial transaction events using multi-threading.
- **Apache Kafka Cluster** (multi-broker, partitioned topics) handles distributed ingestion.
- **Apache Spark Structured Streaming** consumes Kafka data and performs real-time aggregations.
- **Kafka Sink Topics** store aggregated metrics for downstream consumers.
- **Checkpointing & State Store** ensure fault tolerance and exactly-once semantics.
- **Docker Compose** orchestrates the entire distributed setup.

---

## ⚙️ Tech Stack

- Apache Kafka (Multi-Broker Setup)
- Apache Spark 3.5 (Structured Streaming)
- Python (Kafka Producer & Spark Jobs)
- Docker & Docker Compose

---

## 📊 Key Features

- 🚀 Handles **1.2B+ events/hour** throughput
- 🔁 Multi-threaded Kafka producers with batching & compression
- 📈 Real-time merchant-level aggregations
- 💾 Stateful streaming with checkpointing & recovery
- 🐳 Fully containerized distributed architecture

---

## 🧪 Data Flow

1. Kafka Producer generates financial transaction events
2. Events are published to Kafka topics with multiple partitions
3. Spark Structured Streaming reads data from Kafka
4. Real-time aggregations are computed per merchant
5. Aggregated results are written back to Kafka topics

---

## ▶️ How to Run

```bash
docker compose up -d
spark-submit spark_processor.py
python main.py

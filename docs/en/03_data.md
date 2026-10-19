# 🗄️ 3. Data Engineering for ML

> Russian version: [03_data.md](../ru/03_data.md)

> In real work an ML engineer spends half the time on data, not models. If you come from DE, you already have a head start. If not, don't skip this one: below is what you **must** be able to do.

---

## 🔍 SQL (Advanced)

- [ ] JOINs (INNER, LEFT, FULL, CROSS, SEMI, ANTI)
- [ ] Window functions: `ROW_NUMBER`, `LAG/LEAD`, `SUM() OVER`
- [ ] CTEs, recursive CTEs
- [ ] Subqueries, EXISTS vs IN
- [ ] Indexes, EXPLAIN, optimization
- [ ] Partitioning, sharding
- [ ] PostgreSQL, ClickHouse (de facto standard in Russia: Yandex Metrica, VK, Avito)

📚 **Resources:**
- [Stepik — Introduction to SQL](https://stepik.org/course/63054)
- [SQL-EX](https://sql-ex.ru/) — exercises
- [DataLemur](https://datalemur.com/) — interview-style tasks
- [ClickHouse documentation](https://clickhouse.com/docs/ru)

---

## 🐼 Pandas / Polars / NumPy

- [ ] NumPy: vectorization, broadcasting, fancy indexing
- [ ] Pandas: groupby, merge, pivot, apply vs vectorize
- [ ] Memory optimization (`category`, `int8`)
- [ ] **Polars** — modern Pandas alternative: faster, lazy execution plan
- [ ] **DuckDB** — SQL over Parquet/CSV right in a notebook, no server
- [ ] EDA: dataset profiling, anomaly search

---

## 🚀 Big Data Stack

- [ ] **Apache Spark** (PySpark) — main tool in Russian Tier-1 companies
  - DataFrame API, Spark SQL
  - Partitioning, broadcast join
  - UDF, Pandas UDF
- [ ] **Hadoop / HDFS** — overview
- [ ] **Hive / Trino / Presto** — SQL over big data

---

## 🌬️ Orchestration and Pipelines

- [ ] **Apache Airflow** — gold standard in Russia
  - DAG, operators, sensors, TaskFlow API
  - XCom, branching, dynamic DAGs
- [ ] **dbt** — transformations in DWH
- [ ] Alternatives: Prefect, Dagster

---

## 📨 Streaming

- [ ] **Apache Kafka** (producers/consumers, topics, partitions)
- [ ] Spark Streaming / Flink (overview)
- [ ] Use case: online features for ML, real-time inference

---

## 🏪 Data Storages

| Type | Technologies | Where you will see it |
|---|---|---|
| OLTP | PostgreSQL, MySQL | Any backend |
| OLAP | ClickHouse, Greenplum | Yandex, Avito, X5 |
| DWH | Snowflake, BigQuery (less common in Russia) | — |
| Data Lake | S3 / HDFS + Parquet/Iceberg | Sber, T-Bank |
| Vector DB | Qdrant, Milvus, Weaviate, pgvector | LLM/RAG |
| Feature Store | Feast, in-house solutions | Yandex, Sber |

---

## ✅ Checkpoint project

An ETL pipeline in Airflow:
1. Pulls data from a public API, for example hh.ru vacancies.
2. Cleans/enriches it in PySpark.
3. Loads it into PostgreSQL and ClickHouse.
4. Builds a data mart for a dashboard (Superset/Metabase).
5. Deploys through `docker-compose`.

---

<!-- nav -->
← Back: [📐 2. Math for ML](02_math.md) · [Contents](../../README.md) · Next: [🤖 4. Classical ML](04_classical_ml.md) →

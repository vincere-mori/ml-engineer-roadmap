# 🗄️ 3. Data Engineering для ML

> English version: [03_data.md](../en/03_data.md)

> У тебя уже есть база DE — это огромный плюс. ML Engineer без DE-навыков сильно ограничен в реальных задачах. Здесь — что **обязательно** надо подтянуть/закрепить.

---

## 🔍 SQL (Advanced)

- [ ] JOIN'ы (INNER, LEFT, FULL, CROSS, SEMI, ANTI)
- [ ] Оконные функции: `ROW_NUMBER`, `LAG/LEAD`, `SUM() OVER`
- [ ] CTE, рекурсивные CTE
- [ ] Подзапросы, EXISTS vs IN
- [ ] Индексы, EXPLAIN, оптимизация
- [ ] Партицирование, шардирование
- [ ] PostgreSQL, ClickHouse (де-факто стандарт в РФ — Яндекс.Метрика, VK, Avito)

📚 **Ресурсы:**
- [Stepik — Введение в SQL](https://stepik.org/course/63054)
- [SQL-EX](https://sql-ex.ru/) — задачи
- [DataLemur](https://datalemur.com/) — задачи с собесов
- [ClickHouse документация](https://clickhouse.com/docs/ru)

---

## 🐼 Pandas / Polars / NumPy

- [ ] NumPy: vectorization, broadcasting, fancy indexing
- [ ] Pandas: groupby, merge, pivot, apply vs vectorize
- [ ] Оптимизация по памяти (`category`, `int8`)
- [ ] **Polars** — современная замена Pandas (быстрее, ленивый план)
- [ ] **DuckDB** — SQL по Parquet/CSV прямо в ноутбуке, без сервера
- [ ] EDA: построение профиля датасета, поиск аномалий

---

## 🚀 Big Data Stack

- [ ] **Apache Spark** (PySpark) — основной инструмент в Tier-1 РФ
  - DataFrame API, Spark SQL
  - Партицирование, broadcast join
  - UDF, Pandas UDF
- [ ] **Hadoop / HDFS** — обзорно
- [ ] **Hive / Trino / Presto** — SQL поверх big data

---

## 🌬️ Оркестрация и пайплайны

- [ ] **Apache Airflow** — золотой стандарт в РФ
  - DAG, операторы, sensors, TaskFlow API
  - XCom, branching, dynamic DAGs
- [ ] **dbt** — трансформации в DWH
- [ ] Альтернативы: Prefect, Dagster

---

## 📨 Стриминг

- [ ] **Apache Kafka** (продьюсеры/консьюмеры, топики, партиции)
- [ ] Spark Streaming / Flink (обзорно)
- [ ] Use case: онлайн-фичи для ML, real-time inference

---

## 🏪 Хранилища данных

| Тип | Технологии | Где встретишь |
|---|---|---|
| OLTP | PostgreSQL, MySQL | Любые backend |
| OLAP | ClickHouse, Greenplum | Yandex, Avito, X5 |
| DWH | Snowflake, BigQuery (реже в РФ) | — |
| Data Lake | S3 / HDFS + Parquet/Iceberg | Sber, T-Bank |
| Vector DB | Qdrant, Milvus, Weaviate, pgvector | LLM/RAG |
| Feature Store | Feast, собственные решения | Yandex, Sber |

---

## ✅ Контрольный проект

ETL-пайплайн на Airflow:
1. Тянет данные из публичного API (например, hh.ru вакансии).
2. Чистит/обогащает в PySpark.
3. Грузит в PostgreSQL и ClickHouse.
4. Делает витрину для дашборда (Superset/Metabase).
5. Деплой через `docker-compose`.

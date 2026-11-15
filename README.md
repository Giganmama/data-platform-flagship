# Data Platform Flagship

Production-grade data platform consolidating multiple data engineering patterns.

## Architecture

Sources (Postgres legacy)
-> Debezium CDC -> Kafka
-> Spark Structured Streaming (Scala)
-> Delta Lake (Bronze/Silver/Gold)
-> ClickHouse (витрины)
-> Airflow (оркестрация) + Great Expectations (DQ)

## Modules

- `ingestion/` - Kafka producers/consumers (Scala)
- `streaming/` - Spark Structured Streaming jobs
- `lakehouse/` - Delta Lake medallion architecture
- `warehouse/` - ClickHouse + Greenplum
- `features/` - Feature store
- `migration-lab/` - CDC migration with dual run & reconciliation
- `orchestration/` - Airflow DAGs
- `dq/` - Great Expectations data quality

## Quick Start

```bash
# TODO: добавить docker-compose up и инструкции
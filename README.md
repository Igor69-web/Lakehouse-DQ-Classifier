# Metadata-driven Data Quality & Error Classification Engine for Lakehouse Architectures (Trino, Iceberg, ClickHouse)

## Ключевые слои и стек:
* **Source Layer:** `PostgreSQL` (транзакционная БД источника).
* **Storage & Compute Layer (Silver):** `MinIO` (S3) + Apache Iceberg + Trino (распределенный SQL-движок).
* **Serving / Gold Layer:** `ClickHouse` (аналитическая СУБД для витрин).
* **Control & Metadata Layer:** `Python Core` + `PostgreSQL` (Репозиторий метаданных SCD Type 2 + Lineage).
* **Observability:** `Grafana` (мониторинг метрик DQ и инцидентов).

## Deployment 
Развертывание системы происходит на Windows с использованием `Docker Desktop + WSL2` и ОЗУ на `10 ГБ`. 

### Предварительные требования
* `Docker Desktop` + `WSL2` (для Windows) или Linux/macOS
* `Docker Compose v2.x+`
* `Python 3.10+`

### Схема системы
<img width="956" height="1073" alt="ShemaDWH" src="https://github.com/user-attachments/assets/894ebc90-e168-4656-ae0c-d032349e7f36" />

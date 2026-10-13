### Hi, I'm Basant Bhattarai

Senior Data & AI Engineer in Kathmandu, working US and EU hours. Nine years building systems that have to keep working: data platforms, the databases under them, and AI systems that write into them — and the architecture that keeps all three recoverable.

- **Data platforms.** Kafka and Kinesis ingestion, Spark processing, Airflow and dbt, an Iceberg lakehouse, Trino and ClickHouse serving. A 15 TB+ production footprint, 100M+ events a day, 99.9% uptime.
- **AI systems on production data.** LangGraph, Google ADK and MCP agents whose output is typed, traced, evaluated and reviewable before it becomes state. Analytics delivery 60% faster.
- **Databases that survive failure.** PostgreSQL and distributed Postgres, HA, backup and point-in-time recovery, version upgrades — measured on rigs I publish, not quoted from a vendor page.

**Open source**

- [spark-sql-kinesis](https://github.com/technobasant/spark-sql-kinesis) [![Maven Central](https://img.shields.io/maven-central/v/io.github.technobasant/spark-sql-kinesis_2.13?label=maven%20central)](https://central.sonatype.com/artifact/io.github.technobasant/spark-sql-kinesis_2.13) — Kinesis source and sink for Spark 4.2 Structured Streaming on AWS SDK v2. Upgrades in place: the checkpoint format is byte-identical, so no drain.
- [db-failover-lab](https://github.com/technobasant/db-failover-lab) — six database engines, eight failover scenarios, one laptop: measured HA, sharding and backup/restore for PostgreSQL 18, Redis, MongoDB, ScyllaDB, SolrCloud and Galera.
- [lakehouse-lab](https://github.com/technobasant/lakehouse-lab) — Iceberg on MinIO with Apache Polaris vending table-scoped credentials to Trino and StarRocks; dbt + Airflow medallion, compaction and rollback, every figure measured.
- [rag-pipeline](https://github.com/technobasant/rag-pipeline) — scrape-to-RAG lakehouse: Airflow, Spark bronze/silver/gold on Delta and MinIO, Chroma, a FastAPI answer service, OpenLineage.

**Recent writing** — measured, with the method stated

- [The Spark 4 upgrade that succeeded and wrote nothing](https://basantbhattarai.com.np/writing/spark-4-s3a-committer-wrote-nothing/)
- [Ten seconds per idle shard: why I maintain a Kinesis connector for Spark 4](https://basantbhattarai.com.np/writing/spark-4-kinesis-connector-idle-floor/)
- [Validate said SUCCESS. The upgrade would have died halfway.](https://basantbhattarai.com.np/writing/hive-metastore-4-upgrade-validate-said-success/)
- [The best OCR model I tested does not ship](https://basantbhattarai.com.np/writing/choosing-an-ocr-engine-for-clinic-records/)
- [The classifier was 95% accurate. The trend it counted was a third too flat.](https://basantbhattarai.com.np/writing/count-prevalence-not-classifications/)

**Stack**

Python · SQL · Scala · Spark · Kafka · Kinesis · Airflow · dbt · Iceberg · Trino · ClickHouse · PostgreSQL · Kubernetes · Terraform · AWS · LangGraph · Google ADK · MCP

[basantbhattarai.com.np](https://basantbhattarai.com.np) · [LinkedIn](https://www.linkedin.com/in/technobasant) · contact@basantbhattarai.com.np

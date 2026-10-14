### Hi, I'm Basant Bhattarai

Senior Data & AI Engineer in Kathmandu, working US and EU hours. Nine years building systems that have to keep working: data platforms, the databases under them, and AI systems that write into them — and the architecture that keeps all three recoverable.

- **Data platforms.** Kafka and Kinesis ingestion, Spark processing, Airflow and dbt, an Iceberg lakehouse, Trino and ClickHouse serving. A 15 TB+ production footprint, 100M+ events a day, 99.9% uptime.
- **AI systems on production data.** LangGraph, Google ADK and MCP agents whose output is typed, traced, evaluated and reviewable before it becomes state. Analytics delivery 60% faster.
- **Databases that survive failure.** PostgreSQL and distributed Postgres, HA, backup and point-in-time recovery, version upgrades — measured on rigs I publish, not quoted from a vendor page.

**Open source**

- [governed-agent](https://github.com/technobasant/governed-agent) — an AI agent whose output becomes state only after a schema, a policy, a grounding check and, where required, a person: LangGraph + MCP, FastAPI with a PostgreSQL outbox, a Next.js review UI, measured on qwen3:8b.
- [platform-deployments](https://github.com/technobasant/platform-deployments) — GitOps for governed-agent on a three-node Kubernetes cluster: Argo CD, an Argo Rollouts canary that aborted a bad release on its own in 6 of 6 runs, CloudNativePG, Kyverno and OpenTelemetry, plus Terraform for EKS.
- [evalproof](https://github.com/technobasant/evalproof) — LLM evaluation as measurement: calibrate the judge against a gold sample, correct its pass rate (ACC/PPI), and gate CI only on significant regressions. Local-first with Ollama; ships as a GitHub Action.
- [spark-sql-kinesis](https://github.com/technobasant/spark-sql-kinesis) [![Maven Central](https://img.shields.io/maven-central/v/io.github.technobasant/spark-sql-kinesis_2.13?label=maven%20central)](https://central.sonatype.com/artifact/io.github.technobasant/spark-sql-kinesis_2.13) — Kinesis source and sink for Spark 4.2 Structured Streaming on AWS SDK v2. Upgrades in place: the checkpoint format is byte-identical, so no drain.
- [realtime-ml](https://github.com/technobasant/realtime-ml) — real-time fraud scoring where leakage, training/serving skew and label delay are measured: Feast, LightGBM, MLflow, shadow serving, drift alerts and a paired-statistics promotion gate.
- [dataset-registry](https://github.com/technobasant/dataset-registry) — ownership before consumption, as a product: owners, freshness SLOs, versioned JSON Schema contracts, OpenLineage lineage, and breaking changes that wait for consumer acknowledgement. Go, PostgreSQL, Next.js.
- [streaming-platform](https://github.com/technobasant/streaming-platform) — Kafka, Flink, ClickHouse and Iceberg with Avro contracts and a freshness SLO; every event counted at every layer, exactly-once through broker kills, TaskManager kills and stalls.
- [retrieval-bench](https://github.com/technobasant/retrieval-bench) — pgvector, Qdrant and OpenSearch on the same embeddings: recall–latency curves, filtered-search recall collapse and its fixes, build cost, writes under load, and hybrid vs vector nDCG on public BEIR data.
- [distributed-db-lab](https://github.com/technobasant/distributed-db-lab) — Postgres scale-out with Citus (migration planner, online rebalance under load with zero errors, tenant isolation), TimescaleDB at scale, and a 2×2 replicated ClickHouse cluster; every failure measured.
- [db-failover-lab](https://github.com/technobasant/db-failover-lab) — six database engines, eight failover scenarios on real multi-node clusters: measured HA, sharding and backup/restore for PostgreSQL 18, Redis, MongoDB, ScyllaDB, SolrCloud and Galera.
- [lakehouse-lab](https://github.com/technobasant/lakehouse-lab) — Iceberg on MinIO with Apache Polaris vending table-scoped credentials to Trino and StarRocks; dbt + Airflow medallion, compaction and rollback, every figure measured.
- [postgres-ha-lab](https://github.com/technobasant/postgres-ha-lab) — Patroni + etcd on amd64 Rocky 8 under QEMU and pgBackRest over mutual TLS: failover, replica rebuild and point-in-time restore actually performed.
- [short-text-triage](https://github.com/technobasant/short-text-triage) — label the string, not the row: multilingual embeddings, HDBSCAN and margin-banded assignment on a seeded corpus; CI re-checks the figures.
- [prevalence-shift](https://github.com/technobasant/prevalence-shift) — why counting predicted labels flattens a trend, and how ACC, SLD and prediction-powered inference fix it; CI re-runs all 1,000 replications.
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

### Hi, I'm Basant Bhattarai

Senior Data & AI Engineer in Kathmandu, working US and EU hours. Nine years building systems that have to keep working: data platforms, the databases under them, and AI systems that write into them — and the architecture that keeps all three recoverable.

- **Data platforms.** Kafka and Kinesis ingestion, Spark processing, Airflow and dbt, an Iceberg lakehouse, Trino and ClickHouse serving. A 15 TB+ production footprint, 100M+ events a day, 99.9% uptime.
- **AI systems on production data.** LangGraph, Google ADK and MCP agents whose output is typed, traced, evaluated and reviewable before it becomes state. Analytics delivery 60% faster.
- **Databases that survive failure.** PostgreSQL and distributed Postgres, HA, backup and point-in-time recovery, version upgrades — measured on rigs I publish, not quoted from a vendor page.

**Open source** — each with its method and measurements in the repository; case studies, grouped the same way, at [basantbhattarai.com.np/work](https://basantbhattarai.com.np/work/)

*Data platforms*

- [streaming-platform](https://github.com/technobasant/streaming-platform) — Kafka, Flink, ClickHouse and Iceberg with Avro contracts and a freshness SLO; every event counted at every layer, exactly-once through broker kills, TaskManager kills and stalls. · [case study](https://basantbhattarai.com.np/work/streaming-platform/)
- [spark-sql-kinesis](https://github.com/technobasant/spark-sql-kinesis) [![Maven Central](https://img.shields.io/maven-central/v/io.github.technobasant/spark-sql-kinesis_2.13?label=maven%20central)](https://central.sonatype.com/artifact/io.github.technobasant/spark-sql-kinesis_2.13) — Kinesis source and sink for Spark 4.2 Structured Streaming on AWS SDK v2. Upgrades in place: the checkpoint format is byte-identical, so no drain. · [case study](https://basantbhattarai.com.np/work/spark-sql-kinesis/)
- [dataset-registry](https://github.com/technobasant/dataset-registry) — ownership before consumption, as a product: owners, freshness SLOs, versioned JSON Schema contracts, OpenLineage lineage, and breaking changes that wait for consumer acknowledgement. Go, PostgreSQL, Next.js. · [case study](https://basantbhattarai.com.np/work/dataset-registry/)
- [lakehouse-lab](https://github.com/technobasant/lakehouse-lab) — Iceberg on MinIO with Apache Polaris vending table-scoped credentials to Trino and StarRocks; dbt + Airflow medallion, compaction and rollback, every figure measured. · [case study](https://basantbhattarai.com.np/work/lakehouse-rag-lab/)
- [rag-pipeline](https://github.com/technobasant/rag-pipeline) — scrape-to-RAG lakehouse: Airflow, Spark bronze/silver/gold on Delta and MinIO, Chroma, a FastAPI answer service, OpenLineage.

*AI systems*

- [governed-agent](https://github.com/technobasant/governed-agent) — an AI agent whose output becomes state only after a schema, a policy, a grounding check and, where required, a person: LangGraph + MCP, FastAPI with a PostgreSQL outbox, a Next.js review UI, measured on qwen3:8b. · [case study](https://basantbhattarai.com.np/work/governed-agent/)
- [evalproof](https://github.com/technobasant/evalproof) — LLM evaluation as measurement: calibrate the judge against a gold sample, correct its pass rate (ACC/PPI), and gate CI only on significant regressions. Local-first with Ollama; ships as a GitHub Action. · [case study](https://basantbhattarai.com.np/work/evalproof/) · [live app](https://evalproof.streamlit.app)
- [realtime-ml](https://github.com/technobasant/realtime-ml) — real-time fraud scoring where leakage, training/serving skew and label delay are measured: Feast, LightGBM, MLflow, shadow serving, drift alerts and a paired-statistics promotion gate. · [case study](https://basantbhattarai.com.np/work/realtime-ml/)
- [retrieval-bench](https://github.com/technobasant/retrieval-bench) — pgvector, Qdrant and OpenSearch on the same embeddings: recall–latency curves, filtered-search recall collapse and its fixes, build cost, writes under load, and hybrid vs vector nDCG on public BEIR data. · [case study](https://basantbhattarai.com.np/work/retrieval-bench/)
- [short-text-triage](https://github.com/technobasant/short-text-triage) — label the string, not the row: multilingual embeddings, HDBSCAN and margin-banded assignment on a seeded corpus; CI re-checks the figures. · [case study](https://basantbhattarai.com.np/work/consulting-short-text-and-alerting/)
- [prevalence-shift](https://github.com/technobasant/prevalence-shift) — why counting predicted labels flattens a trend, and how ACC, SLD and prediction-powered inference fix it; CI re-runs all 1,000 replications. · [case study](https://basantbhattarai.com.np/work/consulting-short-text-and-alerting/) · [live app](https://prevalence-shift.streamlit.app)

*Databases and distributed systems*

- [distributed-db-lab](https://github.com/technobasant/distributed-db-lab) — Postgres scale-out with Citus (migration planner, online rebalance under load with zero errors, tenant isolation), TimescaleDB at scale, and a 2×2 replicated ClickHouse cluster; every failure measured. · [case study](https://basantbhattarai.com.np/work/distributed-db-lab/)
- [db-failover-lab](https://github.com/technobasant/db-failover-lab) — six database engines, eight failover scenarios on real multi-node clusters: measured HA, sharding and backup/restore for PostgreSQL 18, Redis, MongoDB, ScyllaDB, SolrCloud and Galera. · [case study](https://basantbhattarai.com.np/work/multi-engine-ha-lab/)
- [postgres-ha-lab](https://github.com/technobasant/postgres-ha-lab) — Patroni + etcd on amd64 Rocky 8 under QEMU and pgBackRest over mutual TLS: failover, replica rebuild and point-in-time restore actually performed. · [case study](https://basantbhattarai.com.np/work/patroni-ha-backup-lab/)

*Delivery and infrastructure*

- [platform-deployments](https://github.com/technobasant/platform-deployments) — GitOps for governed-agent on a three-node Kubernetes cluster: Argo CD, an Argo Rollouts canary that aborted a bad release on its own in 6 of 6 runs, CloudNativePG, Kyverno and OpenTelemetry, plus Terraform for EKS. · [case study](https://basantbhattarai.com.np/work/platform-deployments/)
*Upstream*

- [awslabs/spark-sql-kinesis-connector#99](https://github.com/awslabs/spark-sql-kinesis-connector/pull/99) — an opt-in option to stop reading a shard once it is caught up, requested in the project's issue #11 (in review).
- [citusdata/citus#7333](https://github.com/citusdata/citus/issues/7333) — a minimal reproduction on Citus 14.2 of node removal leaving cleanup records behind, with the code path; an earlier report of mine, [#4776](https://github.com/citusdata/citus/issues/4776), led to unnamed-constraint support on distributed tables.

**Recent writing** — measured, with the method stated; [all 36 pieces, grouped by subject](https://basantbhattarai.com.np/writing/)

- [The eval score fell 4.8 points. Twelve answers decided whether it meant anything.](https://basantbhattarai.com.np/writing/eval-score-drop-twelve-answers/)
- [The agent got 48 of 54 right. Three of the wrong ones published themselves.](https://basantbhattarai.com.np/writing/agent-measured-by-what-it-publishes/)
- [Validation picked the fraud model that had read the future](https://basantbhattarai.com.np/writing/realtime-ml-point-in-time-leakage/)
- [Exactly-once held through nine failures. The window counts did not.](https://basantbhattarai.com.np/writing/exactly-once-records-not-window-counts/)
- [Citus removed the node. Its cleanup records stayed behind.](https://basantbhattarai.com.np/writing/citus-remove-node-orphaned-cleanup-records/)
- [My canary analysis aborted a good release and promoted a bad one](https://basantbhattarai.com.np/writing/canary-analysis-aborted-good-promoted-bad/)
- [The Spark 4 upgrade that succeeded and wrote nothing](https://basantbhattarai.com.np/writing/spark-4-s3a-committer-wrote-nothing/)

**Stack**

Python · SQL · Go · TypeScript · Scala · Spark · Flink · Kafka · Kinesis · Airflow · dbt · Iceberg · Trino · ClickHouse · PostgreSQL · Citus · Kubernetes · Argo CD · Terraform · AWS · LangGraph · MCP · MLflow · Feast · Next.js

[basantbhattarai.com.np](https://basantbhattarai.com.np) · [LinkedIn](https://www.linkedin.com/in/technobasant) · contact@basantbhattarai.com.np

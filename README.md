### Hi, I'm Basant Bhattarai

Data & AI Architect · Senior Data Engineer in Kathmandu. I design data platforms, the governance around them and the AI on them, then build them: nine years in software, six on production data platforms.

- **Moving analytics off the product's Postgres.** Measure first, stop the damage, then scale out or migrate in stages with a way back. In production, two single-server Postgres databases, one of them a pgvector store, moved to Citus.
- **Platforms chosen on evidence and run at scale.** A proof of concept on criteria fixed in advance, then ingestion, lakehouse and serving that stay correct, recoverable and affordable: a 15 TB+ production footprint, 100M+ events a day, 99.9% uptime.
- **Governance an auditor can check.** Classification, masking, contracts and access review designed into the data model; SOC 2 controls for the platform and its infrastructure; erasure measured, not assumed.
- **AI on governed data.** LangGraph, Google ADK and MCP agents whose output is typed, evaluated and reviewable before it becomes state, with isolation enforced outside the model. Analytics delivery 60% faster.

**Start here** — two sample architecture engagements, published in full, for a fictional client measured on lab copies of its data

- [data-platform-architecture](https://github.com/technobasant/data-platform-architecture) — a SaaS company leaving Postgres: the current state measured on a copy of its database at its peak rate (reports on the primary took the product's p95 from 40 to 525 ms; on the replica 3 of 35 long reports finished), options priced in its EU region, a staged target, a data model across four domains, governance with SOC 2 readiness (a 21-control matrix), migration and 18 decisions with machine-checked evidence; keeping personal data in one table cut what erasing one person rewrote from 31.8 million event rows to 60,000. A proof of concept on Databricks: the smallest warehouse ran the reports in under 3 s, a day's work took 38 s and was billed for 11 minutes awake, and Terraform owned 6 of 7 kinds of governance object. · [case study](https://basantbhattarai.com.np/work/data-platform-architecture/)
- [ai-platform-architecture](https://github.com/technobasant/ai-platform-architecture) — the same client's usage assistant, text-to-SQL over governed data, measured on Qwen3, Llama 3.3, gpt-oss and Databricks Genie: told to stay in one customer's data, the models leaked on 23 of 120 requests; a default-deny query rewrite matched row-level security on every query they wrote and refuses 44 of 44 hand-written escapes; a semantic layer took Llama 3.3 70B from 55 to 70 of 70. · [case study](https://basantbhattarai.com.np/work/ai-platform-architecture/)
- [Choosing where the data lives](https://basantbhattarai.com.np/writing/choosing-where-the-data-lives/) — the decision guide behind them: RDS, Citus, TimescaleDB, ClickHouse, Trino, Iceberg and pgvector, by workload, with the measurements behind each rule.

**Production use cases** — case studies on the site; clients are not named, and their figures stay with them

*Data platforms*

- [Rebuilding a production data platform for scale and recovery](https://basantbhattarai.com.np/work/data-platform-practice/) — six years on one platform: faster processing, lower cost, safer change, and recovery designed before the incident.
- [An analytics lakehouse for a contact-centre platform](https://basantbhattarai.com.np/work/contact-centre-lakehouse/) — S3, Trino, Airflow and AWS Glue, delivered configured, with security, access control, HA and DR.

*Databases*

- [Two Postgres servers that ran out of room, moved to Citus](https://basantbhattarai.com.np/work/postgres-scale-out-citus/) — an application database and a pgvector store, scaled out with the data model doing most of the work.
- [Managed or self-run PostgreSQL](https://basantbhattarai.com.np/work/postgres-on-rds/) — a capacity plan and a fleet of RDS and Aurora databases, tuned and failover-tested; the same rule decided both.

*AI systems*

- [Turning model output into product state you can audit](https://basantbhattarai.com.np/work/governed-ai-delivery/) — a governed analytics workflow with typed state, provenance, evaluation, review and an honest fallback path.
- [Short-text classification and alerting for a lakehouse team](https://basantbhattarai.com.np/work/consulting-short-text-and-alerting/) — a classifier that failed in production, rebuilt around the unit of work, on Databricks.

**Open source** — each with its method and measurements in the repository; case studies, grouped the same way, at [basantbhattarai.com.np/work](https://basantbhattarai.com.np/work/)

*Data platforms*

- [streaming-platform](https://github.com/technobasant/streaming-platform) — Kafka, Flink, ClickHouse and Iceberg with Avro contracts and a freshness SLO; every event counted at every layer, exactly-once through broker kills, TaskManager kills and stalls. · [case study](https://basantbhattarai.com.np/work/streaming-platform/)
- [spark-sql-kinesis](https://github.com/technobasant/spark-sql-kinesis) [![Maven Central](https://img.shields.io/maven-central/v/io.github.technobasant/spark-sql-kinesis_2.13?label=maven%20central)](https://central.sonatype.com/artifact/io.github.technobasant/spark-sql-kinesis_2.13) — Kinesis source and sink for Spark 4.2 Structured Streaming on AWS SDK v2. Upgrades in place: the checkpoint format is byte-identical, so no drain. · [case study](https://basantbhattarai.com.np/work/spark-sql-kinesis/)
- [dataset-registry](https://github.com/technobasant/dataset-registry) — ownership before consumption, as a product: owners, freshness SLOs, versioned JSON Schema contracts, OpenLineage lineage, and breaking changes that wait for consumer acknowledgement. Go, PostgreSQL, Next.js. · [case study](https://basantbhattarai.com.np/work/dataset-registry/)
- [data-stack-lab](https://github.com/technobasant/data-stack-lab) — hands-on data engineering projects, one per tool, on one synthetic SaaS dataset, each checked in CI. dbt: a Type 2 dimension kept all 5,048 invoices on the plan they billed, where Type 1 moved 15.1% of revenue. Airflow 3: backfilled newest-first, high-water-mark loads lost 96.56% of a month with every run green. Data quality: nine injected defects; blocking let 0 of 3,198 bad rows through, and only control totals, volume and per-platform share saw the rows that never arrived. Spark: re-running one day with the default overwrite mode left 1 of 365 daily partitions. Databricks: a truncated file corrected under the same name was skipped by `COPY INTO` and Auto Loader, losing 1,638 events. · [case study](https://basantbhattarai.com.np/work/data-stack-lab/)
- [lakehouse-lab](https://github.com/technobasant/lakehouse-lab) — Iceberg on MinIO with Apache Polaris vending table-scoped credentials to Trino and StarRocks; dbt + Airflow medallion, compaction and rollback, every figure measured. · [case study](https://basantbhattarai.com.np/work/lakehouse-rag-lab/)
- [rag-pipeline](https://github.com/technobasant/rag-pipeline) — scrape-to-RAG lakehouse: Airflow, Spark bronze/silver/gold on Delta and MinIO, Chroma, a FastAPI answer service, OpenLineage.

*AI systems*

- [governed-agent](https://github.com/technobasant/governed-agent) — an AI agent whose output becomes state only after a schema, a policy, a grounding check and, where required, a person: LangGraph + MCP, FastAPI with a PostgreSQL outbox, a Next.js review UI, measured on qwen3:8b. · [case study](https://basantbhattarai.com.np/work/governed-agent/)
- [evalproof](https://github.com/technobasant/evalproof) — LLM evaluation as measurement: calibrate the judge against a gold sample, correct its pass rate (ACC/PPI), and gate CI only on significant regressions. Local-first with Ollama; ships as a GitHub Action. · [case study](https://basantbhattarai.com.np/work/evalproof/) · [live app](https://evalproof.streamlit.app) · `pip install evalproof`
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

**Recent writing** — measured, with the method stated; [all 50 pieces, grouped by subject](https://basantbhattarai.com.np/writing/)

- [RDS, Citus, TimescaleDB, ClickHouse, Trino, Iceberg or pgvector: choosing where the data lives](https://basantbhattarai.com.np/writing/choosing-where-the-data-lives/)
- [Erasing one person rewrote 31.8 million rows. With their e-mail in one table, 60,000.](https://basantbhattarai.com.np/writing/erasure-cost-is-a-modelling-decision/)
- [The day's work took 38 seconds. The warehouse was billed for 11 minutes.](https://basantbhattarai.com.np/writing/warehouse-billed-for-waiting-to-stop/)
- [We deleted the user from the Delta table. Time travel still returned all 100 rows.](https://basantbhattarai.com.np/writing/delta-delete-is-not-erasure/)
- [Told to stay in one customer's data, the models leaked 23 times in 120](https://basantbhattarai.com.np/writing/prompt-is-not-tenant-isolation/)
- [For text-to-SQL, the definitions mattered more than the model](https://basantbhattarai.com.np/writing/semantic-layer-mattered-more-than-the-model/)
- [The read replica was meant to take the reports. 3 of 35 finished.](https://basantbhattarai.com.np/writing/read-replica-cancelled-the-reports/)

**Stack**

Python · SQL · Go · TypeScript · Scala · Spark · Flink · Kafka · Kinesis · Airflow · dbt · Databricks · Unity Catalog · DuckDB · Iceberg · Trino · ClickHouse · PostgreSQL · Citus · pgvector · Kubernetes · Argo CD · Terraform · OpenTofu · AWS · LangGraph · MCP · MLflow · Feast · Next.js

[basantbhattarai.com.np](https://basantbhattarai.com.np) · [Résumé](https://basantbhattarai.com.np/resume/) · [Work with me](https://basantbhattarai.com.np/hire/) · [LinkedIn](https://www.linkedin.com/in/technobasant) · contact@basantbhattarai.com.np

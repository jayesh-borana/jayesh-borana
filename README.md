# Hi, I'm Jayesh 👋

**Lead, Analytics & Data Strategy** — building data platforms that drive business decisions.

- 🏢 Currently at Razor Group — owning P&L analytics for Amazon & Walmart, leading lakehouse migration (160 TB → Apache Iceberg)
- 🎓 IIM Bangalore (MBA) + IIT-BHU (B.Tech)
- 🌍 Based in Gurugram, India
- 📫 [LinkedIn](https://www.linkedin.com/in/jayeshb16/) · jayeshborana@outlook.com

### What I work with
`SQL` · `Python` · `PySpark` · `Redshift` · `Snowflake` · `Apache Iceberg` · `Airflow` · `AWS` · `dbt` · `Tableau` · `Claude API`

---

## Portfolio

A progressive reference of the patterns and systems I build in production, sanitized for public sharing.

### Data platform & modeling
- **[dbt-dimensional-modeling](https://github.com/jayesh-borana/dbt-dimensional-modeling)** — End-to-end Kimball dimensional model on dbt + DuckDB. Staging → intermediate → marts, SCD Type 2 snapshots, 33 tests.
- **[pnl-analytics-framework](https://github.com/jayesh-borana/pnl-analytics-framework)** — Multi-source P&L pipeline with fair-share allocation of marketing spend and platform fees. Full waterfall from gross revenue to CM3.
- **[lakehouse-migration-blueprint](https://github.com/jayesh-borana/lakehouse-migration-blueprint)** — Runnable Iceberg blueprints + migration playbook + operational runbook. 7 working demos via `pyiceberg` + DuckDB.

### Tooling & quality
- **[data-quality-engine](https://github.com/jayesh-borana/data-quality-engine)** — Lightweight Python framework: checks library, YAML suites, Slack reporter, CLI. 19 tests, Python 3.10–3.12 matrix.
- **[data-pipeline-ci-cd-blueprint](https://github.com/jayesh-borana/data-pipeline-ci-cd-blueprint)** — Reference CI/CD for data pipelines: lint → compile → test → data-diff → gated deploy + rollback playbook.
- **[sql-optimization-cookbook](https://github.com/jayesh-borana/sql-optimization-cookbook)** — 13 patterns across Redshift, Snowflake, Spark SQL. Real problems, real fixes, real production context.

### Operational pipelines
- **[sales-forecast-pipeline](https://github.com/jayesh-borana/sales-forecast-pipeline)** — Daily forecast-vs-actuals pipeline: DuckDB warehouse, QTD variance, matplotlib charts, Slack-ready alerts.

### AI / LLM
- **[ai-sql-assistant](https://github.com/jayesh-borana/ai-sql-assistant)** — Claude-powered SQL tooling (generate / explain / review) with full dbt schema awareness. Built on Claude Opus 4.7 with adaptive thinking + structured outputs.

---

### How these connect

Each project is independently useful, but they compose into a full analytics platform:

```
         ┌──────────────────────────────────┐
         │  data-pipeline-ci-cd-blueprint   │  ← PR checks, deploys, rollback
         └───────────────┬──────────────────┘
                         │ protects
                         ▼
   ┌─────────────────────────────────────────┐
   │  dbt-dimensional-modeling               │
   │  pnl-analytics-framework                │  ← the models
   └─────────────────────────────────────────┘
                         │ runs against
                         ▼
   ┌─────────────────────────────────────────┐
   │  lakehouse-migration-blueprint          │  ← storage + format layer
   └─────────────────────────────────────────┘
                         │ monitored by
                         ▼
   ┌─────────────────────────────────────────┐
   │  data-quality-engine                    │  ← DQ checks + alerts
   │  sales-forecast-pipeline                │  ← exec reporting
   └─────────────────────────────────────────┘

              augmented by
                         │
                         ▼
   ┌─────────────────────────────────────────┐
   │  ai-sql-assistant                       │  ← AI layer
   │  sql-optimization-cookbook              │  ← reference docs
   └─────────────────────────────────────────┘
```

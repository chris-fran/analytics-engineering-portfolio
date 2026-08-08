# analytics-engineering-portfolio

An analytics engineering portfolio project built on the [Olist Brazilian E-Commerce dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), using BigQuery, dbt, and Airflow (via Astro CLI).

## Project structure

- `ingestion/` — scripts for loading raw data into BigQuery
- `dbt_project/` — dbt models (staging → marts)
- `dags/` — Airflow DAGs orchestrating ingestion and dbt runs
- `docs/` — setup guides and other project documentation
- `raw_datasets/` — local copies of the source CSVs (see below)

## Data source

Raw data is the Olist Brazilian E-Commerce dataset from Kaggle. Download it locally with [kagglehub](https://pypi.org/project/kagglehub/):

```python
import kagglehub

# Download latest version
path = kagglehub.dataset_download("olistbr/brazilian-ecommerce")

print("Path to dataset files:", path)
```


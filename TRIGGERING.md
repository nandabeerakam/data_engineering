## Triggering the Pipeline Using Airflow

The execution of the PySpark pipeline is triggered using **Apache Airflow**.

### Triggering Steps
- An Airflow DAG is created with a scheduled interval (daily / weekly).
- The DAG uses `SparkSubmitOperator` to submit the PySpark job.
- Runtime parameters such as:
  - Input data path
  - Output location
  - Date filters  
  are passed dynamically to the Spark job.
- Airflow handles retries, logging, and failure notifications.
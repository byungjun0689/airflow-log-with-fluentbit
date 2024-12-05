# Airflow dags and system logging sample

## Build Airflow Docker 
```shell
docker build -t b-airflow:latest .
```

## Docker-compose
```shell
docker-compose up airflow-init
docker-compose up
```

## Test
### Running Dags (success_dag, error_dag)
- located : /opt/airflow/logs/dag
  ├── dag
  ├── error_dag
  │   └── 2024-12-5.log
  └── successful_dag
      └── 2024-12-5.log

### Running fluent-bit 
```shell
cd /opt/fluent-bit

./bin/fluent-bit -c airflow.conf
```

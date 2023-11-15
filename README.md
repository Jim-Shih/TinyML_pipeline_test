# TinyML

## TODOs
1. create a continuous data flow into postgresql
2. ~~create a dbt model for dbt transformation~~
3. create a spark job for batch processing
4. create a Jenkins job for continuous model verification and testing
5. create a airflow job for pipeline orchestration
   1. controls dbt transformation schedule
   2. controls spark batch processing schedule
6. find a way to monitor the data change and model performance also visualize them in grafana

## Components
1. grafana - time series data (demo use, metabase, redash could equip the team the abilities to perform better UI and ad-hoc analysis)
2. spark - batch processing
3. Jenkins - CI/CD
4. postgres + dbt - data warehouse and transformation
5. airflow - pipeline orchestration

## ML ops
1. Data flow
   1. data flows into postgresql and is transformed by dbt on a schedule(hourly)
   2. data is then loaded into spark for batch processing
2. Model flow
   1. Spark is used to train the model
   2. Model come through jenkins and is deployed to the edge device
   3. Model is then used to make predictions
   4. Predictions are sent to grafana for visualization
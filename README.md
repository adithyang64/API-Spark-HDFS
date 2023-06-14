# API-Spark-HDFS

This repo uses a Docker Image to Setup an Hadoop-Spark Environment. The Data flow is in a specific sequence where Data is fetched from an External API Source, followed by loading it into a Spark DataFrame. Analysis on data is made on top of it. Finally, data is stored in the File Path as Parquet Files.

![image](https://github.com/adithyang64/API-Spark-HDFS/assets/67658457/fc827025-40a9-4e46-b66d-ee4546c5abde)


The Docker image used in this project includes the following components:

Hadoop v3.2.1 || Spark v2.4.4 || Conda 3 with Python v3.7

Pull the docker image     [Credits: [Avnish Yadav](https://github.com/avnyadav?tab=repositories)]
```
docker pull avnish327030/spark-hadoop-airflow
```

Rename the pulled docker image
```
docker image tag  avnish327030/spark-hadoop-airflow spark-hadoop-airflow
```

Run the docker image
```
docker run -it -p 9870:9870 -p 8088:8088 -p 8080:8080 -p 18080:18080 -p 9000:9000 -p 8888:8888 -p 9864:9864 -p 8085:8085 -p 8793:8793 -p 8081:8081 -v D:\project\spark_etl_airflow-main\notebook:/root/ipynb -v D:\project\spark_etl_airflow-main\airflow:/home/airflow -v <**YOUR_PATH**>\data:/data avnish327030/spark-hadoop-airflow
```

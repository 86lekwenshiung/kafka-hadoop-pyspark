# Hadoop-Spark-ETL  

## **Overview**  
This project implements an **end-to-end ETL pipeline** using **Hadoop, Kafka, and PySpark** to process log data. It automates the process of generating logs, ingesting them via Kafka, storing them in HDFS, and performing aggregation using PySpark.  

## **Project Structure**  

Hadoop_Project/ │— Py_Script/ # Python scripts for ETL
│ ├── generate_logs.py # Step 1: Generate logs
│ ├── kafka_producer.py # Step 2: Kafka producer to send logs
│ ├── spark_aggregation.py # Step 4: PySpark script for aggregation
│ ├── config.py # Common configurations (paths, topics)
│ └── requirements.txt # Python dependencies
│
│— data/ # Raw and processed data
│ ├── logs/ # Stores generated log files
│ └── hdfs_output/ # Stores Spark processed data
│
│— scripts/ # Helper scripts (batch/shell scripts)
│ ├── start_hadoop.sh # Start Hadoop services
│ ├── start_kafka.sh # Start Kafka broker
│ └── run_spark.sh # Run PySpark job
│
│— config/ # Configuration files
│ ├── kafka_config.properties # Kafka configuration
│ ├── hadoop_env.sh # Hadoop environment variables
│ └── spark_config.conf # Spark settings
│
│— .gitignore # Ignore logs, temporary files
│— README.md # Documentation
│— requirements.txt # Python dependencies

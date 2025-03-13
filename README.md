# Hadoop-Spark-ETL  

## **Overview**  
This project implements an **end-to-end ETL pipeline** using **Hadoop, Kafka, and PySpark** to process log data. It automates the process of generating logs, ingesting them via Kafka, storing them in HDFS, and performing aggregation using PySpark.  

## **Project Structure**  

# Hadoop Project Structure

## Directory Structure

- **Hadoop_Project/**
  - **Py_Script/**: Python scripts for ETL
    - `generate_logs.py`: For Generating logs
    - `kafka_producer.py`: Kafka producer to ingest logs
    - `spark_aggregation.py`: PySpark script for aggregation
    - `config.py`: Common configurations (paths, topics)
    - `requirements.txt`: Python dependencies
  - **data/**: Raw and processed data
    - **logs/**: Stores generated log files
    - **hdfs_output/**: Stores Spark processed data
  - **scripts/**: Helper scripts (batch/shell scripts)
    - `start_hadoop.sh`: Start Hadoop services
    - `start_kafka.sh`: Start Kafka broker
    - `run_spark.sh`: Run PySpark job
  - **config/**: Configuration files
    - `kafka_config.properties`: Kafka configuration
    - `hadoop_env.sh`: Hadoop environment variables
    - `spark_config.conf`: Spark settings
  - `.gitignore`: Ignore logs, temporary files
  - `README.md`: Documentation
  - `requirements.txt`: Python dependencies


## **Setup Instructions**  

### **1. Install Dependencies**  
Ensure Python, Hadoop, Kafka, and Spark are installed and configured.  


```
pip install -r Py_Script/requirements.txt
```

### **2. Generate Log Data** 
Run the script to create log files
```
python Py_Script/generate_logs.py
```

### **3. Start Kafka & Hadoop**
Run the helper scripts to start services:
```
sh scripts/start_hadoop.sh  
sh scripts/start_kafka.sh
```

### **4.Produce Logs to Kafka**
Send logs to Kafka for ingestion:
```
python Py_Script/kafka_producer.py
```

### **5.sh scripts/run_spark.sh**
Process logs stored in HDFS using Spark:
```
python Py_Script/kafka_producer.py
```

Technologies Used
- Hadoop (HDFS for log storage)
- Kafka (Data ingestion pipeline)
- PySpark (Aggregation & processing)
- Python (ETL scripting)





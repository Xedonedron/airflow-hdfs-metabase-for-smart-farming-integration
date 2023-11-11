# Airflow, HDFS, Metabase - Data Lake for Smart Farming

Technology used: *Python, Selenium, Apache Airflow, Hadoop Distributed File System, Metabase*

## Abstract
Smart farming combines Information and communication technologies (ICT) with traditional agricultural practices to improve the quality and quantity of agricultural products. These ICTs could be Unmanned Aerial Vehicles (UAVs) or drones, artificial intelligence, robots, and sensors. In Smart Farming systems, various data types are needed, such as food prices, sensors, weather, images, and video. The data can be structured, semi-structured, or unstructured. Therefore, a system that can integrate Smart Farming data with versatility characteristics is needed to empower various types of analysis. In this study, the authors suggested using a Smart Farming Data Lake System based on Apache Airflow as data integration automation technology, Hadoop Distribution File System (HDFS) as data storage technology, and Metabase as dashboard technology.

## Prerequisite

- Python 3
- Java 11
- Selenium 4.9.1
- Pandas 2.0.1
- Hadoop 3.2.1
- Apache Airflow 2.6.1
- Metabase v0.43.1

## Process

1. Set up the Hadoop environment for HDFS (as a data lake)
2. Set up the Apache Airflow, used for ochestrator
3. Set up the Metabase environment for Business Intelligence, used to display dashboards related to metrics or charts from Airflow data.
4. Creating DAG file of the web scraper for weather info from [*BMKG Website*](https://www.bmkg.go.id/cuaca/prakiraan-cuaca-indonesia.bmkg), and food prices from [*PIHPS Website*](https://www.bi.go.id/hargapangan/TabelHarga/PasarModernKomoditas).
5. Creating DAG file to send a command to capture an image and record video into RapsberryPi (Linux-based Operating System).
6. Creating DAG flie to retrieve the sensor data from InfluxDB using API.
7. Running each DAG on Apache Airflow
8. Review the result on Apache Airflow and ensure the data compeletly exist in HDFS
9. Review the Apache Airflow performance using Metabase Business Intelligence

## Source code: Python script (DAG file) & SQL Query for Metabase
- [*Web_Scraper_DAG*](https://github.com/Xedonedron/data-lake-for-smart-farming/blob/main/dags/Web_Scraper_DAG.py)
- [*Sensor_retrieve_DAG*](https://github.com/Xedonedron/data-lake-for-smart-farming/blob/main/dags/Sensor_retrieve_DAG.py)
- [*Camera_data_capture*](https://github.com/Xedonedron/data-lake-for-smart-farming/blob/main/dags/Camera_data_capture.py)
- [*SQL Query for Metabase*](https://github.com/Xedonedron/data-lake-for-smart-farming/blob/main/Dashboard/Metabase%20Dashboard%20Query.txt)

## Output
The outcome was a:
- [*Weather info*](), [*food prices*](), and [*sensor data*]() dataset that presents results in expected format.
- [*Dashboard*](https://github.com/Xedonedron/data-lake-for-smart-farming/blob/main/Dashboard/metabase%20dashboard.png) from Metabase Business Intelligence

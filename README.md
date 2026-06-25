# WESOnline Tutorial

Data Engineering tutorial projects built with Python, Apache Airflow, PostgreSQL, and Docker. This repository demonstrates the design and implementation of end-to-end data pipelines using different data sources, including REST APIs and Excel files.


# Overview

This repository contains two mini-projects designed to showcase common Data Engineering workflows:

1. Customer Cart Pipeline : A data pipeline that extracts customer cart data from API endpoints, performs transformations, and loads the processed data into PostgreSQL.

2. Survey Data Pipeline : A data pipeline that ingests survey data from a local Excel file, applies data transformations and validations, and loads the results into PostgreSQL.

Both projects are orchestrated using Apache Airflow and containerized with Docker to ensure reproducibility and ease of deployment.

## Tech Stack
* Python
* Apache Airflow
* PostgreSQL
* Docker & Docker Compose
* Pandas
* SQL


## Project 1: Customer Cart Pipeline
### Objective

Build an ETL pipeline that extracts customer cart data from external API endpoints and stores the processed data in PostgreSQL.

### Workflow
Extract customer cart data from API endpoints.
Perform data cleaning and transformation.
Validate data quality.
Load transformed data into PostgreSQL.
Schedule and monitor the pipeline using Airflow.

<img width="959" height="416" alt="image" src="https://github.com/user-attachments/assets/fd9c91fb-1663-44df-ad63-4accba69dbdd" />



## Project 2: Survey Data Pipeline
### Objective

Build a batch-processing pipeline that ingests survey responses from an Excel file and loads the cleaned data into PostgreSQL.

### Workflow
Read survey data from Excel.
Clean and standardize records.
Perform validation checks.
Load processed data into PostgreSQL.
Schedule and monitor execution with Airflow.

<img width="976" height="420" alt="image" src="https://github.com/user-attachments/assets/795e1642-80a4-4275-9fb3-4ba0754ead43" />


## Getting Started
### Prerequisites

Ensure the following are installed:

* Docker
* Docker Compose
* Git

<img width="1004" height="595" alt="image" src="https://github.com/user-attachments/assets/f92837b1-918a-494b-b3bd-ade178f435f6" />


### Clone the Repository

git clone https://github.com/BrightOsas/wesonline-data-engineering-tutorial.git

cd wesonline-data-engineering-tutorial  

### Start the Environment

docker compose up --build

### Access Airflow

Once the containers are running, open the Airflow web interface and unpause the DAGs.

Login using the credentials configured in your Airflow environment.

### Access Pgadmin

* Open the pgAdmin web interface.
* Create and configure a new server connection.
* Set the Host name/address to postgres (this is the default hostname defined in the docker-compose.yml file).
* If you changed the PostgreSQL service name or hostname in your Docker Compose configuration, use the hostname you configured instead.

<img width="1070" height="650" alt="image" src="https://github.com/user-attachments/assets/22f06eeb-622c-415e-8472-83a6dd1a21c2" />


## Learning Objectives

This repository demonstrates:

* Building ETL pipelines with Python
* Working with REST APIs
* Processing Excel datasets
* Orchestrating workflows using Apache Airflow
* Loading data into PostgreSQL
* Containerizing data applications with Docker
* Creating reproducible Data Engineering environments


## Challenge

Now it's your turn! Complete the following tasks to reinforce what you've learned.

### Part 1: Environment Setup
* Set up the project on your local machine.
* Verify that all Docker containers are running successfully.
* Access the Airflow web interface and ensure both DAGs are available.
* Trigger each DAG and confirm that the pipelines complete successfully.
* Validate the loaded data by querying the Bronze and Silver layer tables using pgAdmin.

### Part 2: Extend the Data Pipeline
Currently, both projects load data into the Bronze and Silver layers only. No data is being loaded into the Gold layer.

Your task is to extend each pipeline by implementing a Gold layer.

### Customer Cart Project
* Create at least one Gold layer transformation using data from the Silver layer.
* Load the transformed data into the gold_layer schema.
* Update the Airflow DAG to include the new Gold layer task.
* Configure the task dependencies so the Gold task runs only after the Silver layer has completed successfully.
### Survey Data Project
* Create at least one Gold layer transformation using data from the Silver layer.
* Load the transformed data into the gold_layer schema.
* Update the Airflow DAG to include the new Gold layer task.
* Configure the task dependencies so the Gold task runs only after the Silver layer has completed successfully.

### Part 3: Validation

After implementing the Gold layer:
* Trigger both DAGs.
* Confirm that all tasks complete successfully.
* Verify that the Gold layer tables have been created.
* Validate the data by querying the Gold layer tables in pgAdmin.
* Ensure the transformed data accurately reflects the business logic you implemented.


## Author

Created as a beginner-friendly Data Engineering project designed to introduce new learners to ETL development, workflow orchestration, and data pipeline fundamentals using Python, Apache Airflow, PostgreSQL, and Docker.

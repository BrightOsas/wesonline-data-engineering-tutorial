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

<img width="659" height="316" alt="image" src="https://github.com/user-attachments/assets/fd9c91fb-1663-44df-ad63-4accba69dbdd" />



## Project 2: Survey Data Pipeline
### Objective

Build a batch-processing pipeline that ingests survey responses from an Excel file and loads the cleaned data into PostgreSQL.

### Workflow
Read survey data from Excel.
Clean and standardize records.
Perform validation checks.
Load processed data into PostgreSQL.
Schedule and monitor execution with Airflow.

<img width="776" height="320" alt="image" src="https://github.com/user-attachments/assets/795e1642-80a4-4275-9fb3-4ba0754ead43" />


## Getting Started
### Prerequisites

Ensure the following are installed:

* Docker
* Docker Compose
* Git

<img width="704" height="295" alt="image" src="https://github.com/user-attachments/assets/f92837b1-918a-494b-b3bd-ade178f435f6" />


### Clone the Repository

git clone https://github.com/BrightOsas/wesonline-data-engineering-tutorial.git

cd wesonline-tutorial

#### Start the Environment

docker compose up --build

#### Access Airflow

Once the containers are running, open: http://localhost:8080

Login using the credentials configured in your Airflow environment.

## Learning Objectives

This repository demonstrates:

* Building ETL pipelines with Python
* Working with REST APIs
* Processing Excel datasets
* Orchestrating workflows using Apache Airflow
* Loading data into PostgreSQL
* Containerizing data applications with Docker
* Creating reproducible Data Engineering environments


## Author

Created as a beginner-friendly Data Engineering project designed to introduce new learners to ETL development, workflow orchestration, and data pipeline fundamentals using Python, Apache Airflow, PostgreSQL, and Docker.

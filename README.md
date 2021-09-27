# Cardiological Examinations Graph
This repository contains the final project of the **Big Data Analytics and Business Intelligence** course (AY 20/21) at the *University of Naples Federico II*.

## Assignment
A dataset containing medical information of different patients is provided. Patient's information includes its examinations, with the relative anamnesis and diagnosis, written in Italian.
The aim of the project is to build a **Named Entity Recognition (NER)** system capable of extracting diseases and symptoms from textual inputs. Labeled data are provided to train the model.
Once the NER system is developed, a **graph-based database** must be developed, integrating patients information (examinations, diseases, symptoms, etc.).

## Project
The project, developed in team of 3, is structured as following:
- [preprocessing](https://github.com/fabiod20/big-data-analytics-and-business-intelligence/tree/main/preprocessing) directory contains *data cleaning* and *data preparation* steps, both performed using **PySpark** in a distributed environment, provided by **Databricks**.
- [ner-system](https://github.com/fabiod20/big-data-analytics-and-business-intelligence/tree/main/ner-system) directory contains *training* and *inference* of the NER system, implemented using **John Snow Labs (Spark NLP)**. The system is based on a version of BERT pre-trained on an Italian dataset, and it has been fine-tuned for 10 epochs, exploiting GPUs on **Google Colab**. However, due to the scarcity of labeled data, the model reached limited performance.
- [graph-based-database](https://github.com/fabiod20/big-data-analytics-and-business-intelligence/tree/main/graph-based-database) directory contains the code used to populate a *graph-based database*, built using **Neo4j**. The database stores all the relevant information of the patients, interconnecting each patient with its examinations, diseases, symptoms, drugs and doctors.
- [data-visualization](https://github.com/fabiod20/big-data-analytics-and-business-intelligence/tree/main/data-visualization) directory contains:
  - Three *dashboards* developed in **Microsoft Power BI**, which show respectively general information about doctors, the clinical situation of a given patient, and correlation among diseases, symptoms and drugs.
  - A *bloom perspective* implemented in **Neo4j Bloom**, which allows the user to explore the graph without the need to know *Cypher Query Language.*
- [documentation](https://github.com/fabiod20/big-data-analytics-and-business-intelligence/tree/main/documentation) directory contains an exhaustive documentation of the project, written in Italian.

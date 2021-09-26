# Cardiological Examinations Graph
This repository contains the final project of the **Big Data Analytics and Business Intelligence** course at *University of Naples Federico II*.

## Assignment
A dataset containing medical information of different patients is provided. Patient's information includes its examinations, with the relative anamnesis and diagnosis, written in Italian.
The aim of the project is to build a **Named Entity Recognition (NER)** system capable of extracting diseases and symptoms from textual inputs. Labeled data are provided to train the model.
Once the NER system is developed, a **graph-based database** must be developed, integrating the patients information (examinations, diseases, symptoms, etc.).

## Code
The project, developed in team of 3, is structured as following
- [preprocessing](https://github.com/fabiod20/big-data-analytics-and-business-intelligence/tree/main/preprocessing) directory contains *data cleaning* and *data preparation* steps, both performed using **PySpark** in a distributed environment, provided by **Databricks**.
- [ner-system](https://github.com/fabiod20/big-data-analytics-and-business-intelligence/tree/main/ner-system) directory contains *training* and *inference* of the NER system, implemented using **John Snow Labs (Spark NLP)**. The system is based on BERT, pre-trained on an italian dataset, and it has been fine-tuned for 10 epochs, exploiting GPUs on **Google Colab**. However, due to the scarcity of labeled data, the model reached limited performance.
- [graph-based-database](https://github.com/fabiod20/big-data-analytics-and-business-intelligence/tree/main/graph-based-database)

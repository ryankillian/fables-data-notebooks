---

# Fables Motif Mapping

This repository contains Jupyter notebooks and related assets for the project focused on mapping fine-grained motifs from fables to broader, general themes. Using a combination of machine learning and natural language processing techniques, we aim to derive meaningful insights from the motifs present in various fables.

## Technologies Used

- **Jupyter Notebooks**: An open-source web application that allows for the creation and sharing of documents containing live code, equations, visualizations, and narrative text.
- **Google Colab**: A cloud-based platform that offers free access to GPUs and TPUs, simplifying the process of running Jupyter notebooks without any setup.
- **Scikit-learn**: A machine learning library for Python. It features various algorithms like support vector machine, random forests, and k-neighbours. For this project, we primarily used its clustering algorithms, such as KMeans.
- **BERT (Bidirectional Encoder Representations from Transformers)**: A transformer-based machine learning technique for natural language processing pre-training. It's designed to understand the meaning of each word in a sentence by looking at its surrounding context in both directions.

## Project Structure

- `AWS-Comprehend/`: This directory contains AWS Comprehend analysis. It showcases the methodology adopted for leveraging AWS's natural language processing service to derive insights from the text data.

- `BERT-Analysis`: Directory containing Jupyter notebooks that detail the use of BERT for natural language processing and motif analysis. These detail the process of extracting embeddings from the BERT model. These embeddings are later used in clustering and other analyses to understand patterns and topics within the text.

- `KMeans-Clustering`: Directory containing Jupyter notebooks related to the KMeans clustering approach for motif mapping.

- `data/`: All the primary datasets and relevant data files used across different analyses are stored in this directory.

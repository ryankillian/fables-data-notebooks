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

- `results/`: Directory contain finished motif mapping file.

## Here's a summarized description of our process:

**Objective**:
The main goal was to categorize a list of 700 fine-grained motifs into a smaller number of general themes/motifs to enable faster and more efficient searching.

**Steps Taken**:

1. **Text Representation**:

   - The motifs were vectorized using the TF-IDF (Term Frequency-Inverse Document Frequency) method, which transformed the text data into numerical format suitable for machine learning models.

2. **Dimensionality Reduction**:

   - Due to the high dimensionality of the TF-IDF vectors, we applied PCA (Principal Component Analysis) to reduce the dimensions while retaining the most significant information.

3. **Clustering with K-Means**:

   - We first attempted K-Means clustering with 20 clusters. After visual inspection of the clusters, we found that the distribution of motifs among clusters was skewed, with one cluster containing a disproportionately large number of motifs.
   - We iteratively experimented with various cluster counts (12, 30, 8) to find a more balanced and interpretable distribution.

4. **Attempts with AWS Comprehend**:

   - As an aside, we decided to explore AWS Comprehend for topic modeling, hoping it might provide an effective way to cluster the motifs.
   - After processing the motifs through AWS Comprehend's topic modeling, we obtained clusters. However, the clusters were not particularly coherent or interpretable for our use case.

5. **Alternative Clustering with BERT**:

   - Given the challenges faced with K-Means, we decided to use BERT embeddings for representing the motifs, taking advantage of the state-of-the-art language model's capability to capture semantic meanings.
   - With the BERT representations, we again applied K-Means clustering.

6. **Clustering with K-Means**:

   - We first attempted K-Means clustering with 20 clusters. After visual inspection of the clusters, we found that the distribution of motifs among clusters was skewed, with one cluster containing a disproportionately large number of motifs.
   - We iteratively experimented with various cluster counts (12, 30, 8) to find a more balanced and interpretable distribution.

7. **Cluster Interpretation & Labeling**:

   - For each clustering result, the top motifs of each cluster were reviewed to assign meaningful labels or themes. This interpretive step was crucial in understanding the core idea represented by each cluster.

8. **Finalizing the Clustering**:

   - After several iterations and examinations of clustering results, we settled on 8 general themes or clusters, which provided a balanced and meaningful categorization of the original 700 motifs.

9. **Analysis of Results**:
   - Once the motifs were mapped to their respective general themes, we conducted a quantitative analysis to understand the distribution of fine-grained motifs among the general themes.


**Outcome**:
We successfully reduced the 700 fine-grained motifs into 8 coherent and general themes. This categorization should facilitate faster searching and better organization of the motifs for users. See `data/` and `results/`.

Here's the distribution of fine-grained motifs across each general motif:

1. **Awareness**: 141 motifs
2. **Growth**: 116 motifs
3. **Emotions**: 104 motifs
4. **Deception**: 91 motifs
5. **Values**: 88 motifs
6. **Power**: 85 motifs
7. **Collaboration**: 43 motifs
8. **Choices**: 31 motifs

---

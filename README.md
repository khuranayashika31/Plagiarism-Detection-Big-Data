# Plagiarism-Detection-Big-Data
**Concept:** _Chapter 3 - Mining Massive Datasets_

**Tool:** _Spark_

## Overview
This repository contains the code used to identify duplicate (or closely related) articles.
We employ the Minhash/LSH algorithm for identifying the ten most closely related entries to a designated reference article. 

## Minhash/LSH Algorithm
The Minhash/LSH (Locality-Sensitive Hashing) algorithm is a technique used in the field of data mining and similarity analysis, specifically for identifying similar items within large datasets. This algorithm is often applied to handle high-dimensional data efficiently, such as documents, images, or other types of records.

## More on the algorithm

* In the context of document similarity, Minhashing is a method to estimate the Jaccard similarity between two sets. The Jaccard similarity is a measure of how much two sets overlap. To perform Minhashing, the sets (representing, for example, the words in two documents) are hashed using multiple hash functions. The minimum hash value for each hash function is then retained.
The collection of these minimum hash values generates a signature for each set, and the similarity between two sets is approximated by the ratio of matching minimum hash values to the total number of hash functions used.

* LSH is a method that amplifies the probability of similar items having the same hash value, making it more likely for them to be grouped together.In the Minhash/LSH algorithm, the Minhash signatures generated for items are divided into bands, and hash functions are applied to these bands. Items that hash to the same value in at least one band are considered potential candidates for similarity.
By focusing the similarity search on these candidate pairs, the algorithm significantly reduces the computational effort required to find similar items in large datasets.
![image](https://github.com/khuranayashika31/Plagiarism-Detection-Big-Data/assets/51834607/da382693-c729-4012-8b31-ac42e666d1e9)

Image by: One Stop Data Analysis

Combining Minhashing and LSH provides an efficient way to approximate similarity between items in a large dataset, making it particularly useful for tasks such as identifying similar documents, images, or any other types of records where set similarity is relevant.

P.S: Dataset & notebook in the repository.

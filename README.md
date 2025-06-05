# 📊 Cloud Computing Group Assignment_1

## 👨‍💻 Team Members
- **EG/2020/4248**
- **EG/2020/3893**
- **EG/2020/3851**

---

## 📝 Project Overview

This project implements the **WordCount MapReduce** job using **Hadoop**, applied to the **Enron Email Dataset**. The WordCount job is a foundational example in big data processing — showcasing how large volumes of data can be processed **in parallel** across a cluster using the **MapReduce** paradigm.

---

## 📂 Dataset: Enron Email Dataset

- Contains approximately **500,000 emails**.
- Emails include **sender**, **receiver**, **subject**, and **body** fields.
- Originally released by the **Federal Energy Regulatory Commission (FERC)** during the Enron Corporation investigation.
- link of the data set
  https://www.kaggle.com/datasets/wcukierski/enron-email-dataset
  
---

## ⚙️ MapReduce Workflow

### 1️⃣ Input
- **Source:** Raw textual email files.
- **Storage:** Hadoop Distributed File System (HDFS).

### 2️⃣ Splitting
- Hadoop automatically splits the dataset into smaller chunks for distributed processing.

### 3️⃣ Mapper Phase
Each Mapper:
- Reads email text.
- Extracts text from **subject** and **body** fields.
- Tokenizes into words.
- Emits `(word, 1)` key-value pairs.

### 4️⃣ Shuffle & Sort
- Intermediate results are grouped by key (word).
- All occurrences of a word are collected and forwarded to the same Reducer.

### 5️⃣ Reducer Phase
Each Reducer:
- Receives grouped `(word, 1)` pairs.
- Aggregates word counts using summation.
- Emits final output: `(word, total_count)`.

### 6️⃣ Output
- The final word counts are written back to HDFS for further analysis or usage.
- Here is the structure of the final output
  
![Screenshot 2025-06-05 162955](https://github.com/user-attachments/assets/d6fc5c92-ec1f-481a-80c3-b734becf0425)

---

## 🚀 Technologies Used
- **Apache Hadoop**
- **MapReduce Programming Model**
- **HDFS (Hadoop Distributed File System)**
- **Java (depending on your implementation)**

---

## 📌 Objective
The primary objective of this MapReduce process is to **efficiently analyze the Enron email dataset (~500,000 emails)** using **Hadoop's distributed computing capabilities**. Specifically, the goal is to **identify and count the frequency of each unique word** across the email dataset, demonstrating Hadoop’s effectiveness in handling **large-scale text processing** tasks.

This project aims to showcase the power of **distributed computing** and **parallel processing** by applying the **MapReduce model** to analyze a real-world dataset at scale.

---



# 📊 Cloud Computing Group Assignment_1

## 👨‍💻 Team Members

- **EG/2020/3893** - **Dias B.R.S.T.**
- **EG/2020/4248** - **Umayangana D.M.I.**
- **EG/2020/3851** - **Bandara W.R.S.M.**

---
## 📝 Project Title

### Classic Word-Count MapReduce Job for Enron Email Dataset

---

## 📝 Project Overview

This project implements the **WordCount MapReduce** job using **Hadoop**, applied to the **Enron Email Dataset**. The WordCount job is a foundational example in big data processing — showcasing how large volumes of data can be processed **in parallel** across a cluster using the **MapReduce** paradigm.

---

## 📘 Project Introduction

This project implements a Hadoop MapReduce-based word count analysis on the Enron Email Dataset, a publicly available collection of over 500,000 emails exchanged among employees of the Enron Corporation. Using the **WordCount MapReduce** programs, we process and analyze the textual data to identify the most frequently used words across the email communications.

The goal is to demonstrate how Hadoop can efficiently handle large-scale, unstructured large data (over 1 lakh) using parallel processing. This analysis not only serves as a practical application of distributed computing but also provides insights into communication patterns within a real corporate environment.

---

## 📂 Dataset: Enron Email Dataset

- Contains approximately **500,000 emails**.
- Emails include **sender**, **receiver**, **subject**, and **body** fields.
- Originally released by the **Federal Energy Regulatory Commission (FERC)** during the Enron Corporation investigation.
- link of the data set:
  https://www.kaggle.com/datasets/wcukierski/enron-email-dataset
  
---

## 📂 Hadoop Installation
-  Here's the documentation link of the Hadoop Installation Steps for Linux(Ubuntu): https://drive.google.com/file/d/1iK62pSt7uILSDrKyx5ImPHozJqZGkdfJ/view?usp=sharing

---

## ⚙️ MapReduce Workflow

- Here's the documentation link of the steps to Execute Hadoop MapReduce WordCount Job for Enron Email Dataset:
  https://drive.google.com/file/d/1462UBM3RH6mASc3KyACK5yH_D_sgqUYX/view?usp=sharing
  
### 1️⃣ Input
- **Source:** Raw email csv files. (link of the dataset is provided above)
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
- Here is a screenshot of the structure of the final output data after Map-Reducing process using wordcount Map-Reduce:
  
![Screenshot 2025-06-05 162955](https://github.com/user-attachments/assets/d6fc5c92-ec1f-481a-80c3-b734becf0425)

The structure of the output is in the format: (word, total_count), where each line represents a unique word feature and the number of times it appeared in the dataset.

📁**Here's the link of the Output-data files (.csv and .txt) after Map Reducing process:**
https://drive.google.com/drive/folders/1POQb5G89sBv_a2GB-N5SCP9p4g5cKbdj?usp=sharing


📁**Here is the Drive link with all documentation (Hadoop setup & WordCount steps) and the output files from the Word-count MapReduce process:**
https://drive.google.com/drive/folders/1kvGZrlPIPgTcehGPbMcJxY9kaxJkkOf9?usp=sharing

---

## 📁 Drive Link – Complete Assignment Package

You can access the full assignment package through the Google Drive link below:

https://drive.google.com/drive/folders/1kvGZrlPIPgTcehGPbMcJxY9kaxJkkOf9?usp=sharing

Contents of the folder:

  - 📄 Complete documentation (including Hadoop installation and WordCount process)

  - 💻 Source code and program files (Word-count Map-reduce Program as a zip file)

  - 🖼️ Screenshots of execution steps and output

  - 📽️ Video demonstration of Hadoop Installation and the MapReduce job

  - 📊 Output data files (emails-count.txt, emails-count.csv)

This folder serves as a backup and reference for all materials related to the project submission.

### Drive link of Hadoop-mapreduce-word-count-Java-program: 
https://drive.google.com/file/d/1UVvIYcQfuZmJY0x_UlyAli7FkHsO2rz9/view?usp=sharing


---

## 🚀 Technologies Used
- **Apache Hadoop**
- **MapReduce Programming Model**
- **HDFS (Hadoop Distributed File System)**
- **Java **

---

## 📌 Objective
The primary objective of this MapReduce process is to **efficiently analyze the Enron email dataset (~500,000 emails)** using **Hadoop's distributed computing capabilities**. Specifically, the goal is to **identify and count the frequency of each unique word** across the email dataset, demonstrating Hadoop’s effectiveness in handling **large-scale text processing** tasks.

This project aims to showcase the power of **distributed computing** and **parallel processing** by applying the **MapReduce model** using Apache Hadoop software to analyze a real-world large dataset (over 1 lakh) at scale.

---

## 📊 Results summary (Verified and Analyzed Results)

The MapReduce WordCount process successfully analyzed approximately 500,000 emails from the Enron dataset. The job counted word frequencies across the entire dataset using Hadoop's distributed processing capabilities. The most frequently occurring words were common in corporate communication, such as:
  Top Frequent Words:

- "the": ~4.9 million occurrences

- "to": ~3.4 million occurrences

- "and", "of", "a": each appeared over 1–2 million times

- These high-frequency terms suggest the dataset is rich in general language, with dense narrative communication typical of business emails.

- While common stop-words dominated the output, the analysis:

- Verified successful execution of the MapReduce job on large-scale input

- Confirmed accurate word count results

- Demonstrated Hadoop’s strength in processing real-world, unstructured data efficiently

- Output Dataset Files:

- emails-count.csv

- emails-count.txt

- Open either file to view the word frequencies.
  
- ✅ Below is a screenshot/table showing the Top 20 Word Frequencies from the output.  

  ![image](https://github.com/user-attachments/assets/f9d766a2-325e-489e-a7a3-a7a9e22073b3)



---

## 🔎 Result Interpretation

The output represents word frequency across the Enron email dataset, allowing analysis of frequent keywords and potential insights into communication patterns within Enron.
The WordCount MapReduce job executed on the Enron email dataset successfully produced frequencies of words across approximately 500,000 emails. Commonly occurring terms such as "enron," "energy," "meeting," "report," and names of key employees emerged prominently, highlighting core topics and frequent discussion points within the organization.
The dataset provided insights into the internal communications at Enron, showcasing themes of corporate operations, scheduling meetings, energy trading, and strategic reporting. It clearly reflects Enron’s primary business activities and the nature of corporate discussions occurring during the company’s operational period.
Regarding performance, the Hadoop framework effectively managed the large-scale data, achieving parallel processing across multiple mapper and reducer tasks. Though the job completed successfully, performance optimization could be improved by fine-tuning Hadoop cluster resources, increasing the number of reducers, or implementing data filtering to reduce irrelevant content early in the processing stage, thus enhancing both accuracy and efficiency.

Suggested Improvements:
- Preprocessing: Implement additional text-cleaning processes (removing irrelevant headers, footers, or stop-words) to reduce noise and enhance result accuracy.
-	Resource Optimization: Adjust Hadoop cluster settings (e.g., increase memory allocation, fine-tune mapper and reducer count) to speed up processing.
-	Advanced Analytics: Explore advanced analytics techniques such as sentiment analysis or topic modeling (e.g., LDA) to derive deeper insights from email content.

---

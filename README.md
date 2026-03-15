# 🛡️ AI-Powered Network Anomaly Detection

## 📖 Project Overview
This project demonstrates the integration of **Unsupervised Machine Learning** in Blue Team operations. By analyzing network traffic patterns using the **K-Means algorithm**, we can automatically establish a baseline and detect security anomalies (outliers) that could indicate malicious activity.

---

## 🚀 Key Features
* **Data Source:** Real-world network traffic captured via **Wireshark**.
* **Machine Learning:** Implementation of K-Means clustering using the **Scikit-learn** library.
* **Data Visualization:** High-resolution scatter plots showing 5 distinct traffic clusters and their centroids.
* **Security Insights:** Automated identification of unusual packets, including specific **TLSv1.3** application data spikes.

---

## 🛠️ Step-by-Step Guide: How to Capture Data

To replicate this project, follow these steps in **Wireshark**:

### 1. Launch Capture
* Open Wireshark and select your active network interface.
* Click the **Blue Shark Fin** icon to start.

### 2. Generate Traffic (Baseline)
* Perform normal activities (browsing, streaming) for 5 minutes. This creates the "Normal" data behavior.

### 3. Stop and Export
* Go to **File > Export Packet Dissections > As CSV...**
* Save the file as `test_cap.csv` in your project folder.

---

## 📊 Results & Visualization
The AI successfully groups thousands of packets into clusters. Below is the visual representation of the analysis:

![Network Analysis Graph](Analysis_graph.png)

> **Note:** Isolated data points (Outliers) far from the centroids represent anomalies that a SOC Analyst must investigate.

---

## 📚 Blue Team Vocabulary
* **Unsupervised Learning:** AI that finds patterns without pre-defined labels.
* **Baseline:** The "normal" state of network activity.
* **Outlier:** A data point that differs significantly from others.

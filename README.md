# 🛡️ AI-Powered Network Anomaly Detection

## 📖 Project Overview
This project demonstrates the integration of **Unsupervised Machine Learning** in Blue Team operations. Using the **K-Means Clustering** algorithm, we analyze network traffic patterns to automatically establish a baseline and detect security anomalies (outliers) that could indicate malicious activity.

---

## 🚀 Key Features
* **Data Source:** Real-world network traffic captured via **Wireshark**.
* **Machine Learning:** Implementation of K-Means clustering using the **Scikit-learn** library.
* **Data Visualization:** High-resolution scatter plots showing 5 distinct traffic clusters and their centroids.
* **Security Insights:** Automated identification of unusual packets, including specific **TLSv1.3** application data spikes.

---

## 🛠️ Step-by-Step Guide: How to Capture Data

To replicate this project, follow these detailed steps in **Wireshark**:

### 1. Launch Capture
* Open Wireshark and select your active network interface (Wi-Fi or Ethernet).
* Click the **Blue Shark Fin** icon to start the live capture.

### 2. Generate Traffic (Baseline)
* Perform normal activities (browsing, streaming, or background updates) for 5 minutes. This creates the "Normal" data behavior for the AI to learn.

### 3. Stop and Export
* Click the **Red Stop Button** once finished.
* Go to **File > Export Packet Dissections > As CSV...**
* Ensure **"All packets"** is selected and save the file as `test_cap.csv` in your project folder.

---

## 💻 Execution & Technical Details

The analysis is performed by the main Python script which **fetches** data from the exported Wireshark CSV.

* **Main Script:** `kmeans_script.py`
* **Data Source:** `test_cap.csv`

### **How to Run**
1. **Install Dependencies:**
   ```bash
   pip install pandas scikit-learn matplotlib

   Run the Script:
Open your terminal in the project directory and run:

Bash
python kmeans_script.py test_cap.csv

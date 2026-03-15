Network Anomaly Detection using K-Means Clustering
Project Overview
This project demonstrates the integration of Unsupervised Machine Learning in Blue Team operations. By analyzing network traffic patterns using the K-Means algorithm, we can automatically establish a baseline and detect security anomalies (outliers) that could indicate malicious activity, such as data exfiltration or unauthorized scanning.

Key Features
Data Source: Real-world network traffic captured via Wireshark.

Machine Learning: Implementation of K-Means clustering using the Scikit-learn library.

Data Visualization: High-resolution scatter plots using Matplotlib showing 5 distinct traffic clusters and their centroids (Red Xs).

Security Insights: Automated identification of unusual packets, including specific TLSv1.3 application data spikes that deviate from normal patterns.

Step-by-Step Guide: How to Capture Data
To replicate this project, you need to capture your own network traffic using Wireshark:

1. Launch Capture
Open Wireshark and select your active network interface (Wi-Fi or Ethernet).

Click the Blue Shark Fin icon to start the live capture.

2. Generate Traffic (Baseline)
Browse websites, stream a video, or run background apps for 5 minutes. This creates the "Normal" data behavior for the AI to learn.

3. Stop and Export
Click the Red Stop Button once you have captured sufficient packets.

Go to File > Export Packet Dissections > As CSV...

Ensure "All packets" is selected and save the file as test_cap.csv in your project folder.

How to Run the Project
Install Dependencies:
Ensure you have Python installed, then run:
pip install pandas scikit-learn matplotlib

Execute the Script:
Point the script to your captured CSV file:
python kmeans_script.py test_cap.csv

Results & Conclusion
The AI successfully groups thousands of packets into clusters based on their mathematical similarity.

Normal Traffic: Clusters tightly around the centroids.

Potential Threats: Isolated data points (Outliers) far from the centroids represent anomalies. These are the packets that a SOC Analyst must investigate to ensure network security.

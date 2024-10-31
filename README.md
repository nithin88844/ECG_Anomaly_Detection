# ECG Anomaly Detection using Encoder-Decoder Algorithm
This repository contains an ECG anomaly detection system based on an encoder-decoder neural network architecture. The project aims to identify irregular heartbeats and anomalies in ECG signals by reconstructing normal signals and flagging deviations as potential anomalies.

## Table of Contents
* Project Overview
* Key Features
* Data Requirements
* Model Architecture
* Results
## 1. Project Overview
The ECG Anomaly Detection system is designed to:

Learn a compact representation of normal ECG signals.
Reconstruct the signals and measure the reconstruction error.
Flag signals with high reconstruction errors as potential anomalies, indicating abnormal heart activity.
## 2. Key Features
* Encoder-Decoder Architecture: Utilizes an autoencoder to learn efficient representations of ECG signals.
* Anomaly Detection: Detects deviations from normal heart rhythm by comparing reconstruction errors.
* Real-time Prediction: Can be adapted for real-time monitoring of heart rate signals.
* Visualization: Includes tools for visualizing both normal and anomalous ECG signals.
## 3. Data Requirements
* ECG Dataset: A dataset with labeled normal and abnormal heartbeats (e.g., MIT-BIH Arrhythmia Database).
* Data Format: Ensure the data is preprocessed into sequences suitable for time-series analysis. Each ECG segment should ideally be normalized for best results.
## 4. Model Architecture
* Encoder: Compresses the ECG signal into a latent space representation using LSTM layers.
* Decoder: Reconstructs the original signal, attempting to match it closely if it represents normal heartbeat patterns.
* Anomaly Scoring: Based on the reconstruction error (mean squared error), where higher error values are flagged as potential anomalies.
## 5. Results
The model was evaluated using a subset of labeled ECG data:

* Accuracy: 92%
* Sensitivity: 89% in detecting abnormal heart rhythms
* Latency: Processes approximately 120 signals per minute, suitable for near-real-time applications.
Example ROC Curve and Precision-Recall metrics can be found in the results/ directory.

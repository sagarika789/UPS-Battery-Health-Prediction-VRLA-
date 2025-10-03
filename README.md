# Predictive Maintenance for VRLA Battery Blocks (Schneider Electric Internship)
**Project Overview**
This project applies Machine Learning and statistical analysis to real-time sensor data (impedance and voltage) from Uninterruptible Power Supply (UPS) battery blocks. The goal was to compare battery block health, diagnose degradation, and predict potential failure points using a data-driven approach.

**Compliance Note**
This methodology and analysis were developed during an internship. No proprietary source code or internal data are included in this public repository to comply with the project's non-disclosure agreement (NDA). The focus here is on showcasing the ML methodology and analytical findings

# Features & Technologies
**Key Features**
* **Time-Series Analysis**: Analyzes historical impedance and voltage trends to identify degradation patterns over time (e.g., Block 48's impedance increase).

* **Health Scoring Model**: Creates a composite health score based on normalized inverse impedance and voltage to classify blocks as healthier/unhealthier using a Random Forest Classifier.

* **Failure Prediction**: Uses statistical thresholds to estimate the time of potential failure based on scoring metrics.

* **Unsupervised Analysis**: Implements K-Means Clustering to segment battery data into distinct operational states (Healthy, Degrading, Failed).

# Tech Stack

* Language- Python 3.x

* ML/Analytics- Random Forest, K-Means, Scikit-learn

* Data Handling- Pandas, NumPy, Matplotlib

* Domain- IoT Sensor Data, Predictive Maintenance (PdM), Time-Series Analysis

# Key Findings
The model successfully identified subtle degradation:

* **Block Health Classification**: The model confidently identifies Block 58 as the healthier unit (higher average voltage, lower variability) compared to Block 57.

* **Failure Timeline**: Estimated critical failure thresholds were reached around early 2024, guiding maintenance prioritization.

| Analysis Type            | Block 47 Metrics         | Block 48 Metrics         |
|--------------------------|--------------------------|--------------------------|
| **Average Voltage (V)**  | 13.68 V (Higher)         | 13.57 V (Lower)          |
| **Standard Deviation (V)** | 0.22 (Lower Variability) | 0.33 (Higher Variability) |

**Inference:**  
- Block 47 is healthier and more stable.  
- Block 48 shows signs of degradation (increasing impedance trend).  


**Dataset Note**
This project utilized proprietary time-series sensor data provided during the Schneider Electric internship (VRLA battery readings for UPS 1, 2, and 5). Due to NDA and proprietary nature, the raw CSV files are not included.

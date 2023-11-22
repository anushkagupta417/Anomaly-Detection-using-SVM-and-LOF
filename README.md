# Anomaly Detection using SVM with LOF

## Objective
The goal of this project is to detect anomalies in a dataset representing the status and characteristics of a system over time. This is achieved through the implementation of Support Vector Machine (SVM) and Local Outlier Factor (LOF) algorithms.

## Dataset Description
The dataset captures comprehensive information about the system, focusing on analog and digital parameters recorded over a specific duration.

### Data Columns
- Date
- Time
- P1 to P6 (Analog quantities)
- P7 to P9 (Digital quantities)

## Concept and Model
The code preprocesses the dataset by normalizing analog values using Min-Max scaling and combines datetime information for analysis. Anomaly detection employs One-Class SVM to model normal behavior and LOF to assess local density deviations. Detected anomalies are identified by comparing outcomes from both models, providing insights into significant deviations from expected patterns.

### SVM for Anomaly Detection
The SVM architecture involves training a one-class SVM model to encapsulate normal behavior using a hyperplane in a high-dimensional space. The 'nu' parameter controls the anomaly threshold, and anomalies are distinguished by their position relative to the hyperplane.

### LOF for Anomaly Detection
LOF assesses anomalies based on local density deviations. It calculates an LOF score for each point by comparing its local density to neighboring points. Lower LOF scores indicate normal behavior, leveraging the principle that anomalies have sparser neighborhoods.

## Output
The project generates visual outputs highlighting anomalies detected during analysis. From the obtained results, anomalies were identified on specific dates, such as 2011-10-11, 2011-11-03, and 2011-11-14.

## Dependencies
- pandas
- numpy
- scikit-learn

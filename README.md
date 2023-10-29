# Automated Myocardial Infarction Detection with Deep Learning

## Overview

This GitHub project is a result of a graduate research practice that took place from March 1, 2022, to June 30, 2022, in the School of Computer Science & Engineering. The primary goal of this project was to develop a deep learning model for automated detection and localization of myocardial infarction (MI) using electrocardiogram (ECG) data. The dataset used for this research is the PTB-XL database, which contains ECG records from a variety of patients.

## Introduction

Myocardial infarction (MI), commonly known as a heart attack, is a leading cause of death worldwide. Early and accurate diagnosis of MI is crucial for patient survival. ECGs play a significant role in diagnosing heart conditions. This project aimed to automate MI detection by developing a deep learning model.

## Data Source

The ECG data for this project was sourced from the open-access PTB-XL database. It contains 12-lead ECG recordings from a diverse range of patients.

You can access the dataset at [PTB-XL Dataset](https://physionet.org/content/ptb-xl/1.0.1/).

## Data Processing and Feature Extraction

1. **Data Acquisition and Balancing**: The dataset consists of various diagnostic classes, but for this project, we focused on "NORM" (Normal ECG) and "MI" (Myocardial Infarction) records.

2. **Data Preprocessing**: The ECG records were downsampled to 1000 records for each class, ensuring a balanced dataset.

3. **Feature Extraction**: Time-domain features, such as T wave amplitude, Q wave amplitude, and ST deviation measure, were extracted for each beat in the ECG records, resulting in a 36-dimensional feature vector.

## Model Architecture

The model for automated MI detection was built using deep learning techniques, specifically a combination of 1D Convolutional Neural Networks (CNN) and Bidirectional Long Short-Term Memory (Bi-LSTM) networks.

1. **CNN Layers**: A total of eight 1D CNN layers were used to extract spatial features from the ECG data.

2. **MaxPooling and Dropout**: MaxPooling layers were applied to downsample the feature maps, and dropout layers were used to prevent overfitting.

3. **Bi-LSTM Layers**: Three Bi-LSTM layers were used to capture sequential information in both forward and backward directions.

4. **Output Layer**: The model output was passed through dense layers with ReLU activation and softmax activation in the final layer for multi-class classification.

## Results

The model was evaluated with a test dataset and achieved impressive accuracy:

- **NORM (Normal ECG):** 86.46%
- **MI (Myocardial Infarction) Subclasses:** Ranged from 84.0% to 100.0%

The overall average accuracy of the model was 95.21%.

## Usage

To use this project, follow these steps:

1. **Data Download**: Download the PTB-XL dataset from [here](https://physionet.org/content/ptb-xl/1.0.1/).

2. **Data Preprocessing**: Use the provided code to preprocess and balance the dataset.

3. **Model Training**: Train the deep learning model using the code provided in the repository.

4. **Model Evaluation**: Evaluate the model using your test data or the provided test dataset.

## Learnings

During the research practice, the following skills and knowledge were acquired:

- Data processing and analysis in Python.
- Building and training deep learning models.
- Signal data analysis.
- Understanding the ECG waveform and its components.
- Research on myocardial infarction and ECG interpretation.

## Further Improvements

This project is a solid foundation for automated MI detection, but there is always room for improvement. Future enhancements may include:

- Fine-tuning hyperparameters for better performance.
- Exploring additional features or data sources.
- Enhancing the model's robustness and efficiency.


## Acknowledgments

- [PhysioNet](https://physionet.org) for providing the PTB-XL dataset.
Please feel free to contribute, suggest improvements, or use this project for your own research and applications related to myocardial infarction detection. Thank you for your interest and support!


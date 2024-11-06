# EEG Eye Detection Using XGBoost and Exploratory Data Analysis
## Description
This project focuses on predicting eye status (open or closed) using Electroencephalogram (EEG) data. We explore time-domain, frequency-space, and independent component analysis approaches, and build predictive models using XGBoost and Random Forest.

## Project Goals
Analyze and visualize EEG data to understand underlying patterns.
Build and evaluate machine learning models to predict eye status based on EEG signals.
Compare different modeling approaches to achieve high accuracy.

## Dataset
Source: EEG Eye State dataset collected using an Emotiv EEG Neuroheadset.
Details: The data consists of continuous EEG recordings annotated with eye status (1: closed, 0: open).
Duration: 117 seconds, sampled at 128 Hz, using 14 EEG electrodes.

## Installation
To run this project, you need R and the following packages:
install.packages(c("xgboost", "eegkit", "forecast", "tseries", "caret", "reshape2", "dplyr", "ggplot2"))

If you're on a Mac and encounter X11 issues, install XQuartz:
XQuartz Installation

## Project Setup
Clone the repository:
git clone <your-repo-link>

Install the required packages listed above.
Run the scripts provided for data analysis and modeling.

## Data Analysis
## Exploratory Data Analysis (EDA)
Check for missing values and visualize EEG intensities across different electrodes.
Perform time-domain analysis and investigate patterns related to eye status.
Use statistical tests to check for stationarity and autocorrelation in the time series data.
### Frequency-Space Analysis
Use Fast Fourier Transform (FFT) to analyze frequency components and observe power spectral densities for eye-open and eye-closed states.
Independent Component Analysis (ICA)
Apply ICA to explore whether there are independent sources of neuronal activity that relate to eye status.

### Modeling
XGBoost Model
Train an XGBoost model to predict eye status using EEG data.
Evaluate model performance using log-loss and accuracy metrics.
Random Forest Model
Use the caret library to fit a Random Forest model and compare performance with XGBoost.
### Results
XGBoost: Achieved progressive reduction in log-loss over 100 training rounds.
Random Forest: Achieved high accuracy on the validation set with an optimal mtry value.
### Performance Evaluation
Use confusion matrices to calculate metrics like accuracy, sensitivity, and specificity.
The Random Forest model showed better performance with an accuracy of 99.4%.

### Alternative Approaches
Recurrent Neural Networks (RNNs): Suitable for time series data, capturing temporal dependencies in EEG signals.
Hidden Markov Models (HMMs): Probabilistic models that can represent temporal dependencies in sequential data.

### R Libraries for Future Work
Keras: High-level API for building deep learning models, including RNNs (requires TensorFlow backend).
HiddenMarkov: R library for implementing Hidden Markov Models, supporting various types of HMMs.

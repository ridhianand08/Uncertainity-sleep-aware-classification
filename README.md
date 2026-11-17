
# Uncertainty-Aware Sleep Stage Classification

## Project Overview
This project focuses on classifying different sleep stages using EEG (Electroencephalogram) and EOG (Electrooculogram) signals with Machine Learning techniques. It also explores how reliable the model's predictions are when input signals are noisy, corrupted, or partially missing.

The model classifies sleep into five stages: Wake (W), N1, N2, N3, and REM.

##  Objectives
- Develop an ML-based sleep stage classification system.
- Extract meaningful features from EEG and EOG signals.
- Evaluate model performance under different signal conditions.
- Estimate prediction uncertainty and identify unreliable predictions.
- Improve reliability using confidence-based abstention and signal-quality checks.

## Dataset
- **Dataset:** Sleep-EDF Expanded
- **Recordings:** 197
- **Subjects:** 100
- **Signals:** EEG Fpz-Cz, EEG Pz-Oz, and EOG
- **Epoch Duration:** 30 seconds

##  Methodology
1. Data collection and preprocessing of EEG and EOG signals.
2. Band-pass filtering (0.5–30 Hz).
3. Feature extraction using Welch's Power Spectral Density.
4. Training and comparison of multiple machine learning algorithms.
5. Uncertainty estimation and confidence-based prediction.
6. Robustness testing with noisy signals, missing channels, and feature corruption.
7. Model evaluation using Macro-F1, accuracy, and other performance metrics.

##  Machine Learning Algorithms
- Random Forest
- LightGBM
- XGBoost
- Extra Trees
- Logistic Regression
- Multi-Layer Perceptron (MLP)
- HistGradientBoosting

## Tools & Technologies
- **Programming:** Python
- **Libraries:** NumPy, Pandas, SciPy, Scikit-learn
- **ML Algorithms:** Random Forest, LightGBM, XGBoost
- **Signal Processing:** MNE, PyEDFlib
- **Visualization:** Matplotlib
- **Platform:** Google Colab

## Key Results
- Achieved a test Macro-F1 score of **0.759** using temporal context features.
- Achieved an error-detection AUROC of **0.82** on clean data.
- Reduced prediction error from 23.2% to 15.8% by using confidence-based abstention.
- Improved performance when handling missing channels through random channel masking during training.
- Identified limitations of confidence estimation under severe signal noise.

## Key Learning Outcomes
- EEG and EOG signal processing.
- Feature extraction and machine learning model development.
- Model evaluation and performance optimization.
- Predictive uncertainty and confidence estimation.
- Robustness analysis under different input conditions.

## ⚠️ Disclaimer
This project is developed for academic and research purposes. It is a research prototype and is not intended for clinical diagnosis or medical decision-making.

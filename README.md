# Nurse Stress Prediction Using Wearable Devices

## Project Overview

This project leverages physiological signals from wearable devices to predict stress levels among nurses working in hospital environments. The dataset contains physiological data collected from nurses wearing smartwatches that monitored their heart rate, skin temperature, and electrodermal activity (EDA) while simultaneously reporting their stress levels.

## Objectives

- Evaluate various machine learning models to predict stress levels based on recorded physiological signals
- Identify the most relevant physiological indicators for stress detection
- Provide insights to improve the accuracy and reliability of stress detection via wearable technology

## Data Collection Context

**Study Period:** Data gathered over one week from 15 female nurses aged 30 to 55 years during regular hospital shifts

**Collection Phases:**
- Phase-I: April 15, 2020, to August 6, 2020
- Phase-II: October 8, 2020, to December 11, 2020

**Exclusion Criteria:** Pregnancy, heavy smoking, mental disorders, chronic or cardiovascular diseases

**Data Captured:**
- Physiological Variables: Electrodermal activity, Heart Rate, and skin temperature
- Survey Responses: Periodic smartphone-administered surveys capturing contributing factors to detected stress events
- Measurement Technologies: Empatica E4 for data collection, focusing on Galvanic Skin Response and Blood Volume Pulse (BVP) readings

## Features

The dataset includes the following features:
- **X, Y, Z**: Accelerometer data (3-axis movement)
- **EDA**: Electrodermal Activity (skin conductance)
- **HR**: Heart Rate
- **TEMP**: Skin Temperature
- **datetime**: Timestamp of measurements
- **label**: Stress level classification (0: Low, 1: Medium, 2: High)

## Data Processing Pipeline

1. **Data Loading and Exploration**
   - Load and examine the dataset structure
   - Handle missing values and data types
   - Remove duplicates

2. **Data Cleaning**
   - Outlier detection and removal using IQR and Z-score methods
   - Feature engineering (extracting time-based features)
   - Data normalization and scaling

3. **Exploratory Data Analysis**
   - Statistical analysis of physiological variables
   - Correlation analysis between features
   - ANOVA tests to assess significance of differences across stress levels
   - Visualization of data distributions and relationships

4. **Feature Engineering**
   - Time-based feature extraction (year, month, day, hour, minute, second)
   - Statistical feature creation
   - Feature selection using variance threshold and PCA

## Machine Learning Models

The project implements and compares multiple machine learning algorithms:

### Traditional Machine Learning
- **Logistic Regression**: Baseline linear model
- **Random Forest**: Ensemble method with feature importance analysis
- **Support Vector Machine (SVM)**: Kernel-based classification
- **Decision Tree**: Interpretable tree-based model

### Advanced Ensemble Methods
- **XGBoost**: Gradient boosting with regularization
- **LightGBM**: Light gradient boosting machine
- **Voting Classifier**: Ensemble of multiple models

### Deep Learning
- **LSTM Neural Network**: Sequential modeling for time-series data

## Model Evaluation

Models are evaluated using:
- **Accuracy**: Overall prediction accuracy
- **Precision**: True positive rate
- **Recall**: Sensitivity
- **F1-Score**: Harmonic mean of precision and recall
- **Confusion Matrix**: Detailed classification results

## Key Findings

- **Feature Importance**: Heart rate and EDA show strong correlation with stress levels
- **Model Performance**: Ensemble methods (Voting Classifier, XGBoost) achieve the best performance
- **Statistical Significance**: ANOVA tests confirm significant differences in physiological measures across stress levels

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd nurse-stress-prediction
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

## Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook nurse-stress-sensor.ipynb
```

2. Run the cells sequentially to:
   - Load and preprocess the data
   - Perform exploratory data analysis
   - Train and evaluate machine learning models
   - Generate visualizations and insights

## Requirements

- Python 3.7+
- Jupyter Notebook
- See `requirements.txt` for detailed package versions

## Project Structure

```
nurse-stress-prediction/
├── nurse-stress-sensor.ipynb    # Main analysis notebook
├── requirements.txt             # Python dependencies
├── README.md                    # Project documentation
├── data/                        # Data directory
└── notebooks/                   # Additional notebooks
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Data collection team and participating nurses
- Empatica for providing the E4 wearable devices
- Research institutions involved in the study

## Contact

For questions or contributions, please open an issue or contact the project maintainers. 
# HVAC Predictive Maintenance Using Machine Learning

## Project Overview

This project focuses on predicting potential HVAC (Heating, Ventilation, and Air Conditioning) equipment failures using Machine Learning techniques.

A synthetic dataset containing HVAC sensor readings is created and analyzed to identify patterns associated with equipment failures. The project applies data preprocessing, exploratory data analysis (EDA), feature engineering, and classification algorithms to predict whether an HVAC system is operating normally or experiencing a potential failure.

## Project Objectives

- Create a synthetic HVAC sensor dataset.
- Understand and explore the dataset using Python.
- Handle missing values and outliers.
- Perform Exploratory Data Analysis (EDA).
- Apply feature engineering and feature scaling.
- Train and compare Machine Learning models.
- Evaluate model performance using classification metrics.

## Dataset Information

The project uses a synthetic dataset containing 1,000 records.

The dataset includes the following features:

| Feature | Description |
|---|---|
| Temperature | HVAC operating temperature |
| Humidity | Humidity level |
| Vibration | Equipment vibration level |
| Pressure | System pressure |
| Energy_Consumption | Energy consumed |
| Runtime_Hours | Total operating hours |
| Failure | Target variable (0 = Normal, 1 = Failure) |

**Note:** Failure labels are generated using predefined sensor conditions. This is a synthetic dataset created for educational purposes, not real HVAC maintenance data.

## Technologies and Libraries Used

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## Project Workflow

### 1. Dataset Creation
Created a synthetic HVAC dataset containing 1,000 records with sensor readings and failure labels.

### 2. Data Understanding
- Checked dataset dimensions.
- Examined column names and data types.
- Generated summary statistics.
- Identified missing values and duplicate records.
- Analyzed normal and failure records.

### 3. Data Preprocessing
- Handled missing values using median imputation.
- Detected and capped outliers using the IQR method.
- Split the dataset into training and testing sets (80:20).

### 4. Exploratory Data Analysis (EDA)
Used visualizations to understand:
- Normal vs. failure records.
- Temperature distribution by failure status.
- Vibration distribution by failure status.
- Correlation between numerical features.

### 5. Feature Engineering
Created two additional features:
- High_Temperature
- High_Vibration

### 6. Feature Scaling
Applied StandardScaler to prepare the features for Logistic Regression.

### 7. Model Development
Implemented two classification algorithms:

- Logistic Regression
- Random Forest Classifier

### 8. Model Evaluation
Compared both models using:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Also visualized confusion matrices and ROC curves.

## Model Comparison Results

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 92.5% | 89.2% | 92.5% | 90.8% | 98.1% |
| Random Forest | 100% | 100% | 100% | 100% | 100% |

**Observation:** Random Forest achieved the highest scores on the test dataset.

However, these results should not be interpreted as real-world predictive performance because the dataset is synthetic and the failure labels are generated using predefined rules.

## Project Files

- `HVAC_Predictive_Maintenance.ipynb` – Main Jupyter Notebook containing the complete project.
- `hvac_dataset.csv` – Original synthetic HVAC dataset.
- `hvac_cleaned_dataset.csv` – Preprocessed dataset with engineered features.
- `hvac_model_comparison.csv` – Model evaluation results.

## How to Run the Project

1. Clone this repository:

   ```bash
   git clone https://github.com/YOUR-USERNAME/HVAC-Predictive-Maintenance-ML.git
   ```

2. Navigate to the project folder:

   ```bash
   cd HVAC-Predictive-Maintenance-ML
   ```

3. Install the required libraries:

   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn jupyter
   ```

4. Start Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

5. Open `HVAC_Predictive_Maintenance.ipynb` and run the cells in order.

## Future Improvements

- Use real-world HVAC sensor and maintenance datasets.
- Experiment with additional classification algorithms.
- Perform hyperparameter tuning.
- Improve model generalization using real maintenance records.

## Conclusion

This project demonstrates a basic Machine Learning workflow for HVAC predictive maintenance, covering synthetic data generation, data preprocessing, exploratory data analysis, feature engineering, model training, and evaluation.

It provides practical experience in applying Python and Machine Learning techniques to an equipment maintenance problem.

**Project Type:** Machine Learning Mini Project  
**Dataset:** Synthetic HVAC Sensor Data  
**Models:** Logistic Regression and Random Forest

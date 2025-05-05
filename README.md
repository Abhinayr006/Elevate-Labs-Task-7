# Breast Cancer Wisconsin Dataset Analysis

## Overview
This project uses the Breast Cancer Wisconsin dataset to classify tumors as malignant (M) or benign (B) using a Support Vector Machine (SVM) model. The dataset includes features derived from digitized images of fine needle aspirates (FNA) of breast masses.

## Dataset
- **File**: `Breast_Cancer_Wisconsin.csv`
- **Source**: Loaded from the path specified in the notebook.
- **Description**: Contains 569 entries and 33 columns, including an ID, diagnosis (M/B), and 30 numerical features (e.g., radius_mean, texture_mean). The 'Unnamed: 32' column is entirely NaN and removed during preprocessing.

## Requirements
- Python 3.x
- Libraries:
  - pandas
  - numpy
  - scikit-learn

## Files
- **ElevateLabsTask_7.ipynb**: Jupyter Notebook with the analysis and model training code.
- **Breast_Cancer_Wisconsin.csv**: The dataset used for this project.
- **README.md**: This file, providing an overview of the project.

## Steps
1. **Data Loading and Preprocessing**:
   - Load the dataset using pandas.
   - Remove irrelevant columns ('id', 'Unnamed: 32').
   - Encode the 'diagnosis' column (M=1, B=0).
   - Scale features using StandardScaler.

2. **Model Training**:
   - Split data into training and testing sets.
   - Perform hyperparameter tuning (C and gamma) for an SVM with RBF kernel using GridSearchCV.
   - Best parameters: `C=1`, `gamma='scale'`.
   - Best cross-validation score: ~0.9736.

3. **Evaluation**:
   - Evaluate the best model using 5-fold cross-validation on scaled data.
   - Mean cross-validation accuracy: ~0.9736.

## Usage
1. Place `Breast_Cancer_Wisconsin.csv` in the directory specified in the notebook.
2. Install required libraries:

3. Run the `ElevateLabsTask_7.ipynb` notebook in Jupyter Notebook or JupyterLab.

## Results
The tuned SVM model achieves a cross-validation accuracy of ~97.36%, demonstrating strong performance in classifying breast cancer diagnoses.

## Notes
- Update the dataset path in the notebook (`/content/drive/MyDrive/Colab Notebooks/7/Breast_Cancer_Wisconsin.csv`) to match your local setup.
- The notebook assumes the dataset is clean, except for the 'Unnamed: 32' column, which is handled during preprocessing.

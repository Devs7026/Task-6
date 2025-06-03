
# K-Nearest Neighbors (KNN) Classification 

## Overview

This project demonstrates how to implement the K-Nearest Neighbors (KNN) algorithm for classification tasks using the classic Iris dataset. The workflow includes data normalization, model training and evaluation for multiple values of K, and visualization of decision boundaries.

## Tools Used

- **Python 3**
- **pandas** (for data manipulation)
- **scikit-learn** (for KNN, preprocessing, and evaluation)
- **matplotlib** (for visualization)
- **numpy** (for numerical operations)

## Steps to Solve the Task

### 1. Load and Prepare the Data

- Read the Iris dataset from `Iris.csv` using pandas.
- Map the `species` column to numeric labels for classification.

### 2. Normalize Features

- Use `StandardScaler` from scikit-learn to standardize features.
- This step ensures all features contribute equally to distance calculations in KNN.

### 3. Split the Dataset

- Split the data into training and testing sets (70% train, 30% test) using `train_test_split`, stratified by class.

### 4. Train and Evaluate KNN

- Train `KNeighborsClassifier` models for various values of K (e.g., 1, 3, 5, 7).
- For each K:
  - Fit the model on the training data.
  - Predict on the test data.
  - Evaluate using accuracy score and confusion matrix.

### 5. Visualize Decision Boundaries

- For visualization, use only the first two features (sepal length and sepal width).
- Plot the decision boundaries for a chosen K (e.g., K=3) using `matplotlib`.
- Overlay the training data points colored by class.

## Example Output

```
K = 1: Accuracy = 0.9778
Confusion Matrix:
[[16  0  0]
 [ 0 14  1]
 [ 0  0 14]]

K = 3: Accuracy = 1.0000
Confusion Matrix:
[[16  0  0]
 [ 0 15  0]
 [ 0  0 14]]
...
```
- A plot will display the decision boundaries for the first two features.

## Notes

- The code automatically encodes class labels and normalizes features.


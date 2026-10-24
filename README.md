# SC5002-Lab-Assignment1

## 1. Project Overview

This project explores the application of Linear Regression and Ridge Regression to predict median house values using the California Housing dataset. It investigates how different regularization strengths affect model performance.

## 2. Dataset

The California Housing dataset is loaded using Scikit-learn. A random sample of 1,000 records is selected with `random_state=42`.

The dataset contains eight input features, including median income, house age, average rooms, average bedrooms, population, average occupancy, latitude, and longitude.

The target variable is `MedHouseVal`, representing the median house value.

## 3. Methodology

- StandardScaler is used to standardize numerical features.
- The dataset is divided into 80% training data and 20% testing data.
- Linear Regression is used as the baseline model.
- Ridge Regression is evaluated with alpha values of 0.1, 10, and 1000.
- Model performance is evaluated using mean 5-fold cross-validation R² scores on the training subset.

## 4. Experimental Results

| Model | Alpha | Mean 5-Fold R² |
|---|---|---|
| Linear Regression | - | 0.6457 |
| Ridge Regression | 0.1 | 0.6457 |
| Ridge Regression | 10 | 0.6443 |
| Ridge Regression | 1000 | 0.3574 |

## 5. How to Run

1. Download the `SC5002_Lab_Assignment1.ipynb` file from this repository.
2. Open Google Colab.
3. Upload the notebook.
4. Run all code cells sequentially.
5. View the dataset, model evaluation scores, and performance comparison chart.

The notebook uses Python, NumPy, Pandas, Matplotlib, and Scikit-learn.

## 6. Conclusion

The results show that Linear Regression and Ridge Regression with low regularization strength achieve similar performance. However, increasing alpha to 1000 significantly reduces the R² score, suggesting that excessive regularization can cause underfitting. Therefore, selecting an appropriate regularization strength is important for achieving good predictive performance.

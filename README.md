# SUV Purchase Prediction

A machine learning project that predicts whether a customer will purchase an SUV based on their **age** and **estimated salary**, using logistic regression.

## Overview

This project applies a binary classification model to a customer dataset to determine the likelihood of an SUV purchase. It was built while applying concepts from Andrew Ng's *Supervised Machine Learning: Regression and Classification* course (Coursera).

## Dataset

The dataset (`suv_data.csv`) contains the following features:

| Column | Description |
|---|---|
| User ID | Unique customer identifier |
| Gender | Customer gender |
| Age | Customer age |
| EstimatedSalary | Customer's estimated annual salary |
| Purchased | Target variable (1 = purchased, 0 = did not purchase) |

Only `Age` and `EstimatedSalary` were used as input features for the model.

## Approach

1. **Data loading & exploration** — loaded the dataset with pandas and inspected it with `head()`.
2. **Train/test split** — split the data using `train_test_split` (75% train, 25% test).
3. **Model training** — trained a `LogisticRegression` model from scikit-learn on the raw features.
4. **Feature scaling** — applied `StandardScaler` to standardize `Age` and `EstimatedSalary`, then retrained the model on the scaled data.
5. **Evaluation** — assessed performance using accuracy score, a confusion matrix, and a classification report (precision, recall, F1-score).

## Results

- **Accuracy:** 90%
- **Confusion Matrix:**

  |  | Predicted: No | Predicted: Yes |
  |---|---|---|
  | **Actual: No** | 64 | 5 |
  | **Actual: Yes** | 5 | 26 |

- **Classification Report:**

  | Class | Precision | Recall | F1-score |
  |---|---|---|---|
  | 0 (No purchase) | 0.93 | 0.93 | 0.93 |
  | 1 (Purchase) | 0.84 | 0.84 | 0.84 |

## Tools & Libraries

- Python
- pandas, NumPy
- scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

## How to Run

1. Clone this repository
2. Install dependencies: `pip install pandas numpy scikit-learn matplotlib seaborn`
3. Open `suv_prediction.ipynb` in Jupyter Notebook
4. Run all cells in order

## Author

**SanjayKumar S S**
B.Tech Electronics and Communication Engineering, Birla Institute of Technology, Mesra

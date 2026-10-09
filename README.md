# Bank Marketing Data Analysis and Regression Models

## 📌 Project Overview

This project focuses on analyzing bank marketing data and applying different regression techniques to predict the number of previous customer contacts (`previous`) using campaign-related features. The project explores and compares Simple Linear Regression, Multiple Linear Regression, and Gradient Boosting Regression.

## 🎯 Objectives

* Explore and understand the bank marketing dataset.
* Perform data inspection and descriptive statistical analysis.
* Build and evaluate different regression models.
* Compare model performance using R² scores and error metrics.
* Visualize actual versus predicted values to understand model performance.

## 📂 Dataset

The dataset contains **11,162 records and 17 columns**, including customer demographics, financial information, campaign details, and the target variable.

Key features include:

* `age` – Customer age
* `job` – Type of job
* `marital` – Marital status
* `education` – Education level
* `balance` – Customer account balance
* `campaign` – Number of contacts during the current campaign
* `pdays` – Days since the customer was previously contacted
* `previous` – Number of contacts performed before the current campaign
* `deposit` – Whether the customer subscribed to a term deposit

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook

## 📊 Methodology

### 1. Data Exploration

* Inspected dataset structure and data types.
* Checked for missing values.
* Generated descriptive statistics.

### 2. Simple Linear Regression

Used `campaign` as the independent variable to predict `previous`.

### 3. Multiple Linear Regression

Used `campaign` and `pdays` as independent variables to predict `previous`.

### 4. Gradient Boosting Regression

Applied `GradientBoostingRegressor` using `campaign` and `pdays`, with 100 estimators, a learning rate of 0.1, and a maximum tree depth of 3.

### 5. Model Evaluation

Compared the models using training and test R² scores. The Gradient Boosting model was also evaluated using Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).

## 📈 Results

| Model                        | Training R² | Test R² |
| ---------------------------- | ----------: | ------: |
| Simple Linear Regression     |      0.0030 | -0.0006 |
| Multiple Linear Regression   |      0.2562 |  0.2581 |
| Gradient Boosting Regression |      0.5378 |  0.3705 |

**Gradient Boosting Regression performed best** among the three models, achieving a test R² score of approximately 0.37.

Its additional evaluation metrics were:

* **MAE:** 0.61
* **RMSE:** 2.06

These results suggest that Gradient Boosting captures more of the relationship in the selected features than the linear regression models. However, its predictive performance remains limited.

## 📉 Visualizations

The notebook includes:

* Actual versus predicted value plots.
* Regression prediction visualizations.
* A bar chart comparing training and test R² scores across models.

## 🚀 How to Run the Project

1. Clone the repository:

   ```bash
   git clone <your-repository-url>
   ```

2. Navigate to the project directory:

   ```bash
   cd <your-project-folder>
   ```

3. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib scikit-learn jupyter
   ```

4. Place the `bank.csv` dataset in the appropriate project directory and update the file path in the notebook if necessary.

5. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

6. Open `Data Analysis (5).ipynb` and run the cells.

## 💡 Key Learnings

* Data exploration and descriptive statistics using Pandas.
* Implementing regression models with Scikit-learn.
* Evaluating models using R², MAE, and RMSE.
* Visualizing model predictions and comparing performance.
* Understanding the limitations of simple and multiple linear regression compared with an ensemble method.

## 🔮 Future Improvements

* Perform feature engineering and categorical variable encoding.
* Explore additional relevant predictors.
* Tune model hyperparameters using cross-validation.
* Compare additional regression algorithms.
* Investigate whether predicting `previous` is the most useful objective for the bank marketing dataset.

## 👤 Author

**Swagatika Satapathy**

Feel free to connect with me on GitHub and share feedback or suggestions.

![target mktg](https://github.com/user-attachments/assets/50df9f44-6618-4c5b-956c-a01f2d5b4cc4)
# Direct Marketer Logistic Regression Analysis

## Overview

This repository contains a detailed analysis using Logistic Regression to predict good customers for a direct marketing campaign. The analysis involves data preprocessing, model building, and evaluation using Python libraries like Pandas, Statsmodels, and Scikit-learn. The primary objective is to identify customers who are more likely to spend above average and thus should be targeted in marketing efforts.

## Table of Contents

1. [Overview](#overview)
2. [Project Structure](#project-structure)
3. [Prerequisites](#prerequisites)
4. [Dataset](#dataset)
5. [Analysis Steps](#analysis-steps)
   - [1. Data Loading](#1-data-loading)
   - [2. Data Preprocessing](#2-data-preprocessing)
   - [3. Feature Engineering](#3-feature-engineering)
   - [4. Model Building](#4-model-building)
   - [5. Model Evaluation](#5-model-evaluation)
   - [6. Gain Chart and Customer Targeting](#6-gain-chart-and-customer-targeting)
6. [Results](#results)
7. [How to Use](#how-to-use)
8. [License](#license)
9. [Acknowledgments](#acknowledgments)

## Project Structure

The repository is structured as follows:

```
direct-marketer-logistic-regression/
│
├── data/
│   └── dm.csv                             # Raw dataset used in the analysis
│
├── notebooks/
│   └── Logistic_Regression_Direct_Marketer.ipynb  # Jupyter Notebook containing the analysis
│
├── README.md                              # Project documentation
├── LICENSE                                # License for the project
└── .gitignore                             # Git ignore file
```

## Prerequisites

Before running the notebook, ensure you have the following installed:

- **Python 3.x**
- **Jupyter Notebook**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Statsmodels**
- **Scikit-learn**

You can install the required Python packages using pip:

```bash
pip install pandas numpy matplotlib statsmodels scikit-learn
```

## Dataset

The dataset used in this analysis, `dm.csv`, contains customer information relevant to direct marketing, including demographic details, purchase history, and spending behavior. The target variable (`target`) indicates whether a customer is considered "good" (likely to spend above average) or "bad" (likely to spend below average).

## Analysis Steps

### 1. Data Loading
The dataset is loaded using Pandas, with handling for missing values and initial exploration of the data structure.

### 2. Data Preprocessing
The data is cleaned and prepared for analysis, including handling missing values in the `History` variable by creating a new label `NewCust` for customers without prior history.

### 3. Feature Engineering
A new binary target variable is created based on whether a customer's spending exceeds the average (`AmountSpent`). This variable is then used in the logistic regression model. The dataset is split into training and test sets for model validation.

### 4. Model Building
A Logistic Regression model is built using Statsmodels’ `glm` function. The model includes both continuous and categorical predictors (such as `Age`, `Gender`, `Salary`, etc.). Dummy variables are created for categorical features, particularly for significant levels in `History`.

### 5. Model Evaluation
The model is evaluated using metrics like the confusion matrix, ROC curve, and AUC score. These metrics help assess the model’s performance in distinguishing between good and bad customers.

### 6. Gain Chart and Customer Targeting
A Gain Chart is used to determine the most effective probability thresholds for targeting customers. This allows the marketer to focus on customers with the highest likelihood of being good customers.

## Results

The logistic regression model successfully identifies key predictors of customer behavior, such as `Salary`, `Catalogs`, and `History`. The model’s performance is validated using AUC (Area Under the ROC Curve), which shows a high score of 95%, indicating the model is highly effective. The Gain Chart analysis further refines the targeting strategy by identifying customers most likely to be profitable.

## How to Use

1. **Clone this repository**:
    ```bash
    git clone https://github.com/yourusername/Direct_MKTG_Campaign_Target_Prediction.git
    cd Direct_MKTG_Campaign_Target_Prediction
    ```

2. **Run the Jupyter Notebook**:
    ```bash
    jupyter notebook notebooks/Logistic_Regression_Direct_Marketer.ipynb
    ```

3. **Follow the steps in the notebook** to reproduce the analysis and gain insights into customer targeting using logistic regression.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- The dataset used in this analysis was provided for educational purposes.
- Special thanks to the contributors of open-source libraries like Pandas, NumPy, Statsmodels, and Scikit-learn that made this analysis possible.

---

This README should serve as a comprehensive guide to understanding and running the logistic regression analysis for direct marketing. Feel free to customize it further based on your specific needs.
![image](https://github.com/user-attachments/assets/8e3a84c0-cbd5-4650-8baa-ca39bf426a68)

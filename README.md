# Linear Regression and Model Selection Project

## Project Overview

This project demonstrates fundamental concepts in linear regression, variable selection methods, and advanced regression techniques like Ridge, Lasso, and ElasticNet. The work emphasizes data preprocessing, model evaluation, and performance comparison across different regression models. It is based on exercises from the **SD-TSIA204 Telecom Paris course (2023/2024)**.

- The project is implemented entirely in a Jupyter notebook (`.ipynb` file), making it easy to follow and execute.

## Theoretical Background

### Linear Regression

Linear regression is a fundamental statistical method used to model the relationship between a dependent variable and one or more independent variables. The model assumes that the relationship between the variables is linear and can be expressed in the form:

$$ y = \beta_0 + \beta_1 X_1 + \beta_2 X_2 + ... + \beta_n X_n + \epsilon $$

Where:
- $ y $ is the dependent variable,
- $ X_1, X_2, ..., X_n $ are the independent variables,
- $ \beta_0, \beta_1, ..., \beta_n $ are the coefficients (parameters),
- $ \epsilon $ represents the error term.

The objective of linear regression is to estimate the coefficients $ \beta $ that minimize the difference between the predicted and actual values of the dependent variable, usually using the method of Ordinary Least Squares (OLS).

### Regularization Techniques

**Ridge Regression** introduces a penalty to the loss function to prevent overfitting by shrinking the coefficients. This method is particularly useful when there is multicollinearity among the independent variables. The penalty is proportional to the sum of the squares of the coefficients:

$$ \text{Loss Function} = \sum (y - \hat{y})^2 + \lambda \sum \beta_j^2 $$

**Lasso Regression** adds a penalty equal to the absolute value of the coefficients, which encourages sparsity in the model, potentially setting some coefficients to zero, thus performing feature selection:

$$ \text{Loss Function} = \sum (y - \hat{y})^2 + \lambda \sum |\beta_j| $$

**ElasticNet** is a hybrid method that combines the penalties of both Ridge and Lasso, balancing the tradeoff between shrinking the coefficients and inducing sparsity:

$$ \text{Loss Function} = \sum (y - \hat{y})^2 + \lambda_1 \sum \beta_j^2 + \lambda_2 \sum |\beta_j| $$

### Principal Component Regression (PCR)

PCR is a dimensionality reduction technique that applies Principal Component Analysis (PCA) before fitting a linear model. It helps to address multicollinearity by reducing the data into a smaller set of uncorrelated components that capture the most variance. The goal is to improve model performance by projecting the original data into a lower-dimensional space and performing regression on this transformed data.

# Linear Regression and Model Selection Project

## Project Overview

This project demonstrates fundamental concepts in linear regression, variable selection methods, and advanced regression techniques like Ridge, Lasso, and ElasticNet. The work emphasizes data preprocessing, model evaluation, and performance comparison across different regression models. It is based on exercises from the **SD-TSIA204 Telecom Paris course (2023/2024)**.

## Key Skills Demonstrated

- **Data Preprocessing**: Used `sklearn` to split datasets into training and testing sets, applied standardization techniques using `StandardScaler`, and ensured proper handling of data.
- **Linear Regression**: Implemented Ordinary Least Squares (OLS) regression manually and compared results against `sklearn`'s implementations, including calculating the Mean Squared Error (MSE) and R² scores.
- **Variable Selection**: Developed a forward selection algorithm using p-values from hypothesis tests, iteratively selecting the most relevant features.
- **Advanced Regression Techniques**:
  - **Ridge Regression**: Experimented with different penalty values and visualized the evolution of coefficients and R² scores.
  - **Lasso Regression**: Ran the same procedure as Ridge but optimized for sparsity in the coefficients.
  - **ElasticNet**: Combined Ridge and Lasso regularization terms for a balanced tradeoff between coefficient shrinkage and sparsity.
- **Principal Component Regression (PCR)**: Applied PCA to reduce dimensionality, used singular value decomposition (SVD) for covariance analysis, and fit regression models on reduced data.

## Project Structure

- **Data Preprocessing**: Splitting the data, standardization using `StandardScaler`.
- **Linear Regression Implementation**: Code to estimate coefficients, calculate confidence intervals, and compare OLS models.
- **Forward Variable Selection**: Python function that iteratively selects features with the smallest p-values and halts when the p-value exceeds 0.05.
- **Advanced Regularization Methods**:
  - Ridge, Lasso, and ElasticNet, each with 30 different penalty parameters, visualized in terms of coefficient paths and performance metrics.
- **Principal Component Analysis**:
  - Heatmap of the covariance matrix and plots showing the variance explained by principal components.
  - OLS models fitted on reduced data and score evolution.

## Notable Results

- **Model Comparisons**: Provided a detailed comparison of training and testing errors across OLS, Ridge, Lasso, ElasticNet, and PCR. Highlighted the strengths of each model in various contexts.
- **Data Visualization**: Extensive use of plots to explain the evolution of coefficients, R² scores, and principal components.

## Lessons Learned

- Gained hands-on experience in implementing linear regression from scratch and understanding the tradeoffs between different regression techniques.
- Learned the importance of feature selection in improving model performance and reducing overfitting.
- Explored the strengths of regularization techniques like Ridge and Lasso for handling multicollinearity and selecting sparse models.

## Future Work

- Explore more advanced techniques such as cross-validation for hyperparameter tuning.
- Apply similar regression techniques to larger datasets and real-world problems.


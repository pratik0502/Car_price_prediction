# Car Price Prediction Project

This project aims to predict car prices based on various features using regression modeling. It involves data analysis, outlier treatment, and the application of different regression algorithms. The dataset used in this project is sourced from the 'CarPrice.csv' file.

## Project Steps

1. **Data Loading and Exploration:** The dataset is loaded into a Pandas DataFrame and an initial exploration of the data is performed. This includes checking the data structure, identifying missing values, and understanding the distribution of categorical and numerical variables.

2. **Data Preprocessing:** The dataset undergoes preprocessing steps, such as outlier treatment using Tukey's fences method and imputation of missing values using K-Nearest Neighbors (KNN) imputer. Categorical variables are encoded using one-hot encoding and ordinal encoding.

3. **Modeling:** The preprocessed data is split into training and testing sets. A linear regression model is trained on the training set and evaluated using the R-squared score. Additionally, other regression algorithms like Stochastic Gradient Descent, Ridge regression, Lasso regression, and Elastic Net are applied and their performances are evaluated.

4. **Ensemble Methods:** Ensemble methods are explored using a VotingRegressor with different base estimators, including Decision Tree Regressor, Random Forest Regressor, K-Nearest Neighbors Regressor, and Linear Regression. Cross-validation is used to assess the performance of the ensemble models.

5. **Optimizing VotingRegressor:** A loop is implemented to find the optimal weights for the VotingRegressor by iterating through different weight combinations assigned to each base estimator. The performance of the ensemble models with varying weights is evaluated.

6. **Conclusion and Results:** The project concludes by summarizing the outcomes and results of different regression algorithms and the ensemble methods. The performance of each model is assessed based on metrics such as R-squared score. The findings and insights gained from the project are documented.

## Requirements and Libraries

The following libraries are required to run the project:

- pandas
- numpy
- matplotlib.pyplot
- seaborn
- warnings
- scikit-learn

## Usage

1. Clone the repository to your local machine.
2. Install the required libraries mentioned above.
3. Run the Jupyter Notebook file `CarPrice_Prediction.ipynb` to execute the project.
4. Follow the step-by-step instructions provided in the notebook to perform the data analysis, outlier treatment, and regression modeling.

Note: Make sure to place the `CarPrice.csv` file in the same directory as the Jupyter Notebook file.

## Conclusion 
The project achieves a regression model for predicting car prices with an accuracy of 89%. The ensemble models show improved performance compared to individual regression algorithms, with the VotingRegressor achieving the highest accuracy of 89%. The weights assigned to each base estimator in the VotingRegressor are as follows: 1 for Decision Tree Regressor, 2 for Random Forest Regressor, 1 for K-Nearest Neighbors Regressor, and 1 for Linear Regression.

During the evaluation of individual regression algorithms, the Decision Tree Regressor achieved an accuracy of 74%, the Random Forest Regressor achieved 89%, the K-Nearest Neighbors Regressor achieved 79%, and the Linear Regression model achieved 82%.

The VotingRegressor, which combines the predictions of multiple base estimators, outperformed the individual algorithms by achieving an accuracy of 89%. This indicates that the ensemble model benefits from the diverse perspectives and strengths of the individual algorithms, resulting in more accurate predictions.

Overall, the project demonstrates the effectiveness of ensemble methods, particularly the VotingRegressor, in improving the accuracy of car price prediction compared to using individual regression algorithms alone. By combining the strengths of different models, we can achieve higher prediction accuracy and make more reliable decisions in the automotive industry.

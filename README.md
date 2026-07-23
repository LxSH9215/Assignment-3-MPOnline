# Salary Prediction using Polynomial Regression (AI-ML Assignment - 3)

## Objective
To develop a Polynomial Regression model capable of estimating employee salaries based on their position level, addressing the non-linear relationship present in the dataset.

## Dataset Link
[Position Salaries Dataset on Kaggle](https://www.kaggle.com/datasets/akram24/position-salaries)

## Libraries Used
* **Pandas:** For data loading and initial dataset exploration.
* **NumPy:** For numerical operations and generating grid axes for plotting.
* **Matplotlib:** For visualizing the data points and the regression curve.
* **Scikit-learn:** For data splitting, polynomial feature transformation, model training, and performance evaluation.

## Methodology
1. **Data Understanding & Preprocessing:** The dataset was loaded and checked for missing values. The 'Level' column was isolated as the input feature (X), and 'Salary' as the target variable (y). The data was split into an 80% training set and a 20% testing set.
2. **Model Development:** The input features were transformed using `PolynomialFeatures` to a degree of 5 to best capture the exponential trend. A `LinearRegression` model was then trained on these transformed polynomial features.
3. **Evaluation:** The model was tested on the 20% holdout set, and its performance was measured using MAE, MSE, and R-squared Score. A visualization was created to map the polynomial curve against the original scatter plot.

## Results
* **Mean Absolute Error (MAE):** 13037.79
* **Mean Squared Error (MSE):** 250686067.95
* **R-squared Score:** 0.9950

The resulting plot demonstrated that the 5th-degree polynomial curve provided a near-perfect fit for the actual salary data across all position levels.

## Conclusion
The analysis reveals that employee salaries increase exponentially as the position level rises. By implementing a Polynomial Regression model (Degree = 5), we successfully captured the non-linear relationship inherent in the dataset. While linear models assume a straight-line relationship, polynomial models introduce higher-degree terms to map curves. The primary advantage of Polynomial Regression for this dataset is its flexibility to accurately track steep salary hikes for senior roles, yielding highly accurate predictions and a near-perfect R-squared score.

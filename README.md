# House-price-prediction-using-Linear-Regression
ML Python Project

# Graph 

![](https://github.com/developer-venish/House-price-prediction-using-Linear-Regression/blob/main/graph.png)

# Prediction 

![](https://github.com/developer-venish/House-price-prediction-using-Linear-Regression/blob/main/predict.png)


---------------------------------------------------------------------------------------

Note :- All the code in this project has been tested and run successfully in Google Colab. I encourage you to try running it in Colab for the best experience and to ensure smooth execution. Happy coding!

---------------------------------------------------------------------------------------


The given code performs linear regression to predict house prices based on the area. Here's a step-by-step explanation:

1. Import the necessary libraries:
   - `pandas` for data manipulation and analysis.
   - `LinearRegression` from `sklearn.linear_model` for linear regression modeling.
   - `matplotlib.pyplot` for data visualization.
   - `files` from `google.colab` to upload files in Google Colab.

2. Upload the `house-prices.csv` file using the `files.upload()` function.

3. Read the CSV file into a pandas DataFrame using `pd.read_csv()` and store it in the `dataset` variable.

4. Print the shape of the dataset using `dataset.shape` to see the number of rows and columns in the dataset.

5. Print the first 5 rows of the dataset using `dataset.head(5)` to get a preview of the data.

6. Set the x-axis label as "Area" and the y-axis label as "Price" using `plt.xlabel()` and `plt.ylabel()`.

7. Create a scatter plot of the data points using `plt.scatter()` with `dataset.area` as the x-coordinate and `dataset.price` as the y-coordinate. The points will be displayed in blue and marked with asterisks.

8. Drop the "price" column from the dataset to obtain the feature matrix `X` using `dataset.drop('price', axis='columns')`.

9. Store the "price" column as the target variable `Y` using `dataset.price`.

10. Create an instance of the `LinearRegression` model called `model`.

11. Fit the linear regression model to the data using `model.fit(X, Y)`.

12. Set the value of `x` to the area for which you want to predict the house price.

13. Create a nested list `LandAreainSqFt` with the value of `x` as the input for prediction.

14. Use the trained model to predict the price for the given area using `model.predict(LandAreainSqFt)`. The predicted result is stored in `PredictedmodelResult`.

15. Print the predicted result.

16. Get the slope coefficients (weights) of the linear regression model using `model.coef_` and store it in `m`.

17. Print the slope coefficients.

18. Get the intercept of the linear regression model using `model.intercept_` and store it in `b`.

19. Print the intercept.

20. Calculate the predicted price `y` using the equation `y = m*x + b`, where `m` is the slope coefficient and `b` is the intercept.

21. Print the final predicted price. The format method is used to insert `x` and `y[0]` into the string to display the values.

Note: The code assumes that the dataset contains an "area" column for the independent variable and a "price" column for the dependent variable. Make sure the dataset is structured accordingly.
---------------------------------------------------------------------------------------

Linear regression is a statistical modeling technique used to understand the relationship between a dependent variable and one or more independent variables. It assumes a linear relationship between the variables, meaning that a change in the independent variable(s) is expected to cause a proportional change in the dependent variable.

In linear regression, the goal is to find the best-fit line that minimizes the sum of the squared differences between the predicted values and the actual values of the dependent variable. This line is determined by estimating the coefficients (slope and intercept) that define the relationship between the variables.

The basic form of a linear regression equation with one independent variable is:

y = mx + b

Where:
- y is the dependent variable
- x is the independent variable
- m is the slope or coefficient of the independent variable
- b is the intercept or constant term

The coefficient (m) represents the change in the dependent variable for a one-unit change in the independent variable, while the intercept (b) represents the value of the dependent variable when the independent variable is zero.

Linear regression can be used for both simple regression (one independent variable) and multiple regression (more than one independent variable). It is widely used in various fields for prediction, forecasting, and understanding the relationship between variables.

---------------------------------------------------------------------------------------

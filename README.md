# WID2002 Group Assignment

## Overview

This is our group assignment for Computing Mathematics II where we were tasked to solve real world problems using mathematics principles. Our group decided to calculate how long it could take for a fresh graduate to save 10% savings of the price of a terrace house as down payment. It hence only focuses on this single criteria of purchasing a house.

The assumptions we made for this project were:
| Criteria | Value |
|----------|-------|
|Average Fresh Graduate Salary|RM2424 (Based on national reports)|
|Average Rate of Annual Salary Increase|7.50% (Calculated from yearly trend)|

Datasets used in this project were taken from:

1. Terrace House Prices
   - https://www.data.gov.my/data/ms_MY/dataset/harga-rumah-teres-mengikut-negeri

## Techniques

### Technique 1 : The Original Assignment

The techniques used to solve this problem comprised of the usage of statistics and matrix algebra. Given the nature of the dataset, we first calculated the yearly average by calculating the average over 4 quarters for each state.

When plotting these values, we noticed a linear pattern and hence implemented a matrix least square method to obtain a least square regression line. This enabled us to perform a linear regression to obtain a model of house prices based on the number of years since 2009. We then repeated this step for all of the states and ended up with unique least square lines for each state.

With the ability to predict the price of a terrace house, we then applied geometric progression to calculate two possible situations:

1. The number of years to afford down payment given a fixed montly percent savings (eg. 10%)
2. The monthly percent savings required given the number of years is fixed (eg. the graduate wants to purchase a house after 5 years of work)

This implementation is seen in the `analysis.ipnyb` notebook.

### Technique 2 : Linear Regression Using Gradient Descent

Post-assignment, I decided to test out an implementation of gradient descent to obtain the parameters of the linear model. This implementation is seen in the `linear_regression_test.ipynb` notebook found in the LinearRegression folder.

This is an incomplete implementation of the original project and is mainly a test of the first part of the assignment where we created a model for house price prediction.

## References

1. Least-Squares Method

   - https://textbooks.math.gatech.edu/ila/least-squares.html
   - https://www.youtube.com/watch?v=RlQBEhLhM8Y
   - https://www.youtube.com/watch?v=Z0wELiinNVQ

2. Working with Unknown Equations with Sympy

   - https://docs.sympy.org/latest/tutorial/basic_operations.html

3. Finding and illustrating the intersection of two graphs with shapely and matplotlib

   - https://stackoverflow.com/questions/28766692/intersection-of-two-graphs-in-python-find-the-x-value
   - https://www.youtube.com/watch?v=heGBqav2TbU

4. Gradient Descent for Linear Regression using Python
   - https://towardsdatascience.com/linear-regression-using-gradient-descent-97a6c8700931
   - My implementation is also based on Andrew Ng's Machine Learning course and hence the difference in the derivative equations used.

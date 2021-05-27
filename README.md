# WID2002 Group Assignment

## Overview

Our assignment aims to calculate how long it could take for a fresh graduate to save 10% savings of the price of a terrace house as downpayment. It hence only focuses on one of the criterias to purchase a house.

The assumptions we made for this project were that:
| Criteria | Value |
|----------|-------|
|Average Fresh Graduate Salary|RM2424|
|Average Rate of Annual Salary Increase|7.05% (Calculated from yearly trend)|

Datasets used in this project were taken from:

1. Terrace House Prices
   - https://www.data.gov.my/data/ms_MY/dataset/harga-rumah-teres-mengikut-negeri

## Techniques

The techniques used to solve this problem comprised of the usage of statistics and matrix algebra. Given the nature of the dataset, we first calculated the yearly average by calculating the average over 4 quarters for each state.

When plotting these values, we noticed a linear pattern and hence implemented a matrix least square method to obtain a least square regression line. This enabled us to perform somewhat of a linear regression in obtaining a model of house price prediction based on the number of years from 2009.

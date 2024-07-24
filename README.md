# King County House Sales Data Analysis

This repository contains an analysis of house sales data from King County, USA, including Seattle, for homes sold between May 2014 and May 2015. The goal is to explore the data, understand the key factors affecting house prices, and build predictive models to estimate house prices based on these factors.

## Table of Contents

- [Introduction](#introduction)
- [Data Overview](#data-overview)
- [Data Cleaning](#data-cleaning)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Model Development](#model-development)
- [Key Insights](#key-insights)
- [Conclusion](#conclusion)

## Introduction

The project aims to:
- Understand the distribution and relationships between various features of houses sold in King County.
- Build predictive models to estimate house prices based on these features.
- Gain insights that can be useful for buyers, sellers, and real estate professionals.

## Data Overview

The dataset includes the following columns:
- `id`: Unique identifier for a house.
- `date`: Date the house was sold.
- `price`: Sale price of the house (target variable).
- `bedrooms`: Number of bedrooms.
- `bathrooms`: Number of bathrooms.
- `sqft_living`: Square footage of the living space.
- `sqft_lot`: Square footage of the lot.
- `floors`: Number of floors.
- `waterfront`: Whether the house has a waterfront view.
- `view`: Number of times the house has been viewed.
- `condition`: Condition of the house.
- `grade`: Overall grade given to the housing unit, based on King County grading system.
- `sqft_above`: Square footage of the house apart from the basement.
- `sqft_basement`: Square footage of the basement.
- `yr_built`: Year the house was built.
- `yr_renovated`: Year when the house was renovated.
- `zipcode`: ZIP code of the house location.
- `lat`: Latitude coordinate.
- `long`: Longitude coordinate.
- `sqft_living15`: Living room area in 2015 (implies some renovations).
- `sqft_lot15`: Lot size area in 2015 (implies some renovations).

## Data Cleaning

- Removed the `id` and `Unnamed: 0` columns as they are not relevant for analysis.
- Replaced missing values in the `bedrooms` and `bathrooms` columns with the mean values of their respective columns.

## Exploratory Data Analysis (EDA)

- Used value counts to understand the distribution of houses by the number of floors.
- Created boxplots to compare house prices based on whether they have a waterfront view.
- Used regression plots to examine the relationship between `sqft_above` and house prices.
- Calculated the correlation matrix to identify features that are most correlated with house prices.

## Model Development

- Built a linear regression model to predict house prices based on the `sqft_living` feature, achieving an R² value of 0.492.
- Developed a more comprehensive linear regression model using multiple features, achieving an R² value of 0.657.
- Implemented a Ridge regression model with polynomial features to improve the predictive performance, achieving an R² value of 0.742 for the training data and 0.700 for the testing data.

## Key Insights

- The most influential features on house prices are `sqft_living`, `grade`, and `sqft_above`.
- Houses with waterfront views tend to have higher prices.
- There is a positive correlation between `sqft_above` and house prices.

## Conclusion

The analysis provides valuable insights into the factors influencing house prices in King County. The predictive models developed can estimate house prices with a reasonable degree of accuracy, which can be useful for various stakeholders in the real estate market.


# CoronaVirus_ML

Final project for Data Analytics bootcamp at Ironhack Mexico City.

Consists of a 3 part analysis using Jupyter Notebook to train a model that determines the components for a logistic growth curve that represents the number of infected vs time, for a given country/location.


# V2

V2 compiles the previous 3 parts into a single Jupyter Notebook file.

## Variables

1. Population
2. Area
3. Air_Pm2.5 (Air Quality)
4. Male Population
5. Population Over 65
6. Foreign Turism
7. Health expenditure (USD)
8. Day first infected was detected

## Part 1

Prints the scatter graphs and determines the components L, k and a for a logistic growth curve:

```
y = L / 1 - exp( k ( x - a ) )
```

returns a csv with the components for each location.


## Part 2

Adds Population, Latitute and Longitude to generate plots over time vs population.

Returns csv with added parameters.


## Part 3

Adds rest of parameters from 4 datasets.

Splits Data on train and test.

Tries the following models to determine the components (L, k, a):
- RandomForest
- LinearRegression
- Lasso
- ElasticNet
- RidgeRegression
- SVR
- EnsembleRegressors

Uses the best model for each component (L, k, a) and predicts the components for Mexico.

# Next Steps

1. Causality analysis to check what variables affect specific components.
2. Add upper and lower limits to the predictions based on variability.
3. Add number of deaths as a component. high mortality rate (deaths / cased closed) could indicate the number of cases is underestimated.

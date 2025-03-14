# regtab

This Python package provides tools for extracting regression results and formatting them into a well-structured table. It helps with organizing regression coefficients, t-values (or standard errors), and other statistics such as R-squared and the number of observations. This is useful for presenting regression results in a neat format for academic papers, reports, or presentations.

## Features

- Extracts coefficients, t-values (or standard errors), and observations from regression models.
- Allows you to customize the number of decimal points displayed.
- Option to include R-squared and number of observations in the results.
- Supports renaming variables for clearer output.
- Easily generate formatted regression tables.

## Installation

pip install "https://github.com/rohanbjkr/regtab/raw/refs/heads/main/regtab-0.1-py3-none-any.whl"



## Use 
```
from regtab import regtab
models = {'model1': model1, 'model2': model2}
vars = ['exposurebirth', 'age', 'white', 'black', 'latinx', 'Intercept']
var_labels = {
    'exposurebirth': 'Exposure at Birth',
    'age': 'Age of Individual',
    'white': 'White',
    'black': 'Black',
    'latinx': 'Latinx',
    'Intercept': 'Intercept'
}


df = regtab(
    models, 
    vars, 
    var_labels, 
    show_tvalues=True, 
    decimal_points=3, 
    include_obs=True, 
    include_r2=False
)

print(df)


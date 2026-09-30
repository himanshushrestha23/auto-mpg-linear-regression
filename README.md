# Auto MPG Prediction — Linear Regression

## Description

A machine learning project using Python to predict a car's fuel efficiency (MPG) using Linear Regression. The project focuses on exploring and preparing the Auto MPG dataset, training multiple Linear Regression models, and comparing their performance using test RMSE.

## Dataset

The project uses the Auto MPG dataset, which contains information about different cars and their fuel efficiency.

The target variable is:

- `mpg` — miles per gallon (fuel efficiency)

The dataset includes features such as:

- `cylinders`
- `displacement`
- `horsepower`
- `weight`
- `acceleration`
- `model year`
- `origin`

## Project Workflow

The project follows a practical machine learning workflow:

1. Load the dataset.
2. Explore the dataset and its data types.
3. Investigate the `horsepower` column.
4. Handle missing horsepower values.
5. Explore relationships between numerical features using correlation.
6. Split the data into training and test sets.
7. Train Linear Regression models.
8. Evaluate models using test RMSE.
9. Experiment with different feature sets.
10. Compare the results and select a final model.

## Data Preparation

During exploration, the `horsepower` column was found to contain `?` values instead of numerical values.

These values were:

1. Replaced with missing values.
2. Converted to a numerical data type.
3. Filled using the median horsepower.

This allowed `horsepower` to be used as a numerical feature in the Linear Regression models.

## Models and Experiments

### Model 1 — Initial Model

The initial model uses:

- `displacement`
- `weight`
- `horsepower`
- `cylinders`

to predict `mpg`.

### Model 2 — Single-Feature Experiment

A second model was trained using only:

- `weight`

This experiment tested whether a single feature could perform well on its own.

The single-feature model performed worse than the initial model.

### Model 3 — Adding Model Year

The third model added:

- `model year`

to the features used in the initial model.

Adding `model year` improved the test RMSE compared with the initial model.

## Results

The experiments showed that:

- Using only `weight` performed worse than the initial model.
- The initial model benefited from using multiple features.
- Adding `model year` improved the test RMSE.
- Model 3 was selected as the final model for this project.

The final model uses:

- `displacement`
- `weight`
- `horsepower`
- `cylinders`
- `model year`

## Evaluation

The models were evaluated using **Root Mean Squared Error (RMSE)**.

RMSE measures the typical size of prediction errors and is expressed in the same units as the target.

A lower RMSE indicates that the model's predictions are generally closer to the actual MPG values.

The final model's predictions were also compared with the actual MPG values, along with the L1 Loss for each test example.

## Technologies Used

- Python 3
- Pandas
- NumPy
- Scikit-learn
- Google Colab
- Git & GitHub

## What I Learned

- Exploring a dataset before training a model.
- Investigating unexpected data types.
- Handling missing values.
- Using correlation to explore numerical relationships.
- Preparing features for Linear Regression.
- Splitting data into training and test sets.
- Training Linear Regression models using scikit-learn.
- Making predictions on test data.
- Evaluating regression models using RMSE.
- Comparing different feature sets through experiments.
- Using Git and GitHub to manage and share an ML project.

## How to Run

1. Clone this repository.
2. Open the project folder.
3. Open `auto-mpg-linear-regression.ipynb` in Google Colab or another Jupyter environment.
4. Make sure the dataset is located at:

```text
data/auto-mpg.csv

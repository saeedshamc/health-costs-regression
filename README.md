# Linear Regression Health Costs Calculator

A neural network regression model built with TensorFlow and Keras that predicts individual healthcare costs from personal data such as age, BMI, number of children, sex, smoking status, and region. This project is part of the freeCodeCamp Machine Learning with Python certification.

## Overview

- Dataset: insurance data with about 1,300 people and their healthcare expenses
- Categorical columns (sex, smoker, region) are converted to numbers with one-hot encoding
- 80% of the data is used for training and 20% for testing
- The `expenses` column is popped off to create the training and test labels
- The goal is a Mean Absolute Error under 3500 on the unseen test set

## Model

| Component | Details |
|-----------|---------|
| Input normalization | Keras `Normalization` layer adapted on the training set |
| Hidden layers | Dense 128, 64, 32 with ReLU |
| Output | Dense 1, rescaled to the range of the expenses |
| Optimizer | Adam, learning rate 0.001 |
| Loss | Mean absolute error |
| Training | Up to 500 epochs with early stopping (patience 50) and 20% validation split |

## Results

| Metric | Value |
|--------|-------|
| Test Mean Absolute Error | XX |

Add the predictions plot here:

![Predictions](images/predictions.png)

## Getting Started

### Run in Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO/blob/main/fcc_predict_health_costs_completed.ipynb)

### Run locally

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
jupyter notebook fcc_predict_health_costs_completed.ipynb
```

The notebook downloads the dataset with `!wget`, which needs a Unix shell. On Windows, use Colab or WSL.

## Project Structure

```
.
├── fcc_predict_health_costs_completed.ipynb
├── requirements.txt
├── README.md
├── .gitignore
└── images/
```

## Technologies

Python, TensorFlow, Keras, pandas, NumPy, Matplotlib

## Acknowledgments

Dataset and challenge by [freeCodeCamp](https://www.freecodecamp.org).

# ANLY 530 – Food Demand Forecasting Research

## Project Overview

This project is part of ANLY 530: Principles and Applications of Machine Learning at Harrisburg University.

**Research Title:** Evaluating Machine Learning Models for Weekly Food Demand Forecasting: A Time-Series-Aware Comparative Study

The objective is to investigate how different machine learning approaches predict weekly food demand and whether more complex models offer meaningful improvements over simpler forecasting methods.

## Research Questions

1. How do historical-demand baselines, linear regression, regularized regression, random forests, and gradient boosting compare in predicting weekly food demand?
2. How stable are model errors across chronological validation periods?
3. Do nonlinear ensemble models provide sufficient improvements to justify their additional complexity?

## Dataset

**Dataset:** Genpact Food Demand Forecasting

**Source:** [Food Demand Forecasting – Kaggle](https://www.kaggle.com/datasets/kannanaikkal/food-demand-forecasting)

The training dataset contains approximately 456,548 observations covering weeks 1–145.

Each observation represents weekly food orders for a particular fulfillment center and meal.

**Target variable:** `num_orders`

**Predictor variables:**
- `week`
- `center_id`
- `meal_id`
- `checkout_price`
- `base_price`
- `emailer_for_promotion`
- `homepage_featured`

The dataset is not included in this repository. Download it separately from Kaggle.

## Methodology

The research follows a time-series-aware machine learning approach.

**Data preparation:** Examine missing values, duplicates, distributions, unusual observations, and data quality.

**Preprocessing:** Handle missing values, encode categorical variables, and scale features where appropriate.

**Modeling approaches:**
- Historical-demand baseline
- Linear regression
- Ridge regression
- Lasso regression
- Random Forest (planned)
- Gradient Boosting (planned)

**Validation:** Use chronological training and validation splits to prevent information from future weeks influencing model training.

**Evaluation metrics:** Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and prediction bias.

## Research Design

The dataset is divided chronologically:

| Dataset | Weeks |
|---|---|
| Development | 1–116 |
| Final holdout | 117–145 |

Expanding-window validation is performed within the development period.

All preprocessing and model selection must use training data only.

## Repository Contents

- `Food_Forecasting_Research.ipynb` – Exploratory analysis and baseline modeling notebook
- `README.md` – Research documentation
- `requirements.txt` – Python dependencies

## How to Reproduce the Analysis

1. Download the dataset from Kaggle.
2. Open `Food_Forecasting_Research.ipynb` in Google Colab.
3. Upload `train.csv` to the Colab session.
4. Follow the dataset path instructions in the notebook.
5. Run all cells in order.
6. Review the exploratory analysis and model evaluation outputs.

The notebook uses Python, pandas, NumPy, scikit-learn, matplotlib, and Jupyter-compatible tools.

## Limitations

The study uses a single public competition dataset, which may limit generalizability. Historical associations do not establish causal relationships. Forecasting performance may also depend on whether future pricing and promotional information is available when predictions are generated.

## Research Timeline

- **Week 10:** Research protocol, exploratory notebook, and GitHub repository
- **Week 11:** Verify data quality and baseline experiments
- **Week 12:** Evaluate additional candidate models and complete Milestone 2
- **Week 13:** Final research paper and five-minute presentation

## Individual Contribution

This is an individual research project. The author is responsible for research design, literature review, data analysis, Python implementation, model evaluation, documentation, and final presentation.

## Author

Tripti Rijhwani  
Harrisburg University  
ANLY 530 – Principles and Applications of Machine Learning


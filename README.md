# Feature Engineering Challenge – Titanic Dataset

This project explores whether feature engineering can improve a machine learning model's ability to predict Titanic passenger survival.

## Research Question

Can creating new features improve the accuracy of predicting Titanic passenger survival?

## Project Contents

- `feature_engineering.ipynb` – Jupyter Notebook containing data exploration, baseline modelling, feature engineering, cross-validation, evaluation, and error analysis.
- `Feature_Engineering_Titanic_Project_Report.docx` – Project report.
- `requirements.txt` – Python dependencies.
- `data/README.md` – Instructions for obtaining and placing the dataset.

## Dataset Setup

The Titanic competition dataset is not included in this repository. Download `train.csv` from the Kaggle Titanic competition data page:

https://www.kaggle.com/competitions/titanic/data

Create/keep the file at this exact location:

```text
data/train.csv
```

The notebook loads the dataset using:

```python
df = pd.read_csv("data/train.csv")
```

## Installation

Use Python 3.10 or later. From the project folder, install the dependencies:

```bash
pip install -r requirements.txt
```

## Run the Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open `feature_engineering.ipynb` and run the cells from top to bottom.

## Features Created

1. `Title`
2. `FamilySize`
3. `IsAlone`
4. `FarePerPerson`
5. `Deck`
6. `HasCabin`
7. `TicketPrefix`
8. `NameLength`
9. `AgeGroup`
10. `AgeMissing`

## Model and Evaluation

- Model: Logistic Regression
- Validation: Stratified 5-fold cross-validation
- Metrics: Accuracy and F1-score
- Additional evaluation: held-out test split, confusion matrix, classification report, and analysis of 10 incorrect predictions

## Notes on the Saved Notebook Results

The saved notebook outputs show a baseline mean cross-validation accuracy of approximately **79.69%**. The model using all ten engineered features achieved approximately **82.26%**. Adding `Title` alone achieved approximately **82.83%** in the saved cross-validation results. Results may vary if the notebook is rerun with different data or settings.


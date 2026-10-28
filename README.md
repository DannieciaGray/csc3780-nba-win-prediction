# Predicting NBA Home-Team Wins from Game Statistics

CSC 3780: Fundamentals of Data Science, Fall 2026 (Prof. Kiril Kuzmin)
**Group:** SustainABLE

| Member | Role |
|---|---|
| Danniecia Gray | Modeling & Evaluation, repo maintainer |
| Tony Nguyen | Data Acquisition & Preparation |
| Jinash Rouniyar | Exploratory Analysis & Feature Selection |
| Emanuel Tossou | Report & Presentation |

## Research question
Which game statistics best distinguish NBA wins from losses, and can we predict whether the home team wins from those statistics? We also measure how much home-court advantage matters compared to shooting efficiency, rebounds, and assists.

- **Data:** [NBA Games dataset (Kaggle)](https://www.kaggle.com/datasets/nathanlauga/nba-games), regular-season games
- **Target:** `HOME_TEAM_WINS` (1 = home win, 0 = home loss)
- **Features:** home-minus-away differences in FG%, FT%, 3P%, assists, rebounds (points excluded to avoid target leakage)
- **Models:** majority-class baseline, logistic regression, decision tree, kNN, random forest
- **Metrics:** accuracy, precision, recall, F1, ROC-AUC

## Repository structure
```
data/
  raw/              original Kaggle CSVs (submitted as-is)
  processed/        final dataset used for modeling
notebooks/
  01_data_understanding.ipynb
  02_preprocessing.ipynb
  03_eda_feature_selection.ipynb
  04_modeling_evaluation.ipynb
reports/
  figures/          charts exported from the notebooks
  final_report.pdf  (added at the end)
presentation/       slide deck
```

## Getting started
```bash
git clone https://github.com/DannieciaGray/csc3780-nba-win-prediction.git
cd csc3780-nba-win-prediction
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```
1. Download `games.csv` (and `teams.csv`) from Kaggle into `data/raw/`.
2. Run the notebooks in order (01 → 04). Each one reads the previous step's output.

## Workflow
- Work on a branch named after your task, e.g. `tony/preprocessing`.
- Open a pull request into `main` and ask one teammate to review.
- Restart the kernel and **Run All** before committing a notebook, so it runs in order.

## Deadlines
| Date | Deliverable |
|---|---|
| Oct 31 | Select presentation date (iCollege) |
| Nov 30 / Dec 2 / Dec 7 | Group presentation (12–15 min) |
| Dec 8, 11:00 p.m. | Final submission: data, notebooks, report PDF |

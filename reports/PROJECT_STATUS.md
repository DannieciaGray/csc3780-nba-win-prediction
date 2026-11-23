# Project status — 2026-11-23

## Work completed and verified

- **Jinash Rouniyar — EDA and Feature Selection:** Complete. Notebook `notebooks/03_eda_feature_selection.ipynb` contains executed outputs; nine supporting EDA figures are stored in `reports/figures/`. Final five model inputs: FG_PCT_diff, TOV_diff, REB_diff, FG3_PCT_diff, FT_PCT_diff. The analysis restricts modeling to 16,816 valid games from seasons 2000–2015.
- **Danniecia Gray — Modeling and Evaluation:** Complete and tested. Notebook `notebooks/04_modeling_evaluation.ipynb` ran successfully in the repository's GitHub Actions workflow with the actual processed CSV, and its executed output is committed. The full metrics are in `reports/model_comparison.csv`; confusion matrix is in `reports/figures/final_model_confusion_matrix.png`.
- **Model choice:** Logistic Regression selected by cross-validation ROC-AUC (0.9750). Held-out Accuracy 0.9111, F1 0.9266, ROC-AUC 0.9749. Majority baseline held-out Accuracy 0.5972.
- **Full-dataset validation:** Successful GitHub Actions run: https://github.com/DannieciaGray/csc3780-nba-win-prediction/actions/runs/45178305330

## Remaining work outside these two assignments

- Emanuel: final report and presentation, including data limitations.
- Team: final review and submission.
- Tony: confirm whether problematic 2016–2025 statistics should be excluded upstream. The modeling notebook explicitly excludes these rows, so this issue does not affect the validated results.

## Interpretation note

The predictors are observed in the *same games* as the outcomes. These models classify the outcomes of completed games; they are not pregame forecasts.

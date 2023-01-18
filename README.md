# kaggle-ps-s3e2

Kaggle Playground Series 3, Episode 3 competition

NOTES:

* Catboost by default seems to be the best.
* RandomForest performs slightly better than XGBoost.

Tasks to obtain the best model:

* [x] Basic eda
* [x] Cross-validation
* [x] First training
* [x] Use AutoGluon framework -> improvement over catboost default
* [x] Use ten folds -> improvement by ~0.02%, but test public score disagree
* [ ] Merge original dataset
* [ ] Implement Lasso regression
* [ ] Implement logistic regression
* [ ] Scale numerical variables between 0 and 1

## Train, validation & submission

```bash
cd src
conda activate ml
python create_folds.py
python -W ignore train.py [--model=lgbm]  # [rf|svd|xgb|lgbm|cb]
```

Submission is stored in outputs folder (see `config.py` for complete path)

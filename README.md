

<h3 align="center">AutoML</h3>

<div align="center">

[![Downloads](https://pepy.tech/badge/automl-alex)](https://pepy.tech/project/automl-alex)
![PyPI - Python Version](https://img.shields.io/pypi/pyversions/automl-alex)
![PyPI](https://img.shields.io/pypi/v/automl-alex)
[![CodeFactor](https://www.codefactor.io/repository/github/alex-lekov/automl_alex/badge)](https://www.codefactor.io/repository/github/alex-lekov/automl_alex)
[![Telegram](https://img.shields.io/badge/chat-on%20Telegram-2ba2d9.svg)](https://t.me/automlalex)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---

<p align="center"> State-of-the art Automated Machine Learning python library for Tabular Data</p>

## Works with Tasks:

-   [x] Binary Classification

-   [x] Regression

-   [ ] Multiclass Classification (in progress...)

### Benchmark Results
<img width=800 src="https://github.com/Alex-Lekov/AutoML-Benchmark/blob/master/img/Total_SUM.png" alt="bench">

### Scheme
<img width=800 src="https://github.com/Alex-Lekov/AutoML_Alex/blob/develop/examples/img/shema.png" alt="scheme">


# Features

- Automated Data Clean (Auto Clean)
- Automated **Feature Engineering** (Auto FE)
- Smart Hyperparameter Optimization (HPO)
- Feature Generation
- Feature Selection
- Models Selection
- Cross Validation
- Optimization Timelimit and EarlyStoping
- Save and Load (Predict new data)


# Installation

```python
pip install automl
```

# 🚀 Examples

Classifier:
```python
from automl import AutoMLClassifier

model = AutoMLClassifier()
model.fit(X_train, y_train, timeout=600)
predicts = model.predict(X_test)
```

Regression:
```python
from automl import AutoMLRegressor

model = AutoMLRegressor()
model.fit(X_train, y_train, timeout=600)
predicts = model.predict(X_test)
```

DataPrepare:
```python
from automl import DataPrepare

de = DataPrepare()
X_train = de.fit_transform(X_train)
X_test = de.transform(X_test)
```

Simple Models Wrapper:
```python
from automl import LightGBMClassifier

model = LightGBMClassifier()
model.fit(X_train, y_train)
predicts = model.predict_proba(X_test)

model.opt(X_train, y_train,
    timeout=600, # optimization time in seconds,
    )
predicts = model.predict_proba(X_test)
```
# What's inside

It integrates many popular frameworks:
- scikit-learn
- XGBoost
- LightGBM
- CatBoost
- Optuna
- ...


# Works with Features

-   [x] Categorical Features

-   [x] Numerical Features

-   [x] Binary Features

-   [ ] Text

-   [ ] Datetime

-   [ ] Timeseries

-   [ ] Image


# Note

- **With a large dataset, a lot of memory is required!**
Library creates many new features. If you have a large dataset with a large number of features (more than 100), you may need a lot of memory.

Run
```console
$ optuna-dashboard sqlite:///db.sqlite3
```

# Road Map

-   [x] Feature Generation

-   [x] Save/Load and Predict on New Samples

-   [x] Advanced Logging

-   [x] Add opt Pruners

-   [ ] Docs Site

-   [ ] DL Encoders

-   [ ] Add More libs (NNs)

-   [ ] Multiclass Classification

-   [ ] Build pipelines

Contact: kaushikeva0026@gmail.com


# WineClassifier

A statistics + ML based study of the differentiating characteristics of red and white wines.

Can a wine's type (red or white) be predicted purely from lab-measured physicochemical
properties — acidity, sugar, sulfur dioxide, density, pH, etc. — with no tasting involved?
This project explores that question on the [UCI Wine Quality dataset](https://archive.ics.uci.edu/ml/datasets/wine+quality)
(6,497 wines, 11 numeric features), comparing:

- **Logistic regression** — a full 11-feature model vs. a compact, hand-picked 2-feature model
- **Principal Component Analysis (PCA)** — how much class-separating signal survives an
  unsupervised reduction to 2 dimensions
- **Support Vector Machine** — a linear-kernel SVM tuned with grid search

See [`wine_classifier.ipynb`](wine_classifier.ipynb) for the full analysis, including
plots, model diagnostics, and a discussion of precision/recall trade-offs.

## Running it

```bash
pip install numpy pandas matplotlib seaborn scikit-learn statsmodels jupyter
jupyter notebook wine_classifier.ipynb
```

The dataset is fetched automatically from a public GitHub-hosted CSV — no manual download
needed.

## Background

This project began as an individual final exam for CMSE 202 (Michigan State University,
Fall 2022). It's been reorganized here as a standalone project: the exam scaffolding,
grading cells, and git-workflow instructions have been removed, and a few rough edges in
the original modeling code (numerical instability in the full logistic regression fit,
deprecated pandas usage) have been cleaned up. The statistical and ML content is unchanged
in substance.

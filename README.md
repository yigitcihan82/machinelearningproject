# Machine Learning – Midterm Assignment

Breast Cancer Wisconsin and Wine Classification: Decision Tree, KNN, Gaussian Naive Bayes and K-Means,
with three training/validation seeds (42, 52, 62) and a fixed test set.

- Repository: [PASTE REPOSITORY LINK HERE]
- Video: [PASTE VIDEO LINK HERE]

## Dataset sources

Both datasets are loaded directly from scikit-learn; no data file is downloaded.

- Breast Cancer Wisconsin (Diagnostic): `sklearn.datasets.load_breast_cancer` (569 samples, 30 features, 2 classes)
- Wine: `sklearn.datasets.load_wine` (178 samples, 13 features, 3 classes)

## Files

| File | Content |
|---|---|
| `breast_cancer.ipynb` | Sections 1–10 for Breast Cancer Wisconsin (66 classifier fits + 6 K-Means fits) |
| `wine.ipynb` | Sections 1–10 for Wine Classification (66 classifier fits + 6 K-Means fits) |
| `comparison.ipynb` | Sections 11–12: comparison of the two datasets and run/output inventory (reads the CSV files, fits nothing) |
| `report.docx` | Written report |
| `results/` | The six CSV files of Section 12 (`classifier_runs`, `classifier_summary`, `classifier_test`, `kmeans_runs`, `kmeans_summary`, `kmeans_test`) and the split row indices of each dataset |
| `figures/` | 21 PNG figures (EDA, parameter comparisons, confusion matrices, ROC curves, class-versus-cluster plots) |
| `requirements.txt` | Exact package versions |

## Python and package versions

Python 3.13, numpy 2.5.3, pandas 3.0.5, scikit-learn 1.9.1, matplotlib 3.11.2
(the versions are also printed at the top of each notebook).

## How to install and run

```
pip install -r requirements.txt
jupyter nbconvert --to notebook --execute --inplace breast_cancer.ipynb
jupyter nbconvert --to notebook --execute --inplace wine.ipynb
jupyter nbconvert --to notebook --execute --inplace comparison.ipynb
```

Or open each notebook (for example in VS Code), select the Python kernel and choose *Restart* and then *Run All*.
The two dataset notebooks are self-contained and can be run in any order; each one replaces only its own rows in the
shared CSV files. `comparison.ipynb` must be run last.

## Totals

132 classifier fits + 12 K-Means fits = 144 model fits. The 2 classifier and 4 clustering test evaluations
reuse the seed-42 fitted models and add no fits.

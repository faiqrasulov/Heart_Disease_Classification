# Heart disease: comparing seven classifiers

> Course assignment from 2023, kept as it was written. The notes under "Reading the result" were added in November 2026.

Compares SVM (linear and RBF), logistic regression, k-nearest neighbours, naive Bayes, random
forest and a decision tree on the 303-patient heart disease dataset.

## Result

Accuracy on the 61 test patients (80/20 stratified split, standardised features):

| Model | Accuracy |
|---|---|
| SVM, RBF kernel | 85.2% |
| SVM, linear kernel | 85.2% |
| Logistic regression | 85.2% |
| k-nearest neighbours (k = 6) | 82.0% |
| Gaussian naive Bayes | 80.3% |
| Random forest (10 trees) | 77.0% |
| Decision tree (depth 4) | 75.4% |

## Reading the result

- **The ranking is not reliable.** With 61 test patients one patient is 1.6 points, and the top
  three models are tied at 52 correct. The brief asks which model is best "on average"; that needs
  repeated cross-validation, which the notebook does not do.
- The linear models doing as well as the non-linear ones is the stable finding: on 303 rows there
  is little for a flexible model to gain.

## Newer work on the same topic

- [credit-risk-scorecard](https://github.com/faiqrasulov/credit-risk-scorecard): model comparison with repeated cross-validation and confidence intervals.

## Files

| File | Content |
|---|---|
| `Heart Disease Classification.ipynb` | Analysis |
| `Heart Disease Classification.html` | Rendered copy |
| `heart.csv` | The dataset |
| `About.txt` | Original brief |

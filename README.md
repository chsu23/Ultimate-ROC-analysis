# Ultimate ROC Analysis Tool

All statistical calculations run in the user's browser; no Python installation, backend server, or database is required.

## Features

- Import Excel (`.xlsx`, `.xls`) or CSV (`.csv`) files
- Single-marker ROC analysis
- Separate ROC curves for Marker 1 and Marker 2
- Optional logistic regression combined model
- AUC, 95% CI, optimal cutoff, and Youden index
- Sensitivity, specificity, accuracy, PPV, NPV, TP, TN, FP, and FN
- Optional paired bootstrap comparison of maximum Youden indices
- Optional DeLong's test for paired AUC comparison
- Optional McNemar's test for paired accuracy comparison
- Downloadable ROC plots and Excel/CSV results


## Data Privacy

- Uploaded datasets are parsed and analyzed in browser memory.
- The application contains no code that sends uploaded analysis data to a backend server.
- Excel import/export uses the SheetJS library loaded from cdnjs, so an internet connection is required for Excel functionality.
- Do not commit real patient data, identifiers, protected health information, or other sensitive files to the public GitHub repository.

## Outcome Format

The outcome column must contain exactly two valid classes. If one class is numeric `0`, the tool selects `0` as the default positive outcome. Users may select either class as positive.

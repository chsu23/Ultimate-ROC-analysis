# ROC Analysis Tool

A browser-based ROC analysis application that can be deployed directly to GitHub Pages. All statistical calculations run in the user's browser; no Python installation, backend server, or database is required.

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

## Repository Contents

- `index.html`: Main web application
- `sample_data.xlsx`: Example Excel dataset
- `sample_data.csv`: Example CSV dataset
- `.nojekyll`: Publishes the repository as static files without Jekyll processing

## Deploy to GitHub Pages

1. Create a new GitHub repository.
2. Upload all files from this folder to the repository root.
3. Open the repository **Settings**.
4. Select **Pages** in the left sidebar.
5. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
6. Select the `main` branch and `/(root)` folder, then click **Save**.
7. After deployment is complete, open the URL displayed in the Pages settings.

A project-site URL usually follows this format:

```text
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/
```

## Updating the Site

Edit or replace `index.html` on the `main` branch. GitHub Pages will redeploy the site automatically.

## Data Privacy

- Uploaded datasets are parsed and analyzed in browser memory.
- The application contains no code that sends uploaded analysis data to a backend server.
- Excel import/export uses the SheetJS library loaded from cdnjs, so an internet connection is required for Excel functionality.
- Do not commit real patient data, identifiers, protected health information, or other sensitive files to the public GitHub repository.

## Outcome Format

The outcome column must contain exactly two valid classes. If one class is numeric `0`, the tool selects `0` as the default positive outcome. Users may select either class as positive.

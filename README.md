# Kenya Malaria PCA Formative Assignment

This repository contains the completed PCA formative assignment notebook built from the provided template. The analysis uses Kenyan county-level malaria data from the Humanitarian Data Exchange (HDX), then implements Principal Component Analysis from scratch with NumPy.

## Main Deliverable

- `Completed_PCA_Formative_Kenya_Malaria_HDX.ipynb`

Open this notebook in Google Colab or Jupyter, run every cell, confirm that all outputs and plots are visible, then export the notebook as a PDF for submission.

## Dataset Choice

The assignment requires an Africanized dataset with missing values, at least one non-numeric column, and at least seven columns. This project uses Kenya malaria-related HDX resources and merges them by county.

HDX resources used:

- Malaria cases per 100,000 people in Kenya: `kenya_malaria_cases_per_100000_county.csv`
- Kenya expenditure on malaria per capita per county: `kenya_malaria_spending_county.csv`
- Kenya bed nets, malaria/fever occurrence, and health spending per county: `kenya_malaria_bednets_county.csv`

Source pages:

- https://data.humdata.org/dataset/malaria-cases-per-100-000-people-in-kenya
- https://data.humdata.org/dataset/kenya-health-spending-per-capita-per-county
- https://data.humdata.org/dataset/bed-nets-and-illness-by-county-kenya

The merged analysis table includes county name, country, malaria cases per 100,000 people, bed-net usage percentages, fever/malaria occurrence percentages, spending measures, and derived malaria burden/prevention features.

## Assignment Checklist

- Africanized dataset: Kenya county-level malaria data from HDX.
- Minimum seven columns: the merged dataset has more than seven columns.
- Missing values: the HDX cases file contains missing/blank values, and the notebook counts and handles them before PCA.
- Non-numeric data: county, country, and malaria burden group are identified; categorical features are handled before PCA.
- PCA from scratch: covariance, eigendecomposition, eigenvalue sorting, explained variance, and projection are implemented with NumPy.
- Dynamic component selection: the notebook selects the smallest number of components that retains at least 90% explained variance.
- Benchmarking: the notebook includes a vectorized PCA function and runtime comparison on the original and repeated larger dataset.
- Visualization: the notebook plots original feature space and PCA space after transformation.
- No sklearn: sklearn is not used.

## Files

- `Template_PCA_Formative_1[Peer_Pair_Number] (2).ipynb`: original assignment template.
- `Completed_PCA_Formative_Kenya_Malaria_HDX.ipynb`: completed notebook to run and export.
- `kenya_malaria_cases_per_100000_county.csv`: HDX malaria cases resource.
- `kenya_malaria_spending_county.csv`: HDX malaria spending resource.
- `kenya_malaria_bednets_county.csv`: HDX bed-net/malaria/fever resource.
- `README.md`: project documentation.

## How to Run

1. Open `Completed_PCA_Formative_Kenya_Malaria_HDX.ipynb`.
2. Run all cells from top to bottom.
3. Verify that data previews, covariance output, eigenvalues, explained variance output, benchmarking output, and both plots are visible.
4. Export the notebook as a PDF.
5. Add the completed group contribution/task sheet PDF to the repository.
6. Combine the notebook PDF and task sheet PDF into one final PDF as required by the assignment.

## PCA Use Case

The use case is Kenyan malaria burden and prevention analysis at county level. PCA reduces malaria cases, fever/malaria occurrence, bed-net usage, and spending variables into fewer principal components so counties can be compared using the dominant patterns in the data.

The selected principal components preserve broad information such as malaria pressure, prevention coverage, and spending intensity. The main tradeoff is that reducing dimensions compresses exact county-level details from individual indicators.

## Notes for Submission

The final interpretation paragraphs in the notebook should be reviewed and rewritten by the group in your own words before submission, especially because the assignment explicitly asks students to avoid AI-generated interpretations.


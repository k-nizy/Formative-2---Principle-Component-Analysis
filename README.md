# Kenya Malaria PCA Formative Assignment

This repository contains the completed PCA formative assignment notebook built from the provided template. The analysis uses Kenyan county-level malaria data from the Humanitarian Data Exchange (HDX), then implements Principal Component Analysis from scratch with NumPy only.

## Main Deliverable

- `Completed_PCA_Formative_Kenya_Malaria_HDX.ipynb`

Open this notebook in Google Colab or Jupyter, run every cell, confirm that all outputs and plots are visible, then export the notebook as a PDF for submission.

## Dataset Choice

The assignment requires an Africanized dataset with missing values, at least one non-numeric column, and at least seven columns. This project uses Kenya malaria-related HDX resources and merges them by county.

HDX resources used:

- Malaria cases per 100,000 people in Kenya: `kenya_malaria_cases_per_100000_county.csv`
- Kenya expenditure on malaria per capita per county: `kenya_malaria_spending_county.csv`
- Kenya bed nets, malaria/fever occurrence, and health spending per county: `kenya_malaria_bednets_county.csv`

## How to Run
1. Open Completed_PCA_Formative_Kenya_Malaria_HDX.ipynb in Google Colab or Jupyter.
2. Run all cells from top to bottom.
3. Confirm that all outputs are visible: data previews, covariance matrix, eigenvalues, explained variance, benchmarking results, and both plots.
4. Export the notebook as a PDF.
5. Combine the notebook PDF and task_sheet.pdf into one final PDF for submission.

Source pages:

- https://data.humdata.org/dataset/malaria-cases-per-100-000-people-in-kenya
- https://data.humdata.org/dataset/kenya-health-spending-per-capita-per-county
- https://data.humdata.org/dataset/bed-nets-and-illness-by-county-kenya

The merged analysis table includes county name, country, malaria cases per 100,000 people, bed-net usage percentages, fever/malaria occurrence percentages, spending measures, and derived malaria burden/prevention features.

## Assignment Checklist

- Africanized dataset (Kenya county-level malaria data from HDX)
- Minimum seven columns
- Missing values present and handled
- Non-numeric columns identified and handled
- PCA implemented from scratch with NumPy (no sklearn)
- Dynamic component selection based on explained variance
- Benchmarking included
- Before and after PCA visualizations included
- Group contribution/task sheet PDF in repository

## Files

- `Template_PCA_Formative_1[Peer_Pair_Number] (2).ipynb`: original assignment template.
- `Completed_PCA_Formative_Kenya_Malaria_HDX.ipynb`: completed notebook to run and export.
- `kenya_malaria_cases_per_100000_county.csv`: HDX malaria cases resource.
- `kenya_malaria_spending_county.csv`: HDX malaria spending resource.
- `kenya_malaria_bednets_county.csv`: HDX bed-net/malaria/fever resource.
- `README.md`: project documentation.


## PCA Use Case

The use case is Kenyan malaria burden and prevention analysis at county level. PCA reduces malaria cases, fever/malaria occurrence, bed-net usage, and spending variables into fewer principal components so counties can be compared using the dominant patterns in the data.

The selected principal components preserve broad information such as malaria pressure, prevention coverage, and spending intensity. The main tradeoff is that reducing dimensions compresses exact county-level details from individual indicators.

## Challenges and Lessons Learned

During this project, we learned that implementing PCA from scratch requires careful handling of missing values, proper standardization, and correct sorting of eigenvalues and eigenvectors. We also understood the importance of dimensionality reduction in simplifying complex health datasets while preserving meaningful information.

## PCA Implementation Summary

Data Handling

Missing values in the HDX cases file are counted and handled before PCA is applied. Non-numeric columns (county name, country, malaria burden group) are identified and excluded from the numerical 
pipeline before standardization.

Component Selection

Components were selected using a 90% explained variance threshold — the smallest number of principal components whose cumulative explained variance reaches or exceeds 90%.

This threshold was chosen because the dataset captures related but overlapping public health indicators (spending, bed-net coverage, case rates, fever occurrence). A 90% cutoff retains the dominant patterns overall malaria pressure and prevention coverage intensity without keeping noise from weakly correlated indicators.

Tradeoff: By reducing to fewer components, we lose the ability to distinguish between counties that differ only on secondary indicators. For example, two counties with similar malaria case rates but very different bed-net coverage or spending levels may appear close together in PCA space even though their prevention situations are meaningfully different. Fine-grained county comparisons based on individual indicators are not possible from the reduced representation alone.

## Notes for Submission

The final interpretation paragraphs in the notebook should be reviewed and rewritten by the group in your own words before submission, especially because the assignment explicitly asks students to avoid AI-generated interpretations.


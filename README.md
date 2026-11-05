# Privacy-Preserving HR Analytics — Clustering

A data analytics project exploring how privacy transformations affect the usefulness of employee data for unsupervised segmentation.

**Academic context:** MSc in Business Intelligence & Analytics, ISCAP (2025/26)  
**Authors:** Débora Jesus and João Coelho

## Project objective

Can employee-related data be transformed to reduce exposure of sensitive information while retaining useful structure for analytical segmentation?

The project uses a **synthetic dataset of 10,000 employee records** generated for the notebook. It does not contain real employee records.

## Methodology

1. Generate and document the synthetic dataset.
2. Classify variables according to their sensitivity.
3. Apply K-Means clustering to the original dataset.
4. Create a protected version using anonymisation, pseudonymisation (hashing), and encoding.
5. Apply K-Means to the transformed dataset.
6. Compare the two cluster assignments using the **Adjusted Rand Index (ARI)**.
7. Use controlled mapping tables to support interpretation of transformed identifiers.

## Findings

The project reports a high ARI between the original and transformed cluster assignments, indicating that the selected transformations retained much of the clustering structure in this synthetic experiment.

The identified profiles were interpreted as:
- Career progression
- Underperformance
- Retirement

The ARI is a measure of similarity between cluster assignments; it is not, by itself, proof that a dataset is anonymous or that re-identification risk has been eliminated.

## Technology stack

- Python and pandas
- scikit-learn (K-Means and Adjusted Rand Index)
- hashlib for pseudonymisation examples
- Matplotlib for visual analysis
- Google Colab / Jupyter Notebook

## Repository structure

```text
.
├── notebooks/   # End-to-end analysis and experiments
├── data/        # Synthetic dataset (10,000 records)
└── docs/        # Project report
```

## Reproducing the analysis

1. Open the notebook in Jupyter or Google Colab.
2. Run the data-generation and preparation cells.
3. Execute the baseline clustering.
4. Apply the privacy transformations.
5. Run the transformed-data clustering and compare the labels with ARI.

## Scope and limitations

- The dataset is synthetic; findings should not be generalized to real HR populations.
- Hashing is pseudonymisation, not anonymisation. Identifiers may remain linkable, especially when the input space is small or predictable.
- A high ARI indicates similar cluster structure, not that every transformation is privacy-preserving.
- The project is an academic demonstration and is not a production HR decision system.

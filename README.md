# PCA on Gene Expression Data

This project explores **Principal Component Analysis (PCA)** on gene expression data for dimensionality reduction and visualization. Using the **GSE5325** dataset from the Nature Primer "What is principal component analysis?", we analyze how specific biomarkers can distinguish between different breast cancer subtypes.

The aim was to understand how PCA can help identify patterns and separation in biological samples using high-dimensional transcriptomics data.

## Files Included

* **data/filtered.tsv.gz** → Filtered gene expression matrix for 105 patients.
* **data/class.tsv** → Sample class labels (1: ER+ breast cancer, 0: ER- breast cancer).
* **data/columns.tsv.gz** → Metadata/column information mapping IDs to Gene Symbols.
* **PCA_Analysis.ipynb** → The Google Colab containing the analysis and visualizations.

## Analysis Workflow

1.  **Data Processing**: Extracted expression levels for key biomarkers **GATA3** and **XBP1** for all 105 patient samples.
2.  **Visualization (Figure 1a)**: Generated a 2D scatter plot to observe the raw correlation between the two genes and the clinical labels.
3.  **Dimensionality Reduction**: Applied PCA to project the 2D gene data onto a single **Principal Component (PC1)**.
4.  **Separation Analysis (Figure 1c)**: Visualized the samples along the PC1 axis to demonstrate how PCA captures the maximum variance and successfully separates ER+ from ER- samples.

## Key Insights
* **PC1** captured a significant percentage of the total variance, effectively condensing two dimensions of data into one while maintaining the biological "signal."
* The analysis confirms that GATA3 and XBP1 expression levels are strong predictors of Estrogen Receptor (ER) status in breast cancer patients.

## Tools Used

* **Python**
* **pandas** (Data manipulation)
* **scikit-learn** (PCA implementation)
* **matplotlib** (Data visualization)

## Running the Project

1. **Clone the repository**:
   ```bash
   git clone https://github.com/deekshant-artiya/pca.git
   cd pca

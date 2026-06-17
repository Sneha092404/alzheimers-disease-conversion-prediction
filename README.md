Alzheimer's Disease Conversion Prediction Using Serum miRNA Expression Profiles and Machine Learning

Project Overview

Alzheimer's disease (AD) is a progressive neurodegenerative disorder and one of the leading causes of dementia worldwide. Mild Cognitive Impairment (MCI) is considered an early stage of cognitive decline, but not all MCI patients progress to Alzheimer's disease. Identifying individuals at high risk of conversion from MCI to AD is important for early intervention, treatment planning, and biomarker discovery.

This project develops a machine learning pipeline to predict Alzheimer's disease conversion using serum microRNA (miRNA) expression profiles. The analysis was performed using publicly available human data obtained from the NCBI Gene Expression Omnibus (GEO) database.

The project combines bioinformatics, data preprocessing, machine learning, dimensionality reduction, and biomarker analysis to investigate whether miRNA expression patterns can distinguish MCI converters from non-converters.

---

Dataset Information

Dataset Source

- Database: NCBI Gene Expression Omnibus (GEO)
- GEO Accession Number: GSE150693
- Organism: Homo sapiens (Human)

Study Description

The dataset contains serum miRNA expression profiles collected from patients diagnosed with Mild Cognitive Impairment (MCI). Patients were monitored over time and classified into two groups:

- MCI-C (Converters): Patients who later developed Alzheimer's disease.
- MCI-NC (Non-Converters): Patients who remained stable and did not convert to Alzheimer's disease.

Dataset Statistics

- Total Samples: 197
- MCI Converters (MCI-C): 83
- MCI Non-Converters (MCI-NC): 114
- Total miRNA Features: 2,562

---

Project Objectives

The main objectives of this project were:

1. Acquire and process Alzheimer's-related miRNA expression data from GEO.
2. Construct a machine learning-ready feature matrix.
3. Develop a classification model capable of predicting disease conversion.
4. Identify the most informative miRNA biomarkers.
5. Visualize sample distributions using Principal Component Analysis (PCA).
6. Evaluate model performance using standard machine learning metrics.

---

Methodology

Data Acquisition

The original GEO Series Matrix file (GSE150693_series_matrix.txt.gz) was downloaded from the NCBI GEO repository and imported into Python using Pandas.

Data Preprocessing

Several preprocessing steps were performed:

- Removal of metadata rows
- Extraction of miRNA expression values
- Construction of a feature matrix
- Transposition of the dataset
- Label generation for MCI-C and MCI-NC classes
- Feature scaling using StandardScaler

Machine Learning

A Random Forest Classifier was selected due to its ability to handle high-dimensional biological datasets.

Pipeline:

1. Train-Test Split (80:20)
2. Feature Standardization
3. Random Forest Model Training
4. Prediction on Unseen Test Data
5. Performance Evaluation

Dimensionality Reduction

Principal Component Analysis (PCA) was applied to reduce the 2,562-dimensional dataset into two principal components for visualization purposes.

Biomarker Discovery

Random Forest feature importance scores were used to identify the most influential miRNAs contributing to disease conversion prediction.

---

Results

Model Performance

Classification results:

- Accuracy: 62.5%
- Precision calculated for both classes
- Recall calculated for both classes
- F1-score calculated for both classes
- Confusion Matrix generated

PCA Visualization

PCA analysis revealed substantial overlap between MCI-C and MCI-NC samples, indicating that disease progression is driven by complex biological patterns rather than simple linear separation.

Top Candidate Biomarkers

Feature importance analysis identified multiple candidate miRNAs that contributed strongly to classification performance and may represent potential biomarkers associated with Alzheimer's disease progression.

---

Technologies and Libraries

Programming Language

- Python

Libraries

- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

---

Project Structure

Data/

- GSE150693_series_matrix.txt.gz (Original GEO dataset)
- alzheimers.csv.csv (Processed dataset)

Results/

- PCA_plot.png
- confusion_matrix.png
- classification_report.txt
- project_summary.txt
- top_miRNA_importance.csv

Notebook/

- Alzheimer_Pipeline.ipynb

Documentation/

- README.md

---

Key Achievements

- Successfully processed real-world Alzheimer's disease biomarker data.
- Developed a complete machine learning pipeline from raw GEO data.
- Classified MCI converters and non-converters using serum miRNA profiles.
- Achieved 62.5% prediction accuracy on unseen patient samples.
- Identified candidate miRNA biomarkers through feature importance analysis.
- Generated publication-style visualizations and performance reports.

---

Future Work

Potential improvements include:

- Support Vector Machine (SVM) implementation
- XGBoost classification
- Hyperparameter optimization
- K-fold cross-validation
- Multi-omics data integration
- Pathway enrichment analysis
- External validation using independent Alzheimer's datasets

---

Conclusion

This project demonstrates that serum miRNA expression profiles contain predictive information related to Alzheimer's disease progression. By integrating bioinformatics and machine learning approaches, it is possible to identify patterns associated with MCI-to-Alzheimer's conversion and discover candidate molecular biomarkers for future research.

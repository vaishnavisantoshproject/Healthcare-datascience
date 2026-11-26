# Healthcare Data Science: Lung Cancer Gene Expression Analysis and Classification

## Project Overview

This project focuses on applying Data Science, Statistical Analysis, and Machine Learning techniques to healthcare data for analyzing lung cancer gene-expression patterns.

The study uses gene-expression data from **The Cancer Genome Atlas (TCGA)** to investigate differences between two major types of lung cancer:

- Lung Adenocarcinoma (LUAD)
- Lung Squamous Cell Carcinoma (LUSC)

The primary objective is to identify Differentially Expressed Genes (DEGs) and explore whether gene-expression patterns can distinguish between these two cancer subtypes using Machine Learning.

## Objectives

- Analyze gene-expression patterns in lung cancer patients.
- Compare gene expression between LUAD and LUSC.
- Identify statistically significant Differentially Expressed Genes.
- Perform statistical analysis to understand gene-expression distributions.
- Visualize patterns using PCA, heatmaps, boxplots, and volcano plots.
- Develop a Logistic Regression model to classify cancer subtypes.
- Evaluate model performance using standard classification metrics.

## Dataset

**Data Source:** The Cancer Genome Atlas (TCGA)

The project uses two datasets:

1. **Gene Expression Dataset**
   - TCGA Lung HiSeqV2 gene-expression data.
   - Contains gene-expression measurements across patient samples.

2. **Clinical Dataset**
   - TCGA Lung Clinical Matrix.
   - Contains clinical information, including primary disease labels.

The datasets are used together to associate gene-expression profiles with their respective cancer subtypes.

## Technologies and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- Statsmodels

## Methodology

### 1. Data Loading and Preprocessing
- Loaded compressed gene-expression data.
- Loaded clinical information.
- Matched patient samples with their corresponding cancer subtype.
- Prepared the dataset for statistical analysis and machine learning.

### 2. Exploratory Data Analysis (EDA)
Performed exploratory analysis to understand gene-expression patterns using:
- Descriptive statistics
- Mean and variance analysis
- Skewness and kurtosis
- Boxplots
- Kernel Density Estimation (KDE)

### 3. Statistical Analysis
Applied statistical techniques to investigate gene-expression distributions:

- Shapiro-Wilk Test for normality.
- Q-Q plots to examine normality.
- Independent t-test to compare gene expression between cancer subtypes.
- Log Fold Change (logFC) calculation to measure differences in gene-expression levels.

### 4. Principal Component Analysis (PCA)
Applied PCA to reduce the dimensionality of gene-expression data and visualize sample distributions across the two cancer subtypes.

### 5. Differentially Expressed Gene Identification
Identified candidate Differentially Expressed Genes using:
- Log Fold Change.
- Statistical significance (p-value).

A volcano plot was generated to visualize gene-expression differences.

The analysis uses thresholds of:
- Absolute logFC > 2
- P-value < 0.05

### 6. Machine Learning – Logistic Regression
Developed a Logistic Regression classification model using selected gene-expression features.

The model aims to distinguish between:
- Lung Adenocarcinoma
- Lung Squamous Cell Carcinoma

### 7. Model Evaluation
Evaluated the classification model using:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix
- Classification Report

Also explored model coefficients to understand the contribution of selected gene features.

## Visualizations

The project includes:
- PCA plots
- Gene-expression boxplots
- KDE distribution plots
- Q-Q plots
- Volcano plots
- Gene-expression heatmaps
- Feature importance visualizations

## Project Structure

```text
Healthcare-Data-Science/
│
├── des_workshop_(2).py
│
├── Dataset/
│   ├── TCGA.LUNG.sampleMap_HiSeqV2.gz
│   └── TCGA.LUNG.sampleMap_LUNG_clinicalMatrix
│
├── Visualizations/
│
├── Results/
│
└── README.md
```

*Note: The dataset files are not included in this repository. The folder structure above is a suggested organization.*

## Installation and Execution

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Healthcare-Data-Science.git
```

### 2. Navigate to the Project Directory

```bash
cd Healthcare-Data-Science
```

### 3. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn statsmodels
```

### 4. Configure Dataset Paths

Update the dataset file paths in the Python script according to your local environment.

### 5. Run the Project

The original analysis was developed in Google Colab. Upload the datasets to your Google Drive and configure the paths before executing the notebook.

## Key Outcomes

The project explores the potential of gene-expression analysis for distinguishing between two lung cancer subtypes.

It combines statistical hypothesis testing, differential gene-expression analysis, dimensionality reduction, data visualization, and machine learning classification.

## Future Scope

- Explore additional machine learning algorithms.
- Apply advanced feature-selection techniques.
- Investigate biological relevance of selected genes.
- Validate results using independent datasets.
- Explore deep learning approaches for gene-expression classification.

## Disclaimer

This project is developed for academic and research purposes only. The analysis is not intended for clinical diagnosis, treatment recommendations, or medical decision-making.

## Acknowledgement

The project uses publicly available TCGA lung cancer research data. We acknowledge the researchers and institutions responsible for making these datasets available for scientific research.

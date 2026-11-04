
# District-Level Multidimensional Poverty and Health in India

**Team 08 | CS215 – Data Analysis and Interpretation**

## Overview

This project investigates the relationship between multidimensional poverty and health outcomes across districts in India. Using district-level data from the National Family Health Survey (NFHS-5), collected during 2019–2020, the project examines whether districts experiencing higher levels of multidimensional poverty also tend to experience poorer health outcomes.

The analysis focuses on understanding the strength and direction of associations between the Multidimensional Poverty Index (MPI) and selected health indicators. It also explores differences between districts, identifies potential outliers, and examines whether multidimensional poverty can serve as an indicator of health-related development.

## Research Question

How strongly is district-level multidimensional poverty associated with health indicators across districts in India, and which health indicators show the strongest relationship with MPI?

## Research Objectives

- Examine the association between district-level MPI and selected health indicators.
- Quantify the strength and direction of relationships using statistical measures.
- Compare linear and rank-based correlations to identify potential nonlinear or monotonic relationships.
- Investigate differences in health outcomes among districts with similar levels of multidimensional poverty.
- Identify outlier districts and explore possible explanations for their outcomes.
- Evaluate the limitations of using MPI as a standalone measure of health-related development.

## Research Hypothesis

The primary hypothesis is that districts with higher multidimensional poverty tend to experience poorer health outcomes.

However, the strength of this relationship may vary across health indicators. Some indicators may show a stronger association with MPI than others, reflecting differences in healthcare access, living conditions, and other socioeconomic factors.

The analysis will distinguish correlation from causation and acknowledge the influence of factors such as population characteristics, urbanization, and regional differences.

## Data Sources

The project uses district-level data from the following sources:

| Dataset | Purpose |
|---|---|
| National Family Health Survey – NFHS-5 | Source of district-level health and household indicators |
| Multidimensional Poverty Index (MPI) | Main explanatory variable representing multidimensional poverty |

The analysis uses NFHS-5 data collected during 2019–2020. The selected variables are based on the availability of comparable district-level observations.

## Methodology

The project follows a data-driven analytical workflow.

### 1. Data Collection and Preparation

- Obtain the district-level MPI and health indicator datasets.
- Inspect the datasets for missing values, duplicates, and inconsistencies.
- Standardize district identifiers and verify the compatibility of district names.
- Merge the datasets using appropriate district identifiers.
- Examine the completeness and comparability of the merged dataset.

### 2. Exploratory Data Analysis

- Examine the distributions of MPI and selected health indicators.
- Calculate descriptive statistics, including mean, median, standard deviation, minimum, and maximum.
- Identify unusual observations and potential outlier districts.
- Use visualizations to examine variation across districts.

### 3. Correlation Analysis

The project uses two correlation measures:

- **Pearson correlation coefficient (r):** Measures the strength and direction of a linear relationship between MPI and a health indicator.
- **Spearman rank correlation coefficient (ρ):** Measures the strength and direction of a monotonic relationship using ranked observations.

The two measures are compared to assess whether the observed relationships are approximately linear or whether rank-based associations provide additional insights.

### 4. Regression Analysis

Simple linear regression is used to examine the relationship between MPI and individual health indicators.

Regression results are interpreted in terms of the estimated association, direction of the relationship, and proportion of variation explained by the model.

### 5. Interpretation and Conclusion

The results are interpreted in the context of multidimensional poverty and health-related development.

The analysis discusses the strength of the observed relationships, potential outlier districts, and limitations of drawing conclusions from district-level observational data.

## Tools and Technologies

The project uses the following tools:

- **Python** for data analysis and scripting
- **Jupyter Notebook** for interactive analysis and documentation
- **pandas** and **NumPy** for data manipulation
- **Matplotlib** for data visualization
- **SciPy** for statistical analysis
- **Git and GitHub** for version control and collaboration

## Project Structure

```text
district-wealth-development/
├── data/
│   ├── raw/
│   └── clean/
├── notebooks/
│   └── CS215_MPI_Health_Analysis.ipynb
├── CHATS.md
├── reports/
├── requirements.txt
└── README.md
```

This structure may be updated as the project develops. Raw datasets may be excluded from version control where licensing, file size, or redistribution restrictions apply.

## Requirements and Setup

The project requires Python and the packages listed in `requirements.txt`. The notebook also uses SciPy for correlation and regression calculations, so ensure that `scipy` is included in the requirements file.

### 1. Clone the repository

```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Create and activate a virtual environment

```bash
python -m venv .venv
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

On Windows:

```bash
.venv\Scripts\activate
```

### 3. Install the dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```


### 4. Launch the notebook

```bash
jupyter notebook
```

Open `notebooks/CS215_MPI_Health_Analysis.ipynb` and run the cells.

The notebook expects the cleaned dataset to be available at:

```text
data/clean/MPI vs Health Indicators.xlsx
```

## Limitations and Challenges

The project acknowledges the following limitations:

- The analysis is based on district-level data and may not reflect individual-level relationships.
- The findings are observational and do not establish causal relationships.
- The availability and completeness of district-level observations may vary across indicators.
- Differences in district characteristics, population composition, and regional conditions may influence the observed relationships.
- MPI and certain health-related indicators may share underlying dimensions, potentially affecting the strength of their association.
- The analysis uses NFHS-5 data collected during 2019–2020 and does not establish how these relationships have changed over time.

## Expected Outcomes

The project aims to produce:

- A cleaned and integrated district-level dataset.
- Descriptive statistics for MPI and selected health indicators.
- Visualizations illustrating the relationships between MPI and health indicators.
- Pearson and Spearman correlation estimates.
- Regression results for individual health indicators.
- Identification and discussion of outlier districts.
- A conclusion assessing the association between multidimensional poverty and health-related development.

These outcomes represent the objectives of the analysis and do not imply any predetermined findings.

## Research Principle

The project prioritizes transparent data sources, reproducible analysis, and careful statistical interpretation. Conclusions will be limited to what the available data and methods support.

---

**Project:** District-Level Multidimensional Poverty and Health in India  
**Course:** CS215 – Data Analysis and Interpretation  
**Team:** 08  
**Data Source:** NFHS-5 (2019–2020)  
**Status:** Data analysis and interpretation

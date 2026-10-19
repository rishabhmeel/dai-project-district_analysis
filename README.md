## Environment Setup

### 1. Create a virtual environment

Ensure Python and `pip` are installed. Then run:

```bash
python -m venv venv
source venv/bin/activate
```

On Windows, activate it using:

```powershell
venv\Scripts\activate
```

### 2. Install dependencies

Install all dependencies listed in `requirements.txt`:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### 3. Generate or update `requirements.txt`

If you install additional packages or change package versions, update the dependency file using:

```bash
python -m pip freeze > requirements.txt
```

This records the installed packages and their versions so others can reproduce the Python environment.

### 4. Run the project

Activate the virtual environment and run the relevant Python script or notebook.

**Note:** The virtual environment itself (`venv/`) should not be committed to Git. Commit `requirements.txt` instead.

## We are using NFHS-5 data which was from the timeline 2019-2020

# District Wealth and Development Indicators in India

**Team 08 | Open Project Proposal**

## Overview

This project investigates the relationship between district-level economic prosperity and development indicators across India. It aims to understand whether wealthier districts tend to achieve better development outcomes and identify which indicators are most strongly associated with economic prosperity.

India's districts differ in their economic conditions, healthcare access, education, sanitation, and infrastructure. By combining district-level datasets and applying statistical analysis, the project seeks to identify meaningful patterns in these differences.

**Research question:** How strongly is district-level wealth associated with development indicators across districts in India, and which indicators best explain differences in district development?

## Research Objectives

- Examine the association between district-level wealth and development outcomes.
- Analyze differences in child health and health insurance coverage across districts.
- Explore additional indicators such as education, sanitation, infrastructure, and access to basic services, subject to data availability.
- Identify patterns, correlations, and outlier districts.
- Investigate whether similarly wealthy districts experience different development outcomes.
- Evaluate the limitations of wealth as a standalone measure of development.

## Research Hypothesis

The primary hypothesis is that districts with higher economic prosperity tend to perform better on selected development indicators. However, the strength of this relationship may vary across indicators and geographical regions.

The analysis will distinguish **correlation from causation** and consider factors such as population, urbanization, state policies, and regional differences.

## Data Sources

The project will use publicly available datasets with district-level coverage, subject to availability, reliability, and comparability.

| Dataset / Source                          | Purpose                                                                                             |
| ----------------------------------------- | --------------------------------------------------------------------------------------------------- |
| District-level prosperity or wealth index | Main explanatory variable representing economic well-being                                          |
| National Family Health Survey (NFHS)      | Source for district-level health and household indicators                                           |
| Child health indicators                   | Measure developmental outcomes related to child health                                              |
| Health insurance coverage                 | Examine access to health insurance and financial protection                                         |
| Additional development indicators         | Explore education, sanitation, infrastructure, and basic services where suitable data are available |

### Research References

1. Subramanya, V., et al. (2025). _Development and validation of a district-level index of socioeconomic development for India._ [DOI](https://doi.org/10.1101/2025.04.02.25325109)
2. _Progress on Sustainable Development Goal indicators in 707 districts of India: A quantitative mid-line assessment using the National Family Health Surveys, 2016 and 2021_ (2023). [Read paper](https://pmc.ncbi.nlm.nih.gov/articles/PMC10306006/)
3. Gouda, J., Gupta, A. K., and Yadav, A. K. _Association of child health and household amenities in high focus states in India: A district-level analysis._ [DOI](https://doi.org/10.1136/bmjopen-2015-007589)
4. National Family Health Survey, NFHS-5. [Official NFHS-5 portal](https://www.nfhsiips.in/nfhsuser/nfhs5.php)

_Note: Dataset selection is preliminary. Final variables and geographical coverage will depend on the availability of comparable district-level data._

## Methodology

The project will follow a data-driven workflow:

1. **Data collection:** Identify and obtain relevant wealth and development datasets.
2. **Data cleaning:** Handle missing values, standardize district identifiers, and check data quality.
3. **Dataset integration:** Merge datasets using compatible district identifiers and assess differences in administrative boundaries and reference years.
4. **Exploratory data analysis:** Examine distributions, summary statistics, and regional variation.
5. **Visualization:** Create scatter plots and other visualizations to explore relationships between variables.
6. **Correlation analysis:** Use Pearson and/or Spearman correlation coefficients to quantify associations.
7. **Regression analysis:** Where data quality and sample size permit, estimate the association between district wealth and individual development indicators.
8. **Interpretation:** Investigate outliers, compare districts with contrasting outcomes, and discuss limitations and potential confounding factors.

## Tools and Technologies

The planned technical stack includes:

- **Python** for data analysis and scripting
- **pandas** and **NumPy** for data manipulation
- **Matplotlib** and **Seaborn** for visualization
- **SciPy** (`scipy.stats`) for statistical analysis
- **statsmodels** and **scikit-learn** for regression and related analytical tasks, where appropriate
- **Git and GitHub** for version control and collaboration

R and interactive visualization tools such as Tableau, Power BI, Plotly, or Shiny may also be considered.

## Project Workflow

| Stage                   | Planned Activity                                                   |
| ----------------------- | ------------------------------------------------------------------ |
| Project design          | Refine the research question and select variables                  |
| Data collection         | Identify, collect, and document datasets                           |
| Data preparation        | Clean, standardize, and merge district-level data                  |
| Intermediate checkpoint | Review data availability, progress, and challenges                 |
| Statistical analysis    | Conduct exploratory analysis, correlation, and suitable regression |
| Results validation      | Verify the analysis pipeline and findings                          |
| Final deliverables      | Prepare the position paper, presentation, and video                |

The team will collaborate throughout the project, with responsibilities adjusted collectively based on progress and availability.

## Team Members

| Name               | Roll Number |
| ------------------ | ----------- |
| Rishabh            | 25B0931     |
| Sugam Kumar Thakur | 25B1058     |
| Aaryan Chavda      | 25B1065     |
| Arshdeep           | 25B1082     |

## Project Planning

- [Project planning spreadsheet](https://docs.google.com/spreadsheets/d/1WeEgMUot7anoarLgUrO869UfOqGmf7j51bWOTu9e4V0)

## Limitations and Challenges

The project anticipates several methodological challenges:

- Availability of a reliable and comparable district-level wealth measure.
- Differences in district boundaries and administrative definitions over time.
- Inconsistent reference years across datasets.
- Missing observations and differences in data quality.
- Potential confounding from urbanization, population characteristics, and state-level policies.
- The risk of interpreting statistical associations as causal relationships.

These issues will be documented and addressed during data preparation and interpretation.

## Proposed Repository Structure

```text
district-wealth-development/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_data_cleaning.ipynb
│   └── 03_statistical_analysis.ipynb
├── src/
│   ├── data_cleaning.py
│   ├── data_merging.py
│   └── analysis.py
├── figures/
├── reports/
├── requirements.txt
└── README.md
```

This is a proposed structure; files will be added as the project develops. Raw datasets may be excluded from version control where licensing, file size, or redistribution restrictions apply.

## Expected Outcomes

The project aims to produce:

- A cleaned and integrated district-level dataset, subject to data availability.
- Exploratory visualizations of wealth and development indicators.
- Correlation estimates between economic prosperity and selected outcomes.
- Regression results where methodologically appropriate.
- Comparisons of districts with contrasting development outcomes.
- A discussion of the strengths and limitations of wealth as an indicator of district development.

These are planned deliverables, not completed findings.

## Research Principle

The project will prioritize transparent data sources, reproducible analysis, and careful statistical interpretation. Conclusions will be limited to what the available data and methods support.

---

**Project:** District Wealth and Development Indicators in India  
**Team:** 08  
**Status:** Research proposal and data collection stage

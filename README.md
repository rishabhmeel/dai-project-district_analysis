# District-Level Multidimensional Poverty and Health in India

**Course:** CS215 – Data Analysis and Interpretation  
**Group:** 08  
**Mentor:** Namish Bansal

## Team Members

- Rishabh Meel — 25B0931
- Sugam Kumar Thakur — 25B1058
- Aaryan Chavda — 25B1065
- Arshdeep Singh — 25B1082

## Overview

This project investigates the relationship between district-level multidimensional poverty and selected health indicators across India.

The **Multidimensional Poverty Index (MPI)** measures poverty through overlapping deprivations in health, education, and living standards, rather than income alone.

**Research question:** How strongly, and in what direction, is MPI associated with health outcomes across Indian districts, and which indicators show the strongest associations?

The analysis is exploratory and observational. It describes statistical associations and does not establish causal effects.

## Data

The project combines district-level MPI data with health indicators from the National Family Health Survey (NFHS-5), collected during 2019–2021. The merged dataset contains **707 districts** and eight health indicators:

- Improved sanitation
- Menstrual hygiene
- Full vaccination
- Adequate diet among children aged 6–23 months
- Anaemia among women aged 15–49
- High blood sugar among men
- Tobacco use among women
- Alcohol use among men

Health indicators are expressed as percentages.

## Repository Structure

```text
.
├── data/
│   ├── clean/
│   │   └── MPI vs Health Indicators.xlsx
│   └── raw/
│       ├── datasheet.xls
│       └── india_district_mpi_nfhs4_nfhs5.xlsx
├── CS215_MPI_Health_Analysis...  # Main analysis notebook
├── data_loading.ipynb            # Data preparation and merging
├── ENVIRONMENT.md
├── README.md
└── requirements.txt
```

## Methodology

### Data preparation

The `data_loading.ipynb` notebook:

1. Loads the raw health-indicator and MPI spreadsheets.
2. Selects the eight health indicators and district identifiers.
3. Standardizes district and state names, accounting for spelling differences and renamed districts.
4. Handles specially encoded values: suppressed values are treated as missing, and parenthesized negative estimates are converted to positive percentages.
5. Merges the datasets and saves the cleaned file to `data/clean/MPI vs Health Indicators.xlsx`.

Missing values are not imputed. Analyses use the available observations for each pair of variables.

### Analysis

The main notebook uses descriptive statistics, visualizations, Pearson and Spearman correlations, and simple linear regression. It also plots the MPI distribution and visualizes the strongest negative associations with fitted trendlines.

## Key Findings

- MPI has a mean of **0.065** and a median of **0.053**. Its distribution is concentrated at lower values, with a right tail toward higher deprivation.
- Menstrual hygiene has the strongest negative Pearson correlation with MPI (**r = −0.748**), followed by improved sanitation (**r = −0.656**).
- Full vaccination (**r = −0.324**), high blood sugar among men (**r = −0.314**), and adequate diet (**r = −0.179**) have weaker negative correlations.
- Anaemia among women (**r = 0.242**) and tobacco use among women (**r = 0.222**) have modest positive correlations.
- Alcohol use among men has little observed linear association with MPI (**r = −0.025**, p = 0.511).

The fitted regressions estimate that a 0.1 increase in MPI is associated with a decrease of approximately **20.464 percentage points in menstrual hygiene** and **16.835 percentage points in improved sanitation**. These describe observed district-level relationships and should not be interpreted as causal effects.

## Tools and Libraries

- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- SciPy

## Setup and Usage

Clone the repository and move into its directory:

```bash
git clone <repository-url>
cd <repository-folder>
```

Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Run `data_loading.ipynb` to prepare the cleaned dataset, then run the main analysis notebook. The cleaned spreadsheet should be available at:

```text
data/clean/MPI vs Health Indicators.xlsx
```

## Limitations

- The analysis is observational and aggregated by district; it cannot establish causality or individual-level relationships.
- District averages may hide substantial variation within districts.
- Other regional, demographic, and socioeconomic factors may influence both MPI and health outcomes.
- Sanitation is also represented within MPI, so its association with MPI may partly reflect conceptual overlap.
- The data describe a specific survey period and may not represent current conditions.

## Conclusion

District MPI is most strongly negatively associated with menstrual hygiene and improved sanitation. Associations with vaccination, high blood sugar among men, and adequate diet are weaker. Anaemia and tobacco use among women show positive associations, while alcohol use among men has little observed association.

Overall, the project describes how MPI and selected health indicators vary together across districts; it does not establish causal relationships.

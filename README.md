# Legal Cooperative Adoption Under Law 13-21: Evidence from Rif Farmer Households

**Author:** Your Name  

**Affiliation:** Your University  

**Contact:** your.email@univ.edu  

**Last updated:** 2026-06-02

---

## Abstract

This repository contains all data and analysis code for a study of legal cooperative
adoption among cannabis farmers in Morocco's Rif region following Law 13-21 (2021).
We use logistic regression and propensity score matching to identify determinants of
formalization and estimate the causal income effect of joining the legal market.

## Repository Structure

```
/
├── data/
│   ├── morocco_cannabis_master.csv          Primary analysis file (n=800 households)
│   ├── morocco_cannabis_survey_clean.csv    Cleaned household survey
│   ├── morocco_cannabis_anrac_clean.csv     ANRAC license data 2021-2024
│   ├── morocco_cannabis_unodc_clean.csv     UNODC production data 1998-2023
│   ├── morocco_cannabis_emcdda_panel.csv    EMCDDA European market panel
│   ├── morocco_cannabis_table1.csv          Table 1: Descriptive statistics
│   ├── morocco_cannabis_table2.tex          Table 2: Regression results (LaTeX)
│   ├── morocco_cannabis_logit_mfx.csv       Marginal effects (Model 3)
│   ├── morocco_cannabis_psm_results.csv     PSM ATT estimates
│   └── morocco_cannabis_subgroup_analysis.csv  Subgroup adoption rates
├── figures/
│   ├── morocco_cannabis_pub_figure1_legal_market.pdf
│   ├── morocco_cannabis_pub_figure2_adoption_barriers.pdf
│   ├── morocco_cannabis_pub_figure3_marginal_effects.pdf
│   ├── morocco_cannabis_pub_figure4_subgroups.pdf
│   ├── morocco_cannabis_pub_figure5_income_change.pdf
│   ├── morocco_cannabis_pub_figure6_psm_balance.pdf
│   └── morocco_cannabis_pub_figure7_unodc_emcdda.pdf
├── notebooks/
│   ├── morocco_cannabis_01_data.ipynb       Data acquisition
│   ├── morocco_cannabis_02_clean.ipynb      Cleaning and validation
│   ├── morocco_cannabis_03_eda.ipynb        Exploratory analysis
│   ├── morocco_cannabis_04_model.ipynb      Statistical modeling
│   ├── morocco_cannabis_05_figures.ipynb    Publication figures
│   └── morocco_cannabis_06_export.ipynb     This file
└── docs/
    └── index.html                           GitHub Pages report
```

## How to Reproduce

1. Open [00_master_setup.ipynb](notebooks/) in Google Colab
2. Edit Cell 1 with your project name and GitHub credentials
3. Run all cells (approx. 2 minutes)
4. Run notebooks 01 through 06 in order

All notebooks are self-contained and include path bootstrap cells,
so they also run independently without the master setup.

## Data Sources

| Dataset | Source | Access |
|---|---|---|
| Farmer household survey | Primary data collection | This repo |
| ANRAC license data | www.anrac.gov.ma | Public |
| UNODC production estimates | unodc.org/wdr | Public |
| EMCDDA seizures and prices | emcdda.europa.eu/data/stats | Public |
| World Bank indicators | data.worldbank.org | API |
| Literature corpus | openalex.org | API (free) |

## Key Variables

| Variable | Description | Type |
|---|---|---|
| joined_legal_cooperative | Outcome: joined ANRAC cooperative (0/1) | Binary |
| land_size_ha | Agricultural land holding (hectares) | Continuous |
| distance_to_anrac_km | Distance to nearest ANRAC office (km) | Continuous |
| education_yrs | Years of formal education | Continuous |
| prior_arrests | Number of cannabis-related arrests | Count |
| household_income_usd | Annual household income pre-law (USD) | Continuous |
| info_access_legal | Aware of legal market process (0/1) | Binary |
| region | Province: Chefchaouen / Al-Hoceima / Ouazzane | Categorical |

## Citation

If you use this code or data, please cite:

> Your Name (2026). *Legal Cooperative Adoption Under Law 13-21: Evidence from Rif Farmer Households*.
> Your University. https://github.com/hsmalling/research

## License

Code: MIT License  |  Data: CC BY 4.0

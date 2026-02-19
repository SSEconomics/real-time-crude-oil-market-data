# Real-Time Data Vintages for the Global Crude Oil Market

[![DOI](https://zenodo.org/badge/DOI/placeholder.svg)](https://doi.org/10.5281/zenodo.placeholder)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## Overview
This repository hosts the **living dataset** of real-time data vintages for the global crude oil market. While many datasets provide ex-post revised data, this repository maintains the actual information available to policymakers and market participants at specific points in history.

* **File:** `MASTERFILE_Real_Time_Data.xlsx`
* **Update Frequency:** First Wednesday of every month.
* **Data Cutoff:** Last day of each month at 11:59 pm EST.

By using these vintages, researchers can conduct genuine out-of-sample forecasting exercises and structural modeling without the risk of look-ahead bias.


---

## 📂 Replication vs. Living Data

This repository is intended for **ongoing research and new forecasting exercises**.

* **For New Research:** Use the `MASTERFILE` in this repository for the most up-to-date vintages.
* **For Paper Replication:** To perfectly replicate the results in **Benyo, Ellwanger, and Snudden (2026)**, please use the frozen version of the data and code provided in the official replication package:
    * [**Official Replication Package (ICPSR)**](https://doi.org/10.3886/E218641V4) (Includes Stata and MATLAB code).

---

## 📝 How to Cite

If you use this data in your research, please provide the **Primary Citation** below. Additional citations are required if your analysis focuses on specific historical periods or variables.

### Primary Citation (Required)
> Benyo, E., R. Ellwanger, and S. Snudden (2026). A reappraisal of real-time forecasts of the real price of oil. *Economic Inquiry*, 64(1): 167-176.

<details>
<summary><b>Supporting Citations (Click to expand)</b></summary>

* **For vintages prior to 2010M11:** Baumeister, C., and Kilian, L. (2012). Real-time forecasts of the real price of oil. *Journal of Business & Economic Statistics*, 30(2): 326-336.
* **For Refiner's Acquisition Cost (RAC) methodology:** Ellwanger, R. and S. Snudden (2023a, 2023b). *Journal of Banking and Finance* / *The Energy Journal*.
* **For 1973 Nominal RAC imputation:** Mork, K. A. (1989). *Journal of Political Economy*, 97(3): 740-744.
</details>

* [Replication Package: Benyo et al. (2026) - *A reappraisal of real-time forecasts of the real price of oil*](https://doi.org/10.3886/E218641V4)

<details>
<summary><b>Click to copy BibTeX entries</b></summary>

```bibtex
@article{benyo2026reappraisal,
  title={A reappraisal of real-time forecasts of the real price of oil},
  author={Benyo, E. and Ellwanger, R. and Snudden, S.},
  journal={Economic Inquiry},
  volume={64},
  number={1},
  pages={167--176},
  year={2026}
}

@article{baumeister2012real,
  title={Real-time forecasts of the real price of oil},
  author={Baumeister, C. and Kilian, L.},
  journal={Journal of Business \& Economic Statistics},
  volume={30},
  number={2},
  pages={326--336},
  year={2012}
}

@article{ellwanger2023rw,
  title={Forecasts of the Real Price of Oil Revisited: Do they Beat the Random Walk?},
  author={Ellwanger, R. and Snudden, S.},
  journal={Journal of Banking and Finance},
  volume={154},
  pages={106962},
  year={2023}
}

@article{ellwanger2023futures,
  title={Futures Prices are Useful Predictors of the Spot Price of Crude Oil},
  author={Ellwanger, R. and Snudden, S.},
  journal={The Energy Journal},
  volume={44},
  number={4},
  pages={45--62},
  year={2023}
}

@article{mork1989oil,
  title={Oil and the macroeconomy when prices go up and down: an extension of Hamilton's results},
  author={Mork, K. A.},
  journal={Journal of Political Economy},
  volume={97},
  number={3},
  pages={740--744},
  year={1989}
}

```

</details>

## Data Dictionary

The spreadsheet contains 5 real-time variables, and all the variables are at a monthly frequency.

| Variable | Unit | Delay | Release Time | Notes / Source |
| --- | --- | --- | --- | --- |
| `Nominal RAC` | Dollars per Barrel | 2 months | Last week of month | EIA MER. Imputation for 1973 follows Mork (1989). Pre-2010M11 from Baumeister & Kilian (2012). |
| `US Crude Oil/Petrol Inventories` | Million Barrels | 1 month | Last week of month | EIA MER. Pre-2010M11 from Baumeister & Kilian (2012). |
| `OECD Petroleum Inventories` | Million Barrels | 3 months | First week of month | EIA MER and International Data Browser. Pre-2010M11 from Baumeister & Kilian (2012). |
| `World Oil Production` | Millions of barrels per day | 4 months (post-2019M07) | First week of month | EIA MER and International Data Browser. Pre-2010M11 from Baumeister & Kilian (2012). |
| `US CPI` | Seasonally adjusted index | 1 month | Middle of the month | Federal Reserve Bank of Philadelphia (PCPI). |

## Vintage Completeness (Color Coding Legend)

We distinguish the data by 5 different colors based on the way that the data is collected for a particular vintage:

* **Green:** The full historical vintage is directly observed for that particular month. This implies that the entire historical series was downloaded at that point in time.
* **Grey:** The data was constructed from the pdf files of the data rather than the original spreadsheet. These cases include all revisions.
* **Blue:** This indicates that the data range had some revisions made but we were able to deduce the data exactly using surrounding vintages.
* **Orange:** This is the case where we were not able to observe the actual data itself and had to use information to that point in time to fill in missing values.
* **Purple:** Used to show in Baumeister and Kilian (2012) where revisions occurred but were not reflected in the data.

---

## Related Resources

* [Backcasted Crude Oil Prices](https://github.com/SSEconomics/backcasted-crude-oil-prices) - Spot prices for Brent and WTI (not subject to real-time revision).
* [SSEconomics GitHub](https://www.google.com/search?q=https://github.com/SSEconomics) - More tools for empirical macroeconomics.

---

## Quick Start: Code & Examples *(Coming Soon!)*

To ensure broad accessibility, starter code will be provided in both **R** and **Stata**. These scripts are currently in development and will be uploaded shortly.

### [R Users]

See `scripts/analysis_r.R` *(Coming Soon)*.

### [Stata Users]

See `scripts/analysis_stata.do` *(Coming Soon)*.




# Real-Time Data Vintages for the Global Crude Oil Market

[![DOI](https://zenodo.org/badge/DOI/placeholder.svg)](https://doi.org/10.5281/zenodo.placeholder)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## Overview
This repository contains the real-time data vintages for the global crude oil market, provided in `MASTERFILE_Real_Time_Data.xlsx`. This data package is updated monthly using real time data available on the last day of each month at 11:59 pm EST. This data package is updated on the first Wednesday of every month. 

By providing actual real-time vintages rather than heavily revised ex-post data, this repository allows researchers to conduct genuine out-of-sample forecasting exercises without look-ahead bias. Note that monthly average and end-of-month spot prices for Brent and WTI crude oil are not subject to real-time revision and are reported in a [separate data package](https://github.com/SSEconomics/backcasted-crude-oil-prices).

## How to Cite
When using this data in your research or analysis, please cite the appropriate following sources:

**For the real-time data for the global crude oil market, please cite:**
> Benyo, E., R. Ellwanger, and S. Snudden (2026). A reappraisal of real-time forecasts of the real price of oil. *Economic Inquiry*, 64(1): 167-176.

**For vintages prior to 2010M11, please cite:**
> Baumeister, C., and Kilian, L. (2012). Real-time forecasts of the real price of oil. *Journal of Business & Economic Statistics*, 30(2): 326-336.

**For the real-time Refiner's Acquisition Cost (RAC) data, please cite:**
> Ellwanger, R. and S. Snudden, (2023a). Forecasts of the Real Price of Oil Revisited: Do they Beat the Random Walk? *Journal of Banking and Finance*, 154(106962): 1-8.
> 
> Ellwanger, R. and Snudden, S. (2023b). Futures Prices are Useful Predictors of the Spot Price of Crude Oil. *The Energy Journal*, 44(4): 45-62.

**If utilizing the imputed 1973 Nominal RAC data, please also cite:**
> Mork, K. A. (1989). Oil and the macroeconomy when prices go up and down: an extension of Hamilton's results. *Journal of Political Economy*, 97(3): 740-744.

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

## Quick Start: Code & Examples

To ensure broad accessibility, starter code is provided in both **R** and **Stata**.

### [R Users]

See `scripts/analysis_r.R`.

### [Stata Users]

See `scripts/analysis_stata.do`.

## Replication Materials

This repository is maintained as a living dataset for ongoing research and forecasting. If you are looking to perfectly replicate the results of the original papers, please use the static replication packages available on my [research page](https://stephensnudden.com/research/):

* [Replication Package: Benyo et al. (2026) - *A reappraisal of real-time forecasts of the real price of oil*](https://doi.org/10.3886/E218641V4)



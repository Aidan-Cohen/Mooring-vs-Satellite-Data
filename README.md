In Situ vs. Satellite-Derived pCO2 Estimates in the California Current System
Overview

This project compares partial pressure of CO2 (pCO2) measured directly by an ocean mooring against pCO2 estimated from satellite-derived chlorophyll and sea surface temperature (SST) data, using published empirical formulas. The goal is to evaluate how well remote-sensing-based estimates track real, in-situ measurements — which matters because satellite data can cover far larger areas and longer time spans than moorings can, but only if the estimates are reliable.

Data
In-situ mooring data (2010–2023): measured xCO2 (seawater, wet) from a CCE1 mooring located at 122°W, 33°N
Satellite data: chlorophyll concentration, sea surface temperature, and productivity from NOAA ERDDAP satellite products
Data covers overlapping time periods to allow direct comparison between measured and calculated values
Methods

The analysis (mooring vs calculated.Rmd) was conducted in R and includes:

Data cleaning of satellite products (removing header/unit rows, converting types, handling missing values)
Applying published empirical formulas (from prior oceanographic literature) to convert satellite chlorophyll and SST into estimated pCO2 values
Random sampling of mooring records to match against satellite-derived estimates for comparable dates (e.g., January, December/January)
Linear regression and ANOVA comparing calculated (satellite-derived) pCO2 against measured (in-situ mooring) pCO2
Pearson correlation to quantify the strength of agreement between the two data sources
Visual comparison via scatterplots and histograms of the distributions
Skills Demonstrated
Working with real-world environmental/oceanographic datasets (NOAA ERDDAP, mooring buoy data)
Data cleaning and wrangling of messy, multi-source time series data
Applying domain-specific empirical formulas from scientific literature
Linear regression, ANOVA, and correlation analysis to validate one data source against another
Data visualization in base R
Files
mooring vs calculated.Rmd — main analysis notebook
mooring2010-2023_CCE1_122W_33N.csv — in-situ mooring pCO2 measurements
erdMWchlamday_*.csv — satellite-derived chlorophyll data
erdMWsstdmday_*.csv — satellite-derived SST data
erdMH1ppmday_*.csv — satellite-derived productivity data
CCE1_122W_33N_Dec2009_Sep2010.csv — additional mooring data for an earlier time window
How to Run

Open mooring vs calculated.Rmd in RStudio (or Posit Cloud) and knit to PDF. All CSV files should be in the same directory as the .Rmd file.

Notes

This was an exploratory analysis; some variable names and intermediate steps reflect iterative data exploration rather than a final polished pipeline.

What Factors Contribute to Runs Batted In (RBI) in Major League Baseball?

Authors: Omar Aguilar Razo, Aidan Cohen

Overview

This project uses multiple linear regression to examine which offensive statistics — batting average (AVG), slugging percentage (SLG), and on-base percentage (OBP) — best predict runs batted in (RBI) for MLB players. It also investigates whether the MLB's 2023 pitch clock rule change (15/20-second pitch timer) had a measurable effect on these relationships by comparing models built on 2022 (pre-rule) and 2023 (post-rule) season data.

Data
Player-level batting statistics for the 2022 and 2023 MLB seasons, sourced from Baseball Savant / MLB Statcast leaderboards
Filtered to players with at least 500 plate appearances in the given season
Variables: RBI, batting average, slugging percentage, on-base percentage
Methods

The analysis (410_project.Rmd) was conducted in R and includes:

Multiple linear regression predicting RBI from AVG, SLG, and OBP, fit separately for the 2022 and 2023 seasons
Regression diagnostics: QQ plots to check normality of residuals, residuals-vs-fitted plots to check independence and constant variance, Cook's distance to check for outliers, and VIF to check for multicollinearity
Confidence interval comparison for the AVG and SLG coefficients across seasons, to test whether the pitch clock rule shifted their relationship to RBI
Exploratory scatterplots and boxplots comparing predictor distributions across years
Key Findings
Slugging percentage was the strongest, most consistent predictor of RBI in both seasons.
Batting average was a significant predictor in 2023 but not in 2022, while on-base percentage was not significant in either season.
95% confidence intervals for the AVG and SLG coefficients overlapped between 2022 and 2023, indicating no statistically significant shift in these relationships.
Conclusion: the 2023 pitch clock rule does not appear to have meaningfully changed how batting average, slugging percentage, or on-base percentage relate to RBI production.
Noted limitation: the study only examined batter-side statistics; incorporating pitcher statistics could better isolate the pitch clock's effect, since the rule most directly affects pitchers.
Skills Demonstrated
Multiple linear regression and model interpretation
Regression assumption checking (normality, independence, homoscedasticity, multicollinearity, outliers)
Confidence interval construction and comparison across groups
Data wrangling and visualization in R
Applied sports analytics / sabermetrics
Files
410_project.Rmd — main analysis and report
2022stats.csv, 2023stats.csv — MLB player batting statistics for each season
How to Run

Open 410_project.Rmd in RStudio (or Posit Cloud) and knit to HTML or Word. Both CSV files should be in the same directory as the .Rmd file.

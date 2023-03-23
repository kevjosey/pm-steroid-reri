# Effects of PM2.5 and Corticosteroid Use on Cardiovascular and Thromboembolic Events Among Older Adults: Evidence of Drug-Environment Interaction

This repository contains code used to fit history adjusted marginal structural Cox models with a time-to-event outcome. We use this model to estimate the risks to cardiovascular and thromboembolic events (CTE) caused by exposure to fine particulate matter (PM2.5) and corticosteroids (steroids) for high-risk older adults receiving Medicare services. Below is a detailed description of the various scripts, which we have divided into two parts. The scripts in the root directory contain the necessary functions for constructing the inverse probability weights and for evaluating additive interactions with a Cox proportional hazard model. The code used to evaluate the PM2.5/Steroid interactions can be found in the [`Steroids`](https://github.com/kevjosey/pm-steroid/blob/main/Steroids/) directory.

### Functions
[`interaction.R`](https://github.com/kevjosey/pm-steroid/blob/main/Functions/interaction.R) Functions for evaluating additive and multiplicative interactions. 

[`ipw_fun.R`](https://github.com/kevjosey/pm-steroid/blob/main/Functions/ipw_fun.R) Functions for generating inverse probability weights (with Random Forest or GEE). 

### Steroids
[`Steroids/descriptives.R`](https://github.com/kevjosey/pm-steroid/blob/main/Steroids/descriptives.R) Contains code for finding descriptive statistics that populate Tables 1, 2, and 3. 

[`Steroids/ipw_models.R`](https://github.com/kevjosey/pm-steroid/blob/main/Steroids/ipw_models.R) Code for transforming data (wide-format) into a counting process with season/drug-quarter changes. Also includes the code that fits the random forest models of the (generalized) propensity scores used to construct the inverse probability weights.

[`Steroids/cox_models.R`](https://github.com/kevjosey/pm-steroid/blob/main/Steroids/cox_models.R) Code for fitting the proportional hazard models relating PM2.5 and steroids to each of the six health outcomes that we examined in the manuscript.

[`Steroids/output.R`](https://github.com/kevjosey/pm-steroid/blob/main/Steroids/output.R) Creates tables and figures from the fitted proportional hazard model.

### Data
For data privacy reasons, the Medicare data used in this study cannot be made publicly available, but interested parties can request access by applying through the US Centers for Medicare and Medicaid Services. The PM2.5 exposure data are publicly available at the following link: https://doi.org/10.7927/0rvr-4538. Area-level covariates used herein are also publicly available from the US Census Bureau website.

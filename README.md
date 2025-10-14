# Bay-Area-Carnivore-Cognition

This repository contains all raw data and scripts for the data analysis implemented in Stanton *et al.* (2026) titled *XXXXXXXXX* and published in *XXXXXXXXXX*.

Please find below a description of all raw and clean data sets and the scripts used to format the raw data, run the models, and create the figures presented in the manuscript.

## Data Files

In the `Data` folder, you will find two data files:

`Q1_Summary_All_DummyRows_Max_07282025` and `Q1_Summary_Firsts_DummyRows_Max_07282025`. Both data files contain raw data from problem-solving attempts. The Summary_All data sheet contains all observations (i.e., all trials) whereas the Summary_Firsts datasheet contains only first-attempt observations (i.e., only first trials).

| Column                     | Description |
|----------------------------|-------------|
| Key                        |             |
| Species                    |             |
| Subject                    |             |
| Location                   |             |
| Home                       |             |
| ObservationNumber          |             |
| Date                       |             |
| Time                       |             |
| Photoperiod                |             |
| Weather                    |             |
| VisibilityIssue            |             |
| Arrival                    |             |
| Condition                  |             |
| NumSubjectsInObservation   |             |
| Interference               |             |
| AggressionSeen             |             |
| Dog                        |             |
| Coyote                     |             |
| PuzzleReset                |             |
| TrialLengthAvg             |             |
| TrialLengthMax             |             |
| PropVigilantAvg_RT         |             |
| PropVigilantMax_RT         |             |
| LookAtCamera_RT            |             |
| Touch_RT                   |             |
| WorkTimeAvg_PS             |             |
| WorkTimeMax_PS             |             |
| Urinate                    |             |
| TotalExplorationAvg_RT     |             |
| TotalExplorationMax_RT     |             |
| ExploratoryDiversityAvg_PS |             |
| ExploratoryDiversityMax_PS |             |
| ActivityRateAvg_PS         |             |
| ActivityRateMax_PS         |             |
| Solve_PS                   |             |
| WasSolveOffCamera          |             |
| FinalSolverofLocation      |             |
| Solve_PS_Binary            |             |
| TrialNumber_RT             |             |
| TrialNumber_PS             |             |
| Dummy                      |             |

## Scripts

The scripts for the full workflow are available as Rmd files in the `Code` folder. All files are R scripts that were run in R version 4.2.1. The output of the models are not stored on GitHub due to the large file sizes, but can be generated on your own device, or are available for download on Dryad Digital Repository (DOI: XXXXXX).

`Q1-All-Trials.Rmd`: this script uses the *brms* package to construct random-intercept models to compare species-level differences in baseline risk-taking and problem-solving behaviors using all observations (i.e., all trials). The script also generates figures and a summary table of model output.

`Q1-First-Attempts.Rmd`: this script uses the *brms* package to construct random-intercept models to compare species-level differences in baseline risk-taking and problem-solving behaviors using only first observations (i.e., first trials). The script also generates figures and a summary table of model output.

`Q2-Problem-Solving.Rmd`: this script uses the *brms* package to construct random-slope models to assess within-species and among-species effects of boldness, exploration, and effort on problem-solving success. The script also runs a simulation analysis to validate excluding testing location as a random effect from models; generates composite behavioral scores for boldness, exploration, effort from raw observational data; and generates figures and a summary table of model output.

## Model Output

The output of the models are not stored on GitHub in the `Model_Output` folder, but can be generated on your own device, or are available to download on Dryad Digital Repository (DOI: XXX). The `.rds` files that can be downloaded from Dryad are described below.

In the `Q1-All-Attempts` folder:

> `mod.prop.vig.all.rds`: random-intercept model for proportion of time spent vigilant by the subject using all trials
>
> `mod.look.cam.all.rds`: random-intercept model for whether the subject looked at the camera using all trials
>
> `mod.touch.all.rds`: random-intercept model for whether the subject touched the puzzle using all trials
>
> `mod.tot.exp.all.rds`: random-intercept model for total exploration exhibited by the subject using all trials
>
> `mod.exp.div.all.rds`: random-intercept model for exploratory diversity exhibited by the subject using all trials
>
> `mod.work.time.all.rds`: random-intercept model for total work time of the subject using all trials
>
> `mod.act.rate.all.rds`: random-intercept model for activity rate of the subject using all trials
>
> `mod.solve.all.rds`: random-intercept model for whether the subject solved the puzzle using all trials

In the `Q1-First-Attempts` folder:

| `mod.prop.vig.rds`: random-intercept model for proportion of time spent vigilant by the subject using only first attempt trials
| `mod.look.cam.rds`: random-intercept model for whether the subject looked at the camera using only first attempt trials
| `mod.touch.rds`: random-intercept model for whether the subject touched the puzzle using only first attempt trials
| `mod.tot.exp.rds`: random-intercept model for total exploration exhibited by the subject using only first attempt trials
| `mod.exp.div.rds`: random-intercept model for exploratory diversity exhibited by the subject using only first attempt trials
| `mod.work.time.rds`: random-intercept model for total work time of the subject using only first attempt trials
| `mod.act.rate.rds`: random-intercept model for activity rate of the subject using only first attempt trials
| `mod.solve.rds`: random-intercept model for whether the subject solved the puzzle using only first attempt trials

In the `Q2-Problem-Solving` folder:

| `mod.boldness.rds`: random-slope model for effect of boldness on problem-solving success
| `mod.exploration.rds`: random-slope model for effect of exploration on problem-solving success
| `mod.effort.rds`: random-slope model for effect of effort on problem-solving success

## Figures

This folder contains figures generated from scripts in the `Code` folder.

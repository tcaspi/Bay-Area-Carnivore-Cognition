# Bay-Area-Carnivore-Cognition

This repository contains all raw data and scripts for the data analysis implemented in Stanton *et al.* (2026) titled *Traits associated with novel foraging success in urban mesopredators* and published in *Scientific Reports*. The GitHub repository associated with this manuscript is available at <https://github.com/tcaspi/Bay-Area-Carnivore-Cognition>.

Please find below a description of all raw and clean data sets and the scripts used to format the raw data, run the models, and create the figures presented in the manuscript. To access the files, download `Bay-Area-Carnivore-Cognition-main.zip` for all data sets, scripts, and figures and `Model_Output.zip` for model output.

## Data Files

In the `Data` folder, you will find three data files:

`Q1_Summary_All_DummyRows_Max_07282025_Anonymized` and `Q1_Summary_Firsts_DummyRows_Max_07282025_Anonymized`. Both data files contain raw data from problem-solving attempts. The Summary_All data sheet contains all observations (i.e., all trials) whereas the Summary_Firsts datasheet contains only first-attempt observations (i.e., only first trials).

| Column | Description |
|---------------------------|---------------------------------------------|
| Key | **REMOVE?** |
| Species | Species of the subject. |
| Subject | **ASK LAUREN** |
| Location\* | Identifier for the study location where the observation occurred. |
| Home | Whether or not the study location was a private residence. |
| ObservationNumber | **??? Is this trials is is something else ASK LAUREN** |
| Date | Date on which the observation occurred. |
| Time | Time at which the observation occurred. |
| Photoperiod | Whether the observation occurred during the day time or night time. |
| Weather | Weather conditions during the observation. **(clear, rainy, precip, rainy/damp, just rained, foggy) - these need clarification** |
| VisibilityIssue | Whether or not the subject was out of the camera's view for any part of the observation |
| Arrival | Whether or not the subject in the observation was the first to arrive to the puzzle ("First") or other animals had previously visited the puzzle ("Not First") |
| Condition | Social condition of the subject: whether it was observed alone or in a group. |
| NumSubjectsInObservation | Number of subjects present during the observation. |
| Interference | **ASK LAUREN** |
| AggressionSeen | **ASK LAUREN** |
| Dog | Whether a dog ever visited the puzzle or not. **before the subject's observation? after the subjects observation? ASK LAUREN** |
| Coyote | **\^SAME AS ABOVE ASK LAUREN** |
| PuzzleReset | **ASK LAUREN** |
| TrialLengthAvg | Length in seconds of the trial. Where a group of animals were observed, this represents the average trial length across the group. **Length from when the animal enters the screen/camera or actually attempts solving or what? Need to defin what trial means...ASK LAUREN** |
| TrialLengthMax | Length in seconds of the trial. Where a group of animals were observed, this represents the maximum trial length by any individual in the group. **SAME ISSUE AS ABOVE ASK LAUREN. ARE MAXIMUMS PER ANY INDIVIDUAL ANIMAL OR CUMULATIVE ACROSS THE GROUP??** |
| PropVigilantAvg_RT | Proportion of time spent vigilant calculated as the duration of time spent vigilant (seconds) divided by the total observation time (seconds). Where a group of animals were observed, this represents the average proportion of time spent vigilant across the group. |
| PropVigilantMax_RT | Proportion of time spent vigilant calculated as the duration of time spent vigilant (seconds) divided by the total observation time (seconds). Where a group of animals were observed, this represents the maximum proportion of time spent vigilant by any individual in the group. **ARE MAXIMUMS PER ANY INDIVIDUAL ANIMAL OR CUMULATIVE ACROSS THE GROUP??** |
| LookAtCamera_RT | Binary: 1 if the subject ever looked at the camera during the observation, otherwise 0. |
| Touch_RT | Binary: 1 if the subject ever touched the puzzle during the observation, otherwise 0. |
| WorkTimeAvg_PS | Average amount of time in seconds the subject was alert and engaged with the puzzle across problem-solving trials. Where a group of animals were observed, this represents the average work  time across the group. |
| WorkTimeMax_PS | Maximum observed amount of time in seconds the subject was alert and engaged with the puzzle across problem-solving trials. Where a group of animals were observed, this represents the maximum work time by any individual in the group. **ARE MAXIMUMS PER ANY INDIVIDUAL ANIMAL OR CUMULATIVE ACROSS THE GROUP (E.G., ONE RACCOON'S WORK TIME WAS 50 SECONDS OR ALL RACCOONS TOGETHER HAD A WORK TIME OF 200 SECONDS)??** |
| Urinate | Indicator of whether the subject urinated during the observation. |
| TotalExplorationAvg_RT | Average total number of exploratory behaviors (e.g., paw, pull, push, roll, etc.) recorded across the trial. Where a group of animals were observed, this represents the average total of exploratory behaviors observed across the group. |
| TotalExplorationMax_RT | Maximum total number of exploratory behaviors (e.g., paw, pull, push, roll, etc.) recorded across risk-taking trials. Where a group of animals were observed, this represents the maximum number of exploratory behaviors exhibited by any individual in the group. **ARE MAXIMUMS PER ANY INDIVIDUAL ANIMAL OR CUMULATIVE ACROSS THE GROUP (E.G., ONE RACCOON'S TOTAL EXPLORATION WAS 5 OR ALL RACCOONS TOGETHER HAD A TOTAL EXPLORATION OF 15)??** |
| ExploratoryDiversityAvg_PS | Average number of unique behaviors exhibited toward the puzzle across problem-solving trials. |
| ExploratoryDiversityMax_PS | Maximum number of unique behaviors exhibited toward the puzzle across problem-solving trials. **SAME ISSUE HERE AS ABOVE** |
| ActivityRateAvg_PS | Referred to as "Persistence" in the MS and calculated as total exploration divided by total work time. |
| ActivityRateMax_PS | Referred to as "Persistence" in the MS and calculated as total exploration divided by total work time. **SAME ISSUE HERE AS ABOVE** |
| Solve_PS | Whether or not the subject solved the puzzle. "DidNotAttempt" is entered when a subject did not attempt to solve the puzzle. |
| WasSolveOffCamera | Whether or not the puzzle solve occurred off the camera.  "DidNotAttempt" is entered when a subject did not attempt to solve the puzzle. |
| FinalSolverofLocation | Which species solved the puzzle. "None" indicates that no species solved the puzzle at that location. |
| Solve_PS_Binary | Binary puzzle-solving success: 1 = solved, 0 = did not solve. NA indicates that the subject did not attempt to solve the puzzle. |
| TrialNumber_RT | Species-specific trial number for the risk-taking behavioral trial. RT trial numbers track all interactions with the puzzle, regardless of whether the animal attempted to solve it. |
| TrialNumber_PS | Species-specific trial number for the problem-solving behavioral trial. PS trial numbers were assigned only to observations in which a species made a problem-solving attempt |
| Dummy | **I DONT REMEMBER WHAT THIS MEANS. ASK LAUREN.** |

`StantonPuzzleStudyLocation_12182025_Anonymized` contains the coordinates associated with all puzzle-testing study locations.

| Column | Description |
|-------------------|-----------------------------------------------------|
| Location\* | Identifier for the study location where the observation occurred. |
| Latitude | Latitude of the study location. |
| Longitude | Longitude of the study location. |

*\*All study locations associated with private residences have been given anonymous names.*

## Scripts

The scripts for the full workflow are available as Rmd files in the `Code` folder. All files are R scripts that were run in R version 4.2.1. The output of the models are not stored on GitHub due to the large file sizes, but can be generated on your own device, or are available for download on Dryad Digital Repository (DOI: 10.5061/dryad.xsj3tx9vk).

`Q1-All-Trials.Rmd`: this script uses the *brms* package to construct random-intercept models to compare species-level differences in baseline risk-taking and problem-solving behaviors using all observations (i.e., all trials). The script also generates figures and a summary table of model output.

`Q1-First-Attempts.Rmd`: this script uses the *brms* package to construct random-intercept models to compare species-level differences in baseline risk-taking and problem-solving behaviors using only first observations (i.e., first trials). The script also generates figures and a summary table of model output.

`Q2-Problem-Solving.Rmd`: this script uses the *brms* package to construct random-slope models to assess within-species and among-species effects of boldness, exploration, and effort on problem-solving success. The script also runs a simulation analysis to validate excluding testing location as a random effect from models; generates composite behavioral scores for boldness, exploration, effort from raw observational data; and generates figures and a summary table of model output.

## Model Output

The output of the models are not stored on GitHub, but can be generated on your own device, or are available to download from this Dryad Digital Repository (DOI: 10.5061/dryad.xsj3tx9vk) via the `Model_Output.zip` file. The `.rds` files that can be downloaded from Dryad are described below.

In the `Q1-All-Attempts` folder:

-   `mod.prop.vig.all.rds`: random-intercept model for proportion of time spent vigilant by the subject using all trials

-   `mod.look.cam.all.rds`: random-intercept model for whether the subject looked at the camera using all trials

-   `mod.touch.all.rds`: random-intercept model for whether the subject touched the puzzle using all trials

-   `mod.tot.exp.all.rds`: random-intercept model for total exploration exhibited by the subject using all trials

-   `mod.exp.div.all.rds`: random-intercept model for exploratory diversity exhibited by the subject using all trials

-   `mod.work.time.all.rds`: random-intercept model for total work time of the subject using all trials

-   `mod.act.rate.all.rds`: random-intercept model for activity rate of the subject using all trials

-   `mod.solve.all.rds`: random-intercept model for whether the subject solved the puzzle using all trials

In the `Q1-First-Attempts` folder:

-   `mod.prop.vig.rds`: random-intercept model for proportion of time spent vigilant by the subject using only first attempt trials

-   `mod.look.cam.rds`: random-intercept model for whether the subject looked at the camera using only first attempt trials

-   `mod.touch.rds`: random-intercept model for whether the subject touched the puzzle using only first attempt trials

-   `mod.tot.exp.rds`: random-intercept model for total exploration exhibited by the subject using only first attempt trials

-   `mod.exp.div.rds`: random-intercept model for exploratory diversity exhibited by the subject using only first attempt trials

-   `mod.work.time.rds`: random-intercept model for total work time of the subject using only first attempt trials

-   `mod.act.rate.rds`: random-intercept model for activity rate of the subject using only first attempt trials

-   `mod.solve.rds`: random-intercept model for whether the subject solved the puzzle using only first attempt trials

In the `Q2-Problem-Solving` folder:

-   `mod.boldness.rds`: random-slope model for effect of boldness on problem-solving success

-   `mod.exploration.rds`: random-slope model for effect of exploration on problem-solving success

-   `mod.effort.rds`: random-slope model for effect of effort on problem-solving success

## Figures

This folder contains figures generated from scripts in the `Code` folder.

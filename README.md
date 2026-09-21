# Bay-Area-Carnivore-Cognition

This repository contains all raw data and scripts for the data analysis implemented in Stanton *et al.* (2026) titled "**Traits associated with novel foraging success in urban mesopredators**" and published in *Scientific Reports*.

Please find below a description of all raw and clean data sets and the scripts used to format the raw data, run the models, and create the figures presented in the manuscript. To access the files, download `Bay-Area-Carnivore-Cognition-main.zip` for all data sets, scripts, and figures and `Model_Output.zip` for model output.

## Data Files

In the `Data` folder, you will find three data files:

`Q1_Summary_All_Anonymized` and `Q1_Summary_Firsts_Anonymized`. Both data files contain raw data from problem-solving attempts. The Summary_All data sheet contains all observations (i.e., all trials) whereas the Summary_Firsts datasheet contains only first-attempt observations (i.e., only first trials).

| Column | Description |
|---------------------------|---------------------------------------------|
| Species | Species of the subject. |
| Subject | Identifier of the focal individual or group |
| Location\* | Identifier for the study location where the observation occurred. |
| Home | Whether or not the study location was a private residence. |
| ObservationNumber | The sequential number of an observation across all subjects at a given location. |
| Date | Date on which the observation occurred. |
| Time | Time at which the observation occurred. |
| Photoperiod | Whether the observation occurred during the day time or night time. |
| Weather | Weather conditions during the observation (clear, foggy, or rainy). |
| VisibilityIssue | Whether or not the subject was out of the camera's view for any part of the observation |
| Arrival | Whether or not the subject in the observation was the first to arrive to the puzzle ("First") or other animals had previously visited the puzzle ("Not First") |
| Condition | Social condition of the subject: whether it was observed alone or in a group. |
| NumSubjectsInObservation | Number of subjects present during the observation. |
| Interference | Whether or not the subject cannot access the puzzle because another individual is monopolozing and/or defending the puzzle. |
| AggressionSeen | Whether or not the subject charges, snaps/bites, body-blocks, or vocalizes at another individual. |
| Dog | Whether a dog was seen on camera at any time at a given location. |
| Coyote | Whether a coyote was seen on camera at any time at a given location. |
| PuzzleReset | Whether the puzzle was interferred with by a human or dog at a given location and was therefore rebaited and testing restarted. |
| TrialLengthMax | Length in seconds of the trial beginning when an animal enters the frame and ending when it leaves the frame. Where a group of animals were observed, this represents the maximum trial length by any individual in the group. |
| PropVigilantMax_RT | Proportion of time spent vigilant calculated as the duration of time spent vigilant divided by the total observation time (seconds). Where a group of animals were observed, this represents the maximum proportion of time spent vigilant by any single individual in the group. |
| LookAtCamera_RT | Binary: 1 if the subject ever looked at the camera during the observation, otherwise 0. |
| Touch_RT | Binary: 1 if the subject ever touched the puzzle during the observation, otherwise 0. |
| WorkTimeMax_PS | Total observed amount of time in seconds the subject was alert and engaged with the puzzle across problem-solving trials. Where a group of animals were observed, this represents the maximum work time by any single individual in the group. |
| Urinate | Indicator of whether the subject urinated during the observation. |
| TotalExplorationMax_RT | Total number of exploratory behaviors (e.g., paw, pull, push, roll, etc.) recorded across risk-taking trials. Where a group of animals were observed, this represents the maximum number of exploratory behaviors exhibited by any single individual in the group. |
| ExploratoryDiversityMax_PS | Total number of *unique* behaviors exhibited toward the puzzle across problem-solving trials. Where a group of animals were observed, this represents the maximum number of unique exploratory behaviors exhibited by any single individual in the group. |
| ActivityRateMax_PS | Referred to as "Persistence" in the MS and calculated as total exploration (counts) divided by total work time (seconds). Where a group of animals were observed, this represents the maximum number of exploratory behaviors and work time exhibited by any single individual in the group. |
| Solve_PS | Whether or not the subject solved the puzzle. "DidNotAttempt" is entered when a subject did not attempt to solve the puzzle. |
| WasSolveOffCamera | Whether or not the puzzle solve occurred off the camera.  "DidNotAttempt" is entered when a subject did not attempt to solve the puzzle. |
| FinalSolverofLocation | Which species solved the puzzle. "None" indicates that no species solved the puzzle at that location. |
| Solve_PS_Binary | Binary puzzle-solving success: 1 = solved, 0 = did not solve. NA indicates that the subject did not attempt to solve the puzzle. |
| TrialNumber_RT | Species-specific trial number for the risk-taking behavioral trial. RT trial numbers track all interactions with the puzzle, regardless of whether the animal attempted to solve it. |
| TrialNumber_PS | Species-specific trial number for the problem-solving behavioral trial. PS trial numbers were assigned only to observations in which a species made a problem-solving attempt |
| Dummy | Observations that do not contain behavioral data, but indicate that an animal likely solved (off camera) and therefore used to provide a trial number |

`StantonPuzzleStudyLocations_Anonymized` contains the coordinates associated with all puzzle-testing study locations.

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

`Study_Map.Rmd`: this script generates a study-area map identifying solves versus unsolved puzzle locations.

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

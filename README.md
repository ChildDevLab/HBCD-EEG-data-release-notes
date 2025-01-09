# HBCD-data-release-notes
README instructions and scripts for working with the EEG data in the January 15 HBCD public data release.

These instructions will allow the user to extract a full derivative dataset (of summary statistics and trial measures) from the individual-level file based download, found under "Query Data" > "Download File Based Data" on the Lasso interface. 

This repository contains 3 scripts: 
1. concatenate_files_summary.Rmd: A script to concatenate summary statistics (power and SME) across participants for the Resting State, FACE, and MMN Tasks.
2. concatenate_files_trialmeasures.Rmd: A script to concatenate ERP relevant mean amplitudes at the individual trial level across participants for the FACE and MMN Tasks.
3. separate_conditions.Rmd: A script to filter concatenated data into task specific conditions (upright, inverted, object for FACE and standard, deviant, pre-deviant for MMN).

The user will need RStatistics and RStudio to be able to run these scripts. Below are instructions for downloading these interfaces. 

Download R software: 

To install R on Windows OS:

1. Go to the CRAN website (https://cran.r-project.org/).
2. Click on "Download R for Windows".
3. Click on "install R for the first time" link to download the R executable (.exe) file.
4. Run the R executable file to start installation, and allow the app to make changes to your device.
5. Select the installation language.
6. Follow the installation instructions.
7. Click on "Finish" to exit the installation setup.
8. R has now been successfully installed on your Windows OS. Open the R GUI to start writing R codes.

Installing R on MacOS X:
Installing R on MacOS X is very similar to installing R on Window OS. The difference is the file format that you have to download. The procedure is as follows:

1. Go to the CRAN website (https://cran.r-project.org/).
2. Click on "Download R for macOS".
3. Download the latest version of the R GUI under (.pkg file) under "Latest release". You can download much older versions by following the "old directory" or "CRAN archive" links.
4. Run the .pkg file, and follow the installation instructions.


Download RStudio: 
1. 


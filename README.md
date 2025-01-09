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
4. From your downloads folder, run the R executable file to start installation, and allow the app to make changes to your device.
5. Select the installation language.
6. Follow the installation instructions.
7. Click on "Finish" to exit the installation setup.
8. R has now been successfully installed on your Windows OS. Open the R GUI to start writing R codes.

Installing R on MacOS X:
Installing R on MacOS X is very similar to installing R on Window OS. The difference is the file format that you have to download. The procedure is as follows:

1. Go to the CRAN website (https://cran.r-project.org/).
2. Click on "Download R for macOS".
3. Download the latest version of the R GUI under (.pkg file) under "Latest release". You can download much older versions by following the "old directory" or "CRAN archive" links.
4. From your downloads folder, run the .pkg file, and follow the installation instructions.


Download RStudio: 

Installing RStudio Desktop:

1. Go to the RStudio website (https://posit.co/download/rstudio-desktop/).
2. Scroll down to the "All Installers and Tarballs" section. 
3. Click on the download link specific to your operating system (OS). 
4. From your downloads folder, run the RStudio Executable file (.exe) for Windows OS or the Apple Image Disk file (.dmg) for macOS X.
5. Follow the installation instructions to complete RStudio Desktop installation.
6. RStudio is now successfully installed on your computer.


Now that you have these software, you will be able to run the scripts on our repository to manipulate the provided participant level data. First, we will outline how to setup your folder structure. 

#SM later fill this in based on how the EEG data is provided

The following are instructions on how to run each of the provided scripts. 

1. concatenate_files_summary.Rmd:
This script concatenate all summary statistics (SME) across participants and outputs a sheet for the Resting State, FACE, and MMN Tasks. 

2. concatenate_files_trialmeasures.Rmd:
This script concatenates all ERP relevant mean amplitudes at the individual trial level across participants for the FACE and MMN Tasks.

3. separate_conditions.Rmd: 
This script filters concatenated data into task specific conditions (upright, inverted, object for FACE and standard, deviant, pre-deviant for MMN).

4. get_mean_amp.Rmd: 
This script pulls the trial measure data for each participant and calculates mean amplitude at each time window of interest. 



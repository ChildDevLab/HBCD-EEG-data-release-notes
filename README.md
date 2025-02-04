# HBCD-EEG-data-release-notes
README instructions and scripts for working with the EEG data in the March 1 HBCD public data release.

These instructions will allow the user to extract a full derivative dataset (of summary statistics and trial measures) from the individual-level file based download, found under "Query Data" > "Download File Based Data" on the Lasso interface. 

This repository contains 4 scripts: 
*update this when scripts are finalized*

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
#SM this instruction set will be the same but instead would be one single script

The following are instructions on how to run each of the provided scripts. 

1. concatenate_files_summary.Rmd:
This script concatenate all summary statistics (SME) across participants and outputs a sheet for the Resting State, FACE, and MMN Tasks. 

To use this script: 
1. Open the script using RStudio. 
2. Provide a directory path (the path to the folder where the downloaded EEG data is stored) on line 22. 
NOTE: if you are using this script on a Windows computer, you will need to change the direction of the slashes from '\\' to '/'.
3. Provide an output path (the path to the folder where you would like the outputs to end up) on line 23. 
NOTE: if you are using this script on a Windows computer, you will need to change the direction of the slashes from '\\' to '/'.
4. At the top right of the script, click the down arrow next to the "Run" icon. 
5. At the bottom of the list, click "Run All" 
6. Your output sheets can be seen in the folder provided on line 23.

2. concatenate_files_trialmeasures.Rmd:
This script concatenates all ERP relevant mean amplitudes at the individual trial level across participants for the FACE and MMN Tasks.

To use this script: 
1. Open the script using RStudio. 
2. Provide a directory path (the path to the folder where the downloaded EEG data is stored) on line 22. 
NOTE: if you are using this script on a Windows computer, you will need to change the direction of the slashes from '\\' to '/'.
3. Provide an output path (the path to the folder where you would like the outputs to end up) on line 23. 
NOTE: if you are using this script on a Windows computer, you will need to change the direction of the slashes from '\\' to '/'.
4. At the top right of the script, click the down arrow next to the "Run" icon. 
5. At the bottom of the list, click "Run All" 
6. Your output sheets can be seen in the folder provided on line 23.

3. separate_conditions.Rmd: 
This script filters concatenated data into task specific conditions (upright, inverted, object for FACE and standard, deviant, pre-deviant for MMN).

To use this script: 
1. Open the script using RStudio. 
2. Provide a directory path (the path to the folder where the downloaded EEG data is stored) on line 17. 
NOTE: if you are using this script on a Windows computer, you will need to change the direction of the slashes from '\\' to '/'.
3. Provide an output path (the path to the folder where you would like the outputs to end up) on line 18. 
NOTE: if you are using this script on a Windows computer, you will need to change the direction of the slashes from '\\' to '/'.
4. At the top right of the script, click the down arrow next to the "Run" icon. 
5. At the bottom of the list, click "Run All" 
6. Your output sheets can be seen in the folder provided on line 18.

4. get_mean_amp.Rmd: 
This script pulls the trial measure and summary stats data for each participant, calculates mean amplitude at each time window of interest, and combines all three into a csv. 

To use this script: 
1. Open the script using RStudio. 
2. Provide a directory path (the path to the folder where the downloaded EEG data is stored) on line 17. 
NOTE: if you are using this script on a Windows computer, you will need to change the direction of the slashes from '\\' to '/'.
3. Provide an output path (the path to the folder where you would like the outputs to end up) on line 18. 
NOTE: if you are using this script on a Windows computer, you will need to change the direction of the slashes from '\\' to '/'.
4. At the top right of the script, click the down arrow next to the "Run" icon. 
5. At the bottom of the list, click "Run All" 
6. Your output sheets can be seen in the folder provided on line 23.

#SM add here: description of the outputs, notes about ERPs, ROIs, and time windows selected

Descriptions of each task's ERP components, time windows (by age), and ROI are available in the excel file on the GitHub repository, and below: 

Task	Component	Time window	ROI	Age
MMN	MMR	200-400	t7t8	3-9
MMN	MMR	200-400	f7f8	3-9
MMN	MMR	200-400	fcz	3-9
MMN	N1	40-79	t7t8	3-9
MMN	P1	80-100	t7t8	3-9
MMN	N2	100-180	t7t8	3-9
FACE	N290	200-350	p8	3-6
FACE	P1	75-125	oz	3-6
FACE	N290	250-350	oz	3-6
FACE	P400	355-625	oz	3-6
FACE	N290	250-300	p8	6-9
FACE	P1	75-125	oz	6-9
FACE	N290	250-300	oz	6-9
FACE	P400	325-625	oz	6-9
FACE	Nc	300-650	FCz	3-9
VEP	N1	40-79	oz	3-6
VEP	P1	80-140	oz	3-6
VEP	N2	141-300	oz	3-6
VEP	N1	40-79	oz	6-9
VEP	P1	80-120	oz	6-9
VEP	N2	121-170	oz	6-9




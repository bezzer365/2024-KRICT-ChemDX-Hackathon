# 2024 KRICT ChemDX Hackathon

## Project Overview

This project for the [2024 KRICT ChemDX Hackathon](https://gitlab.chemdx.org/global-network/2024-krict-chemdx-hackathon/-/wikis/home) hosted on the 6-8 November 2024 utilises datasets from the [Chemical Data Explorer (ChemDX)](https://www.chemdx.org/) database to develop visualisation tools and fitting functions for Raman spectra using intensity data.

### Authors

- Joshua Berry
- Katerina Christofidou

Material Science and Engineering Department, University of Sheffield, UK

## Data

The data is provided in the form of an .xlsx file `intensity_data.xlsx`, where the Raman shift is provided in cm<sup>-1</sup> and the intensity in arbitrary units for 39 different samples.

## Objectives

- Visualise indivdual spectra
- Enable direct comparison by visualisation across spectra of different samples
- Fit spectra and identify peak positions

## Methodology

First the samples are visualised individually and then stacked vertically to enable direct comparison of spectra across samples. The spectra are then background subtracted using the `Baselines` function of the `pybaselines` library, followed by smoothing and normalisation using the `savgol_filter` function from the `scipy` library. Finally the spectra are fit using the `curve_fit` function, and the peak positions identified using `find_peaks` from the `scipy` library.

## Results

![alt text](https://github.com/bezzer365/2024-KRICT-ChemDX-Hackathon/blob/main/spectrum_fit.png)



Code produced for Raman spectrum visulaisation and analysis contained in the Functions.pynb file. 

Backgroud_Fit - includes the workings for background fits for a single dataset to demostrate the developmet of the functions. 
KRICT2024_Hackathon_Gaussian - includes the workings for constructing the peak finding and Gaussian fitting functions as well as integrated intensities. 
Loop - loops the Gaussian fit through multiple datasets
Functions - the final notebook is the full code, with both functions and loops integrated to allow multiple datasets to be visualised and analysed and can be adapted accordingly. 

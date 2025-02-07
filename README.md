# 2024 KRICT ChemDX Hackathon

## Project Overview

This project was developed for the [2024 KRICT ChemDX Hackathon](https://gitlab.chemdx.org/global-network/2024-krict-chemdx-hackathon/-/wikis/home) hosted from the 6-8 November 2024. It utilises datasets from the [Chemical Data Explorer (ChemDX)](https://www.chemdx.org/) database to create visualisation tools and fitting functions for Raman spectra using intensity data.

### Authors

- Joshua Berry
- Katerina Christofidou

_Material Science and Engineering Department, University of Sheffield, UK_

## Data

The dataset is provided in an Excel .xlsx file `intensity_data.xlsx`, containing Raman spectra for 39 different samples. Each spectrum consists of:
- Raman shift (in cm<sup>-1</sup>)
- Intensity (in arbitrary units)

## Objectives

This project aims to
- Visualise indivdual spectra
- Enable direct comparison of spectra from different samples
- Fit spectra and identify peak positions

## Methodology

1. Visualisation
    - Individual spectra are plotted
    - Spectra are stacked vertically to facilitate direct comparison across samples
2. Preprocessing
    - Background subtraction using the `Baselines` function of the `pybaselines` library
    - Smoothing and normalisation using the `savgol_filter` function from the `scipy.signal` library
3. Fitting and Peak Identification
    - Curve fitting using the `curve_fit` function from the `scipy.optimize` library
    - Peak detection using the `find_peaks` function from the `scipy.signal` library

## Results

📌 __Example Fitted Raman Spectra__
<img src="https://github.com/bezzer365/2024-KRICT-ChemDX-Hackathon/blob/main/spectrum_fit.png" alt="Fitted Spectra" width="400" height="300">

## Future Directions

The python code developed in this project for the 2024 KRICT ChemDX Hackathon successfully provides an effective visualisation and analysis tool for Raman spectra. Future improvements could include:
- Expanding the analysis to additional Raman datasets
- Extending functionality to other material characterisation techniques, such as:
    - X-Ray Diffraction (XRD)
    - Infrared (IR) Spectroscopy

## Code Structure

📂 **Files & Notebooks**  

- **`Functions.ipynb`** – Main script for Raman spectra visualisation and analysis.  
- **`Background_Fit.ipynb`** – Development of background subtraction for a single spectrum.  
- **`KRICT2024_Hackathon_Gaussian.ipynb`** – Peak finding, Gaussian fitting, and integrated intensities.  
- **`Loop.ipynb`** – Iterates Gaussian fitting through multiple datasets.  

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/bezzer365/2024-KRICT-ChemDX-Hackathon.git
2. Navigate to the project directory:
   ```bash
   cd 2024-KRICT-ChemDX-Hackathon

## Useage

Open Jupyter Notebook or Google Collab and follow the instructions of `Functions.ipynb`. The other notebooks are optional and provide an insight into the iterative development of the tools.

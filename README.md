# Plotting-maps-with-Geomagnetic-Field-Models-
Here you can find some useful scripts to plot maps of the geomagnetic field intensity with diferent geomagnetic field models.
Some functions in this repository were adapted from Filipe Terra-Nova's GitHub (@filipecros).

## Geomagnetic Field Models
Geomagnetic field models are mathematical representations that estimate the intensity and direction of the Earth’s magnetic field in space and time. They are constructed from geomagnetic observations obtained from a variety of sources, such as ground-based observatories, satellite measurements and archaeomagnetic/paleomagnetic records. They typically express the field through a spherical harmonic expansion using Gauss coefficients. These models make it possible to separate contributions from different spatial scales, investigate the structure and temporal evolution of the geomagnetic field and gain insight into the underlying core dynamics responsible for the geodynamo. As such, geomagnetic field models are essential tools for reconstructing past field behavior, interpreting regional and global magnetic anomalies and supporting scientific and practical applications including navigation, space weather studies and geophysical interpretations.

## Repository proposal
The aim of this repository is to offer the reader a set of practical scripts for plotting intensity maps (on or below the Earth's surface) using different geomagnetic field models, within specific time intervals and expansion order of the spherical harmonic coefficients (Gauss coefficients).

## Instructions
### ArchKalmag14k (Schanner et al., 2022)
The ArchKalmag14k model is a global geomagnetic field reconstruction for the Holocene, spanning the last 14,000 years, which is derived by applying a Kalman filter–based inversion to available archeomagnetic and volcanic paleomagnetic data.

a) DOI of the paper: 10.1029/2021JB023166;

b) Link to download data (Gauss coefficients): https://ionocovar.agnld.uni-potsdam.de/Kalmag/Archeo/Archeo14k/.

Note: The `ArchKalmag14k_lmax14.txt` file was downloaded from the link above (b), with lmax = 14, output timestep of 50 years and time window from -12000 to 1950 years (minimum and maximum limits reached by the model). If you want a larger lmax, or modify the output timestep, a new `.txt` file must be downloaded from this link. If you choose this file with other requirements, the function that reads the Gauss coefficients must also be modified to "reach" the last coefficient of degree lmax in the Jupyter Notebook file `ArchKalmag14k.ipynb`.

To plot the intensity map, please do this:
1. Dowload the file `ArchKalmag14k_lmax14.txt`;
2. Dowload the file `ArchKalmag14k.ipynb` (or just copy its content);
3. Run.

### COV-OBS.x2 (Huder et al., 2020)
The COV-OBS.x2 model is a geomagnetic field model covering the period 1840–2020, mainly constrained by long-term observatory records, historical ground-based surveys and satellite magnetic measurements. It incorporates annual differences of observatory data, virtual observatory series derived from the CHAMP (2001–2010) and Swarm (since 2013) missions and uses statistical a priori temporal covariances to obtain realistic estimates of the geomagnetic field evolution and its uncertainties.

a) DOI of the paper: 10.1186/s40623-020-01194-2;

b) Link to download data (Gauss coefficients): https://www.spacecenter.dk/files/magnetic-models/COV-OBSx2/COV-OBS.x2-int.

To plot the intensity map, please do this:
1. Dowload the file `covobsx2.txt`;
2. Dowload the file `COV-OBSx2.ipynb` (or just copy its content);
3. Run.

# seismic-event-analysis
Seismic event analysis using real waveform data, P-S arrival times, IASP91 travel-time modelling, and FFT.
# Seismic Event Analysis using Waveform and Frequency-Domain Methods

## Overview

This project analyses a real earthquake using seismic waveform data obtained through the EarthScope FDSN service. The analysis focuses on identifying P- and S-wave arrivals, comparing observed travel times with the IASP91 Earth model, and examining the frequency content of the recorded signal using FFT.

## Earthquake Event

- Magnitude: M 7.3
- Origin Time: 17 July 2026, 14:48:39 UTC
- Latitude: 14.57°
- Longitude: -92.96°
- Depth: 22 km

## Methodology

1. Retrieved seismic waveform data from multiple stations using ObsPy.
2. Preprocessed the waveforms using detrending and tapering.
3. Applied band-pass filtering for seismic signal analysis.
4. Identified P- and S-wave arrivals using waveform analysis and STA/LTA.
5. Calculated theoretical travel times using the IASP91 model.
6. Compared observed P/S arrivals with theoretical travel times.
7. Analysed S-P time variation with epicentral distance.
8. Performed FFT analysis to examine the frequency content of the seismic signal.

## Results

### P-Wave Travel-Time Analysis

The manually identified P-wave arrivals showed close agreement with the second P-arrival branch predicted by the IASP91 model.

- Mean absolute P-wave residual: 0.222 s
- P-wave RMSE: 0.304 s

### S-Wave Travel-Time Analysis

S-wave arrivals showed comparatively larger residuals.

- Mean absolute S-wave residual: 1.006 s
- S-wave RMSE: 1.379 s

The larger residuals are partly associated with uncertainty in manually identifying weaker or emergent S-wave arrivals.

### S-P Time Analysis

The observed S-P time generally increased with increasing epicentral distance, consistent with the expected difference in P- and S-wave propagation times.

### Frequency-Domain Analysis

FFT analysis of the GI.HUCU waveform showed strong low-frequency content, with spectral amplitude generally decreasing toward higher frequencies.

## Limitations

- P- and S-wave arrivals were manually picked, introducing picking uncertainty.
- Some stations had weak or unclear phase arrivals.
- IASP91 is a 1-D Earth velocity model and does not represent local 3-D Earth structure.

## Tools Used

- Python
- ObsPy
- NumPy
- Pandas
- Matplotlib
- SciPy
- IASP91 Travel-Time Model

## Files

- `PROJECT0.ipynb` — Complete analysis notebook
- `PROJECT0.ipynb - Colab.pdf` — PDF version of the notebook

## Author

Mohak Chanda
MSc Applied Geophysics, IIT Bombay

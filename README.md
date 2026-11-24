# Model Glider Low-Cost Data Logger & Flight Dataset

An interactive **Google Colab** engineering tool built with `ipywidgets`, `NumPy`, `Pandas`, and `Matplotlib` to simulate low-cost data logger flights for a **model glider** and convert each flight into a structured **altitude (`[m]`)** or **vertical acceleration (`[g]`)** time-series dataset[cite: 8].

## Overview

A low-cost flight data logger on a small glider records time-stamped sensor measurements across launch, climb/glide, and touchdown so each flight can be analyzed as a clean dataset[cite: 8]. This notebook lets you configure flight scenarios, sampling rate, duration, peak altitude, and sensor noise, inspect a 2D downrange-vs.-altitude flight profile, view the selected dataset plot and table preview, and export the flight log to CSV.

### Supported Flight Profiles
- **Hand Launch & Thermal Glide**
- **Steep Dive & Pull-Up**
- **Gusty Ridge Glide**

### Dataset Outputs
- **Altitude Dataset `[m]`:** Time-series altitude (`altitude_m`) with peak altitude detection.
- **Acceleration Dataset `[g]`:** Time-series vertical load factor (`accel_vert_g`) with `1.0 g` reference and peak load detection.

## Key Features

- **Interactive English UI (`ipywidgets`):** Choose flight profile, dataset output mode, sample rate (`Hz`), flight duration (`s`), peak altitude (`m`), and sensor noise level, then click **Log Flight Dataset** or adjust controls live.
- **2D Flight Trajectory View:** Shows a 2D downrange distance vs. altitude profile from launch (`0 m`) through flight to touchdown (`0 m`).
- **Dataset Plot, Summary & CSV Export:** Displays the time-series graph, key flight statistics, a sample rows preview table, and writes a `.csv` dataset file in the working environment.

## How to Run in Google Colab

1. Open a new notebook in [Google Colab](https://colab.research.google.com/).
2. Paste the glider data logger code into a code cell and run it.
3. Select your flight profile and dataset mode, inspect the plots and table, and download the generated `.csv` file from the Colab file browser if needed.

## Engineering Notes

- Real barometric altitude and IMU acceleration logs also include sensor bias, temperature drift, wind turbulence, and mounting vibrations; pairing synthetic test sets with real flight logs helps validate data-processing and filtering pipelines.

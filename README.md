# Well-Log Visualization in Python


## Overview

Well logs provide essential petrophysical measurements used in oil and gas exploration to evaluate subsurface formations. This project processes a well-log dataset (`WellData.csv`) spanning depths from ~4610 m to 4802 m and generates multi-track log plots—progressing from a basic three-track layout to a customized industry-standard visualization featuring overlaid porosity curves.

## Features

* **Data Preprocessing & Cleaning**: Loads raw well-log CSV data and converts standard industry null/missing value placeholders (`-999.25` and `-999.00`) into `NaN` for accurate statistical profiling and plotting.
* **Statistical Summary**: Generates descriptive statistics across key petrophysical measurements:
  * `DEPTH`: Measured Depth (m)
  * `GR`: Gamma Ray
  * `DT`: Sonic / Acoustic Travel Time
  * `RHOB`: Bulk Density
  * `DRHO`: Density Correction
  * `NPHI`: Neutron Porosity
* **Basic Multi-Track Log Plot**: Visualizes Gamma Ray (`GR`), Bulk Density (`RHOB`), and Sonic (`DT`) across depth using `matplotlib.pyplot.subplot2grid`.
* **Customized Petrophysical Log Plot**:
  * Places curve titles, units/scales, and color-coded spines at the top of each track.
  * Overlays Neutron Porosity (`NPHI`) onto the Bulk Density (`RHOB`) track using a twinned x-axis (`twiny()`) with inverted porosity scales (`0.45` to `-0.15`) for standard crossover interpretation.
  * Inverts the y-axis to display increasing depth downward (`4850` m to `4600` m).

## Prerequisites

To run this notebook locally or in Google Colab, you will need Python 3 and the following libraries:

* `pandas`
* `numpy`
* `matplotlib`



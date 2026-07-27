# Central Texas Atmospheric Anomalies

A data science investigation of whether atmospheric aerosol observations provide additional predictive information about tornado occurrence in Central Texas.

## Research Question

Does aerosol optical depth provide measurable predictive information about tornado occurrence in Central Texas beyond conventional meteorological variables?

## Project Overview

This project investigates whether satellite- and ground-based aerosol measurements can improve models of tornado occurrence when combined with established meteorological variables such as atmospheric instability, moisture, and wind shear.

The project will compare:

- A baseline model using conventional meteorological variables
- An aerosol-enhanced model using the same variables plus aerosol features

The objective is to measure whether aerosol observations contribute useful predictive information—not to assume that aerosols cause tornadoes.

## Project Status

🟡 **Current stage: Research design and literature review**

The research question, geographic scope, datasets, and evaluation plan are currently being defined.

## Documentation

- [Research Question](research-question.md)
- [Project Context](docs/project-context.md)
- [Research Decisions](docs/decisions.md)

## Planned Data Sources

- NOAA tornado and severe-weather records
- NASA MODIS or VIIRS aerosol observations
- ERA5 or NOAA meteorological reanalysis
- EPA Air Quality System measurements
- USGS terrain and elevation data

## Planned Methods

- Exploratory data analysis
- Spatial and temporal data integration
- Feature engineering
- Baseline statistical modeling
- Random Forest and XGBoost
- Model calibration
- SHAP-based interpretation

## License

The original code and documentation in this repository are available under the [MIT License](LICENSE). External datasets remain subject to their respective providers’ terms and attribution requirements.


# Research Decisions

This document records important methodological decisions, their reasoning, and any later revisions. Items that have not yet been finalized are labeled **Provisional** or **Open**.

## Decision Status

- **Finalized:** Adopted unless new evidence requires revision
- **Provisional:** Current working choice that still requires validation
- **Open:** Not yet decided
- **Revised:** Replaced by a later documented decision

---

## D-001: Project Title

- **Status:** Finalized
- **Decision:** Use **Central Texas Atmospheric Anomalies** as the project title.
- **Reasoning:** The title is broad enough to support the initial aerosol–tornado investigation and related future questions without implying that aerosols cause tornadoes.

## D-002: Primary Research Question

- **Status:** Finalized
- **Decision:** Investigate whether aerosol optical depth provides measurable predictive information about tornado occurrence in Central Texas beyond conventional meteorological variables.
- **Reasoning:** This wording distinguishes additional predictive value from causation and requires aerosol variables to be evaluated alongside established weather predictors.

## D-003: Initial Modeling Strategy

- **Status:** Provisional
- **Decision:** Compare two model categories:

  1. A baseline model using conventional meteorological variables.
  2. An aerosol-enhanced model using the same variables plus aerosol-related features.

- **Reasoning:** Direct comparison will show whether aerosol observations add information beyond standard meteorological conditions.

## D-004: Geographic Focus

- **Status:** Open
- **Current direction:** Central Texas, potentially defined using selected counties, a geographic bounding box, or a region surrounding the San Antonio–Austin corridor.
- **Decision criteria:**

  - Tornado-event counts
  - Satellite-data coverage
  - Ground-monitor coverage
  - Meteorological relevance
  - Computational feasibility

- **Next action:** Compare candidate boundaries before selecting the final study region.

## D-005: Study Period

- **Status:** Provisional
- **Current direction:** 2010–2025
- **Reasoning:** This range may provide a sufficiently long event history while overlapping with relevant satellite, meteorological, and ground-monitoring datasets.
- **Next action:** Verify consistent coverage across the selected data sources.

## D-006: Initial Data Sources

- **Status:** Provisional
- **Decision:** Prioritize the following source categories:

  - NOAA tornado and severe-weather records
  - NASA MODIS or VIIRS aerosol observations
  - ERA5 or NOAA meteorological reanalysis
  - EPA Air Quality System measurements
  - USGS terrain and elevation data

- **Reasoning:** These sources collectively represent documented events, atmospheric conditions, aerosol observations, surface air quality, and geographic context.
- **Note:** Specific products will be selected after reviewing documentation, resolution, coverage, and quality controls.

## D-007: Primary Aerosol Measurement

- **Status:** Provisional
- **Decision:** Use aerosol optical depth as the primary satellite-derived aerosol variable.
- **Reasoning:** AOD provides a measure of aerosol loading through the atmospheric column and is available from established satellite products.
- **Limitation:** AOD is not equivalent to surface particulate-matter concentration and may be unavailable when clouds obstruct retrieval.

## D-008: Ground-Level Air-Quality Measurements

- **Status:** Provisional
- **Decision:** Prefer underlying pollutant concentrations, such as hourly PM2.5 measurements, over AQI when suitable data are available.
- **Reasoning:** AQI is a derived public-health index that compresses pollutant information. Direct concentrations retain more detail for scientific analysis.
- **Note:** Ground measurements will be treated as complementary to satellite AOD, not as interchangeable with it.

## D-009: Missing AOD Values

- **Status:** Finalized
- **Decision:** Store unavailable AOD measurements as missing values (`NaN`), never as zero.
- **Additional handling:**

  - Preserve product quality-assurance flags.
  - Create an AOD-missingness indicator.
  - Investigate whether missingness is associated with cloud cover, severe weather, or tornado occurrence.

- **Reasoning:** A failed or cloud-obstructed retrieval indicates that no valid measurement was obtained; it does not indicate clean air or an absence of aerosols.

## D-010: Outcome Definition

- **Status:** Open
- **Current direction:** Define a binary variable indicating whether a documented tornado occurred within a specified distance and forecast window.
- **Candidate distance thresholds:** 25 km and 40 km
- **Candidate lead times:** 1, 3, 6, and 12 hours
- **Next action:** Evaluate how alternative definitions affect event counts, class imbalance, and scientific interpretability.

## D-011: Unit of Analysis

- **Status:** Provisional
- **Current direction:** Geographic grid cell by observation or forecast time.
- **Reasoning:** This structure supports the spatial and temporal integration of tornado records, reanalysis variables, satellite observations, and terrain data.
- **Next action:** Select grid resolution after comparing source resolutions and computational requirements.

## D-012: Data Splitting

- **Status:** Provisional
- **Decision:** Prefer time-based validation, with later years reserved for final testing.
- **Reasoning:** Random row-level splitting could leak information between related times, locations, or storm events. Testing on later periods better represents forecasting unseen conditions.

## D-013: Evaluation Metrics

- **Status:** Provisional
- **Decision:** Do not use ordinary accuracy as the primary measure because tornadoes are rare.
- **Candidate metrics:**

  - Precision-recall area under the curve
  - Brier score
  - Calibration curves
  - Recall at selected false-alarm rates
  - Performance by season and forecast lead time
  - Confidence intervals from temporal or event-based resampling

- **Next action:** Finalize the primary metric before model comparison.

## D-014: Interpretation of Results

- **Status:** Finalized
- **Decision:** Keep statistical association, predictive value, and physical causation separate.
- **Reasoning:** An aerosol variable may improve prediction without causing tornadoes. Correlation or feature importance alone will not support a causal conclusion.

## D-015: Initial Project Scope

- **Status:** Finalized
- **Decision:** Begin with tornado records, meteorological reanalysis, and one aerosol product.
- **Deferred components:**

  - NEXRAD radar data
  - Multiple satellite-product comparisons
  - Operational forecasting deployment
  - Detailed causal modeling
  - Quantum field theory or particle-physics hypotheses

- **Reasoning:** These additions would substantially increase complexity before the core data pipeline and baseline model have been validated.

---

## Open Decisions

The following choices must be resolved before the main dataset is constructed:

- Exact Central Texas study boundary
- Final study period
- NOAA tornado dataset and verification procedure
- NASA aerosol product
- Meteorological reanalysis product
- Spatial grid resolution
- Observation interval
- Tornado distance threshold
- Forecast lead times
- Primary evaluation metric
- Missing-data and quality-control thresholds

## Revision Log

| Date | Decision | Change |
|---|---|---|
| 2026-07-27 | Initial documentation | Created the first research decision record. |

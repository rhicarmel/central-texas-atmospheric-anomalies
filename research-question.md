# Research Question

## Primary Question

Does aerosol optical depth provide measurable predictive information about tornado occurrence in Central Texas beyond conventional meteorological variables?

## Scientific Motivation

Tornado formation is primarily evaluated using meteorological conditions such as atmospheric instability, moisture, wind shear, and storm organization. This project investigates whether aerosol observations contain additional information that may improve local tornado-occurrence models.

The study does not begin with the assumption that aerosols cause tornadoes. It first tests whether a measurable association exists and then determines whether aerosol variables improve prediction after established meteorological factors are included.

## Curiosity

> I wonder whether atmospheric aerosol conditions influence or reflect conditions associated with tornado formation in Central Texas.

## Hypothesis

Aerosol optical depth measured before severe weather events will contain some information about tornado occurrence. However, its predictive contribution is expected to be smaller than that of conventional meteorological variables such as instability, moisture, and wind shear.

## Study Design

Two model categories will be compared:

1. **Baseline model:** Uses conventional meteorological variables only.
2. **Aerosol-enhanced model:** Uses the same meteorological variables plus aerosol-related features.

The comparison will determine whether aerosol observations provide additional predictive value on unseen data.

## Initial Scope

- **Geographic area:** Central Texas, to be defined using counties or a geographic bounding box
- **Study period:** Tentatively 2010–2025, subject to dataset availability
- **Unit of analysis:** Geographic grid cell by observation time
- **Outcome:** Whether a documented tornado occurred within a defined distance and forecast window
- **Initial lead times:** 1, 3, 6, and 12 hours
- **Primary aerosol variable:** Aerosol optical depth (AOD)

## Primary Outcome Variable

`TORNADO_WITHIN_WINDOW`

The variable will equal `1` when a documented tornado occurs within a defined distance of a grid cell during the forecast window and `0` otherwise.

Candidate distance thresholds include 25 and 40 kilometers. These values will be evaluated during study design.

## Predictor Categories

### Conventional Meteorological Variables

- Convective available potential energy (CAPE)
- Convective inhibition (CIN)
- Surface temperature and dew point
- Relative humidity
- Surface pressure
- Precipitable water
- Wind speed and direction
- Low-level and deep-layer wind shear
- Storm-relative helicity
- Recent precipitation

### Aerosol Variables

- Current aerosol optical depth
- Lagged aerosol optical depth
- Rolling AOD averages
- Recent changes in AOD
- AOD anomaly relative to the local seasonal average
- Missing-AOD indicator
- Smoke or dust classifications, where available
- Ground-level particulate-matter measurements, where available

## Evaluation

Because tornadoes are rare, ordinary accuracy will not be treated as the primary performance measure. Evaluation may include:

- Precision-recall area under the curve
- Brier score
- Calibration curves
- Recall at selected false-alarm rates
- Performance by season and forecast lead time
- Confidence intervals using temporal or event-based resampling

The final test data should come from later years rather than randomly selected observations whenever practical. This will better represent prediction on genuinely unseen future conditions.

## Evidence Standard

The hypothesis will receive support only if aerosol features:

1. Improve performance on held-out future data.
2. Improve more than one relevant evaluation metric.
3. Remain informative after conventional weather variables are included.
4. Demonstrate reasonably consistent behavior across seasons or severe-weather events.
5. Remain useful during sensitivity tests involving missing data, spatial resolution, and forecast lead time.

An observed correlation will not, by itself, establish that aerosols cause tornadoes.

## Important Limitation

Satellite aerosol observations are often unavailable when clouds obstruct the satellite’s view, including during severe-weather conditions. A missing AOD value indicates that no valid measurement was retrieved; it does not indicate clean air or an absence of aerosols.

Missing AOD values will be stored as missing (`NaN`) rather than replaced with zero. The project will also preserve data-quality flags and create a missing-AOD indicator to investigate whether measurement availability is systematically related to weather conditions or tornado occurrence.

## Current Research Stage

🟡 **Curiosity and hypothesis development**

The geographic boundary, study period, datasets, outcome definition, and evaluation design remain provisional and will be documented as decisions are finalized.

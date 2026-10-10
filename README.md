# Rönne River: Flow and Coastal Water-Level Scenarios

**A 1D hydraulic analysis of how upstream discharge and downstream sea level affect a 9 km river reach.**

[中文](README.zh-CN.md) · [All figures](docs/FIGURES.md) · [Model and scenario guide](models/README.md) · [Results table](data/scenario-results.csv)

![Four discharge and sea-level scenarios](figures/scenario-depths.png)

## Question

How do river flow and sea level change water levels at two locations upstream of the coastal outlet? The analysis compares four boundary-condition combinations using one common river geometry in HEC-RAS.

## Model setup

| Item | Setting |
|---|---|
| Reach | Lower 9 km of the Rönne River, near Ängelholm |
| Formulation | One-dimensional, steady, subcritical flow |
| Geometry | Terrain-based channel, bank lines, overbank flow paths and cross sections |
| Spatial reference | SWEREF99, as recorded in the analysis |
| Manning n | 0.025 in the channel; 0.04 on the floodplains |
| Upstream boundary | 100 or 160 m³/s |
| Downstream boundary | Known water level of 0.5 or 1.0 m |
| Evaluation sections | RS 2422 and RS 7107 |

## Four scenarios on the same geometry

| Scenario | Discharge (m³/s) | Sea level (m) | WSE at RS 2422 (m) | WSE at RS 7107 (m) |
|---|---:|---:|---:|---:|
| PF1 | 100 | 0.5 | 1.59 | 2.98 |
| PF2 | 100 | 1.0 | 1.62 | 2.98 |
| PF3 | 160 | 0.5 | 1.93 | 3.67 |
| PF4 | 160 | 1.0 | 1.93 | 3.67 |

Values are reported simulation outputs, not measured water levels. The downloadable table also includes depth and velocity.

## Interpretation

Increasing discharge from 100 to 160 m³/s at sea level 0.5 m raises simulated water levels by **0.34 m at RS 2422** and **0.69 m at RS 7107**. Raising sea level from 0.5 to 1.0 m at discharge 100 m³/s produces a **0.03 m rise at RS 2422**, with no change visible at the reported precision at RS 7107.

![Longitudinal profile](figures/longitudinal-profile.png)

The longitudinal profiles show coastal backwater influence near the outlet, weakening upstream as river discharge becomes the dominant influence at the selected sections. PF3 and PF4 have equal reported water levels at both evaluation points; PF4 is not uniquely the highest case at those points.

## Engineering use

The case demonstrates terrain-based geometry preparation, hydraulic boundary setup, controlled scenario comparison and extraction of site-specific design information. Steady simulations describe boundary-condition snapshots. They do not resolve flood-wave timing, time-varying tide–river interaction or provide a validated flood defence design.

## Materials

- Five original result/context figures in the [gallery](docs/FIGURES.md).
- [Baseline model archive and four-scenario instructions](models/README.md).
- [Scenario results](data/scenario-results.csv), transcribed from the analysis record.

Analysis and portfolio: **Tianshu Zhang**. Model archives and reported outputs are preserved; the solver has not been rerun for this release.

# Baseline Modeling

## What is a Baseline Model?

A baseline model is a statistical regression that predicts expected energy consumption based on **influence factors** — variables that drive consumption independently of operational efficiency. Comparing actual consumption against the predicted baseline quantifies the impact of energy interventions.

Dybee uses IPMVP-compliant baseline modeling (International Performance Measurement and Verification Protocol).

## Influence Factors

Common factors used in baseline models:

| Factor | Notes |
|---|---|
| Outdoor temperature | Retrieved automatically from NASA using building coordinates |
| Heating degree days (HDD) | Derived from temperature data |
| Cooling degree days (CDD) | Derived from temperature data |
| Occupancy | Manual schedule or imported data |

Dybee uses linear regression to fit the baseline. The model is evaluated over a **reference period** — typically 12–24 months of pre-intervention data.

## Creating a Baseline

Navigate to **Energy Monitoring → Measurement & Verification**:

1. Select the energy source
2. Define the reference period (pre-intervention date range)
3. Select influence factors to include in the regression
4. Review the model quality indicators (R², residuals)
5. Save the baseline

## Interpreting Model Quality

A well-fitted baseline should have:

- **R² > 0.75** for weather-sensitive buildings (heating/cooling dominated)
- Residuals distributed randomly with no strong seasonal pattern
- No obvious outliers distorting the regression

If the model quality is low, consider adjusting the reference period or adding/removing influence factors.

## Post-Intervention Period

Once a baseline exists, Dybee continuously compares actual consumption to the model prediction. The difference represents measured savings (or regression).

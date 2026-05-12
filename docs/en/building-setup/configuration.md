# Building Configuration

Building configuration is the first step in any Dybee implementation. Settings entered here are used throughout the platform — for energy calculations, weather data, and cost analysis.

## Required Settings

Navigate to **Administration → Building Settings** to configure:

| Setting | Description |
|---|---|
| Building name | Display name across all modules |
| Floor area | Used for energy intensity calculations (kWh/m²) |
| Currency | Applied to all cost calculations |
| Latitude / Longitude | Used to retrieve weather data from NASA |

## Weather Data

Dybee automatically retrieves outdoor temperature and climate data from NASA using the building's coordinates. This data feeds into:

- Baseline regression models
- Degree-day calculations
- The Temperature widget on dashboards

Accurate coordinates are required for weather data to function correctly.

## Next Steps

Once the building is configured:

1. [Add users and assign roles](users.md)
2. [Set up energy sources](../energy-monitoring/sources.md)

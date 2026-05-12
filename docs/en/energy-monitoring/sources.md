# Energy Sources

## What is an Energy Source?

An energy source represents a utility meter or energy type for a building — electricity, natural gas, district heating, water, etc. Each source collects consumption data and feeds into the building's energy totals.

## Creating an Energy Source

Navigate to **Energy Monitoring → Sources** and create an entry for each meter or utility type:

| Field | Description |
|---|---|
| Name | Label for the source (e.g., "Main Electricity Meter") |
| Energy type | Electricity, gas, thermal, water, etc. |
| Unit | Native billing unit (kWh, m³, GJ, etc.) |
| Include in total consumption | Must be enabled for the source to count toward building totals |

!!! warning
    The **Include in total consumption** checkbox must be enabled. Sources without it checked are excluded from all consumption totals and dashboard widgets.

## Multiple Sources

A building can have multiple sources of the same energy type (e.g., two electricity meters). Each is tracked independently and combined in the total when both are included.

## Units and Conversions

Dybee automatically converts all sources to a common set of display units for reporting:

- Native units (as entered)
- kWh equivalent
- GJ
- CO₂ (kg)
- Cost (in the building's configured currency)

# KPIs

!!! info "Analytics Plan"
    This feature requires the Analytics Plan.

## What is a KPI?

A KPI (Key Performance Indicator) is a numeric metric calculated hourly for each entity in a family. Unlike rules (which return 0 or 1), KPIs return quantitative values — efficiency ratios, energy totals, temperature differentials, etc.

KPIs are the primary building blocks for dashboard widgets and cross-entity analysis.

## Creating KPIs

KPIs are defined on a family in **Modeling → Families → KPIs**. Each KPI requires:

| Field | Description |
|---|---|
| Name | Display label |
| Alias | Short code used in formula references |
| Formula | Calculation expression |
| Unit | Display unit (°C, kWh, %, etc.) |

## Referencing KPIs in Formulas

KPIs can be referenced in other formulas using:

```
[EntityName].kpi.ALIAS
```

Or, within a family rule or KPI using hierarchy navigation:

```
kpi.ALIAS          — this entity's KPI
parent.kpi.ALIAS   — parent entity's KPI
load.kpi.ALIAS     — load entity's KPI
```

**Example — Reference a coil's efficiency in an AHU rule:**
```
load.kpi.COIL_EFF < 0.6
```

## KPI Pyramids

The **KPI Pyramid** dashboard widget displays the worst-performing entities for a selected KPI across a family, making it easy to identify outliers in large portfolios with many entities.

## Enabling and Disabling

Like rules, KPI calculations can be disabled at the family or entity level to reduce computation on inactive or excluded entities.

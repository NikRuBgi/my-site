# Formula Types

!!! info "Analytics Plan"
    This feature requires the Analytics Plan.

## Independent Formulas

Independent formulas reference raw BACnet acquisition points directly, without using the model hierarchy. Point names are wrapped in curly braces.

**Syntax:** `{point_name}`

**Example:**
```
({Supply_Air_Temp} - {Return_Air_Temp}) * {Air_Flow_Rate} * 1.2
```

Use independent formulas when:

- You need a simple calculation from raw points
- The formula does not need to generalize across multiple entities
- You are working outside the context of a family rule or KPI

## Targeted Formulas

Targeted formulas reference entities in the building model and navigate their relationships. Entity names are wrapped in square brackets.

**Syntax:** `[EntityName].tag.TAGNAME` or `[EntityName].kpi.ALIAS`

**Example:**
```
[AHU-01].tag.SA_T - [AHU-01].tag.OA_T
```

Use targeted formulas in **rules and KPIs**, where the formula must work generically across all entities in a family. In that context, you use hierarchy functions instead of a specific entity name — the formula is evaluated in the context of each entity.

**Example rule (applies to every AHU in the family):**
```
tag.SA_T > tag.OA_T + 5
```

## Hourly Aggregation

Raw data points are acquired at sub-hourly intervals. When used in rules and KPIs (which calculate hourly), append an aggregation suffix:

| Suffix | Description |
|---|---|
| `.avg` | Hourly average |
| `.max` | Hourly maximum |
| `.min` | Hourly minimum |
| `.tot` | Hourly total (sum) |

**Example:** `tag.SA_T.avg` — average supply air temperature for the hour.

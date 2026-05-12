# Model Hierarchy Navigation

!!! info "Analytics Plan"
    This feature requires the Analytics Plan.

## Overview

Targeted formulas can navigate the energy flow relationships in the building model. This allows a single rule or KPI to reference connected entities without hardcoding specific names.

## Navigation Functions

| Function | Description |
|---|---|
| `parent` | The equipment entity that contains this component |
| `child` | A component entity contained within this equipment |
| `source` | The entity supplying energy to this entity |
| `load` | The entity receiving energy from this entity |
| `firstLoad` | The first entity in the downstream (load) hierarchy |
| `firstSource` | The first entity in the upstream (source) hierarchy |
| `anyLoad` | All entities in the full downstream hierarchy; returns their average |
| `anySource` | All entities in the full upstream hierarchy; returns their average |
| `anyLoadSib` | Sibling entities sharing the same load connection |
| `anySourceSib` | Sibling entities sharing the same source connection |

## Examples

**Reference a parent entity's tag:**
```
parent.tag.OA_T.avg
```

**Reference a load entity's KPI:**
```
load.kpi.EFFICIENCY
```

**Check if any downstream entity has a fault:**
```
anyLoad.kpi.FAULT_RULE > 0
```

## Standard Tag Aliases

These tag names are used by convention in the Factory Library and BGI-supplied families:

| Alias | Description |
|---|---|
| `OA_T` | Outdoor air temperature |
| `SA_T` | Supply air temperature |
| `RA_T` | Return air temperature |
| `AHU` | Air handling unit reference |
| `HC` | Heating coil |
| `T` | Generic temperature sensor |

Following these conventions ensures that imported Factory Library rules and templates work without modification.

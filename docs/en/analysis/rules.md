# Rules

!!! info "Analytics Plan"
    This feature requires the Analytics Plan.

## What is a Rule?

A rule is a formula defined on a family that evaluates to `1` (fault condition) or `0` (normal) for each entity in that family, calculated every hour. When a rule returns `1`, the corresponding entity appears in the Fault Detection module.

## Writing Rules

Rules are written in the [Query Page](../formulas/index.md) using the formula syntax. A rule should express the **abnormal** condition — when it is true, a fault is detected.

**Example — Supply air temperature too high:**
```
tag.SA_T.avg > tag.SA_SP.avg + 3
```
Returns `1` when the average supply air temperature exceeds the setpoint by more than 3°C.

**Example — Fan running outside occupied hours:**
```
tag.FAN_STATUS.avg > 0.5 AND schedule() = 0
```
Returns `1` when the fan is on during unoccupied hours.

## Rule Configuration

Each rule has:

| Field | Description |
|---|---|
| Name | Displayed in the Fault Detection module |
| Alias | Short code for formula reference |
| Formula | The fault condition expression |
| Priority | 0–5; controls color coding in fault detection (red = 0–1, orange = 2–3, yellow = 4–5) |
| Email notification | Optional; triggers an alert when a fault is detected |

## Enabling and Disabling Rules

Rules can be toggled at the **family level** (applies to all entities) or at the **individual entity level** (e.g., to suppress known false positives on a specific unit while keeping the rule active for others).

## Rule Calculation Timing

All rules run hourly. There is no on-demand recalculation — results from the previous hour are always displayed.

# Fault Detection

!!! info "Analytics Plan"
    Fault detection requires the Analytics Plan.

## Overview

The Fault Detection module surfaces active rule violations across all modeled entities. Rules run hourly — when a rule returns `1` for an entity, that fault appears here until it is resolved or acknowledged.

Navigate to **Analysis → Fault Detection**.

## Filtering Faults

Use the filter bar to narrow the fault list:

| Filter | Options |
|---|---|
| Entity scope | Specific component, full family, or all entities |
| Status | Handled / unhandled |
| Text search | Filter by entity name or rule name |

## Priority Color Coding

| Color | Priority Level |
|---|---|
| Red | 0–1 (critical) |
| Orange | 2–3 (high) |
| Yellow | 4–5 (medium) |
| Green | Addressed / resolved |

Priority is set when the rule is defined. See [Rules](../analysis/rules.md) for configuration details.

## Actions per Fault

For each detected fault, you can:

| Action | Description |
|---|---|
| View rule details | Inspect the formula and its recent evaluation history |
| Create a task | Open a corrective commissioning task linked to this fault and entity |
| Open Explorer | Jump to a point-level trend view for the affected entity |
| Open Query Page | Run ad-hoc formula analysis on the entity's data |
| Toggle email alerts | Enable or disable email notification for this rule on this entity |

## Workflow

The recommended fault investigation flow:

1. Filter to unhandled, high-priority faults
2. Review the rule details to understand the condition
3. Open the Explorer to examine the relevant data points
4. If the fault is confirmed: create a corrective task
5. If the fault is a false positive: disable the rule for that entity or adjust the rule threshold

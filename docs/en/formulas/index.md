# Formulas & Calculations — Overview

!!! info "Analytics Plan"
    Formulas and calculations require the Analytics Plan.

## What are Formulas Used For?

Formulas in Dybee are used to:

- Calculate **virtual points** from raw data (e.g., derived efficiency metrics)
- Define **rules** for automated fault detection
- Define **KPIs** for performance tracking
- Perform ad-hoc analysis in the **Query Page**

## Formula Editor

The primary environment for writing and testing formulas is the **Query Page**, accessible from the Analysis module. It allows you to write a formula, select a time range, and validate the result before saving it as a rule or KPI.

## Formula Syntax

Formulas follow a syntax similar to Excel but leverage the building model hierarchy. Two types exist:

- **Independent formulas** — reference raw BACnet points directly
- **Targeted formulas** — navigate the entity model using relationships

See [Formula Types](types.md) for details, and the [Functions Reference](functions.md) for the complete list of available operators and functions.

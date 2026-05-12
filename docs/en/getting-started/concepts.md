# Key Concepts

Understanding these terms is essential before working with Dybee's modeling and analysis features.

## Structural Framework

Dybee organizes building systems in a hierarchy. At the top is the **building**, which contains **families**, which group **entities**.

### Entity

An entity represents a single building system component — an air handling unit, a pump, a coil, a sensor, etc. Entities are the core unit of the Dybee model. Each entity has:

- Associated data points (operational readings from BACnet)
- Tags and parameters for cross-entity standardization
- Linked rules, KPIs, tasks, notes, and files

### Family

A family is a group of similar entities. Families define the rules, KPIs, and templates that apply to all their member entities. There are four family types:

| Type | Description |
|---|---|
| Building | Top-level grouping representing the facility |
| Equipment | Major systems (e.g., AHU, chiller, boiler) |
| Component | Sub-systems within equipment (e.g., heating coil, fan) |
| Instrument | Individual sensors and measurement devices |

### Energy Flow

An energy flow is a directional relationship between entities, indicating which entity supplies energy to which. Flows are used in formula hierarchy navigation (`source`, `load`) and in energy modeling.

## Analysis Concepts

### Rule

A rule is a logical formula that evaluates to `0` (normal) or `1` (fault). Rules run hourly against all entities in their family and trigger alerts in the Fault Detection module when the result is `1`.

### KPI

A KPI (Key Performance Indicator) is a quantifiable metric calculated per entity. KPIs can reference rules, data points, and other KPIs, and are reusable in formulas via `[Entity].kpi.ALIAS`.

### Digital Twin

The digital twin is the complete model of a building's electromechanical systems — its entities, their relationships, their data points, and their behavioral rules. Stages 3 and 4 of the implementation methodology build and operate the digital twin.

## Energy Monitoring Concepts

### Baseline Model

A statistical regression model that predicts expected energy consumption based on influence factors (outdoor temperature, degree days, occupancy). Used to calculate savings by comparing actual vs. predicted consumption.

### IPMVP

The International Performance Measurement and Verification Protocol. Dybee uses IPMVP-compliant baseline modeling for energy savings measurement and verification.

# Digital Twin Overview

!!! info "Analytics Plan"
    Building modeling requires the Analytics Plan.

## What is the Digital Twin?

The digital twin is a structured software representation of a building's electromechanical systems. In Dybee, it consists of:

- **Entities** — individual systems and components (AHUs, pumps, coils, sensors)
- **Families** — groups of similar entities that share rules, KPIs, and templates
- **Energy flows** — directional relationships between entities indicating energy transfer

The digital twin is the foundation for all analytical features: real-time data visualization, fault detection, KPI calculation, and formula-based analysis.

## Modeling Workflow

Build the model in this order:

1. **Define families** — import from the Factory Library or create from scratch; configure tags, parameters, and templates
2. **Create entities** — instantiate individual systems as members of their respective families
3. **Associate data points** — link BACnet acquisition points to entity operations
4. **Map energy flows** — establish source/load relationships between entities
5. **Enable rules and KPIs** — activate fault detection and performance monitoring

See the following pages for details on each step:

- [Families & Templates](families.md)
- [Entities](entities.md)
- [Energy Flows](energy-flows.md)

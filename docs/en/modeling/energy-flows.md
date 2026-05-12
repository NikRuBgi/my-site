# Energy Flows

!!! info "Analytics Plan"
    This feature requires the Analytics Plan.

## What is an Energy Flow?

An energy flow is a directional relationship between two entities indicating that one supplies energy to the other. Flows are used to:

- Represent the physical topology of a building's systems
- Enable hierarchy navigation in formulas (`source`, `load`, `parent`, `child`)
- Support energy flow analysis in dashboards and reports

## Source and Load

Each flow has a direction:

- The **source** entity supplies energy (e.g., a boiler supplying hot water)
- The **load** entity receives energy (e.g., a heating coil receiving hot water from the boiler)

In formulas, you navigate these relationships using `source` and `load` functions. See [Model Hierarchy Navigation](../formulas/hierarchy.md) for the full syntax.

## Configuring Flows

Energy flows are defined in **Modeling → Entities** by editing an entity's relationships. Select the source or load entity from the available entity list within the building model.

!!! tip
    Accurate energy flow mapping is important for formulas that traverse the model hierarchy. Incomplete flows may cause formula errors or unexpected results in rules and KPIs.

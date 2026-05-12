# Entities

!!! info "Analytics Plan"
    This feature requires the Analytics Plan.

## What is an Entity?

An entity is a single instance of a building system — one specific AHU, one pump, one temperature sensor. Entities are members of a [family](families.md) and inherit its rules, KPIs, and template structure.

## Creating Entities

Navigate to **Modeling → Entities** and select the target family. For each entity:

1. Enter a name and description
2. Assign it to the correct family (Equipment, Component, or Instrument)
3. Associate operational data points acquired via BACnet
4. Assign tags to map points to their family-defined roles
5. Set parameter values specific to this instance (setpoints, thresholds)

## Associating Data Points

Each entity has an **Operations** section listing all data points assigned to it. Points are sourced from the BACnet acquisition layer (see [Data Acquisition](../data-acquisition/index.md)).

When assigning a point, select the appropriate **tag** to tell Dybee what that point represents in the context of the family's rules and KPIs.

## Entity-Level Documentation

Each entity has dedicated spaces for:

- **Notes** — free-text observations and modeling decisions
- **Tags** — metadata for filtering and analysis
- **Linked tasks** — commissioning measures associated with this entity
- **Comments** — typed annotations (bookmark, defect, calibration, etc.)
- **Files** — technical documents, plans, and datasheets

## Replicating Entities

When multiple sections of a building contain identical equipment, entities can be replicated to avoid repetitive configuration. Review tag assignments and parameter values after replication to ensure correctness for each instance.

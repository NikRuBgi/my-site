# Families & Templates

!!! info "Analytics Plan"
    This feature requires the Analytics Plan.

## What is a Family?

A family is a group of entities of the same type (e.g., all air handling units in a building). Families define the rules, KPIs, tags, parameters, and templates that apply uniformly to every entity in the group.

Families are designed to manage datasets with thousands of data points across many entities without requiring per-entity configuration.

## Family Types

| Type | Role in the model |
|---|---|
| Building | Top-level container representing the facility |
| Equipment | Major mechanical systems (AHU, chiller, boiler, etc.) |
| Component | Sub-systems within equipment (heating coil, fan, damper) |
| Instrument | Sensors and measurement points |

## Configuration Page

Families are created and managed from **Modeling → Families**. The configuration page is the central hub for:

- Creating and editing families
- Managing tags and parameters
- Defining templates (Gabarits)
- Writing rules and KPIs
- Enabling optimization hints

## Tags and Parameters

**Tags** are metadata labels assigned to data acquisition points within an entity. They standardize point naming across all entities in a family, enabling rules and KPIs to reference `OA_T` (outdoor air temperature) rather than a device-specific point name.

**Parameters** are configurable values specific to each entity instance — setpoints, thresholds, design values — that rules and KPIs can reference.

## Templates (Gabarits)

A template is a pre-defined entity configuration for a specific equipment type. It specifies which component and instrument families the equipment should contain, which tags to expect, and how the entity should be structured.

Templates accelerate model creation when many entities share the same structure (e.g., 20 similar AHUs across a portfolio).

## Factory Library

The Factory Library is a collection of pre-built family configurations provided by BGI. Importing from the Factory Library gives you a ready-made set of tags, parameters, templates, rules, and KPIs for common equipment types.

**To import a family:**

1. Navigate to **Modeling → Families → Import**
2. Select the source: Factory Library or another project
3. Review and confirm the import

!!! tip
    Start with Factory Library imports where possible. Customizing an existing family is faster than building one from scratch.

## Calculation Frequency

Rules and KPIs defined on a family calculate **hourly** for every entity in that family. Calculations can be disabled at the family level or for individual entities.

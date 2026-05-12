# Explorer & Point Sets

!!! info "Analytics Plan"
    The Explorer requires acquired data points, which are available on the Analytics Plan. The mini-explorer is available on all plans for energy data.

## What is the Explorer?

The Explorer is Dybee's primary interface for browsing, visualizing, and analyzing time-series data. It supports real-time and historical views of any acquired BACnet point or calculated formula.

## Access Points

The Explorer is accessible from multiple locations:

- **Main navigation** — Visualization → Explorer
- **Fault Detection module** — directly from a fault card to investigate the relevant points
- **Dashboard widgets** — the Explorer widget links to a pre-configured view

## Mini-Explorer

The mini-explorer is a lightweight popup for quick inspection of a single point. It shows recent trend data without requiring a full Explorer session. Useful for rapid verification during fault investigation.

## Point Sets

A **point set** is a saved collection of points that you regularly analyze together (e.g., all temperature sensors on AHU-01). Point sets allow you to open a multi-point trend view in one click.

**To create a point set:**

1. Open the Explorer
2. Select the points you want to include
3. Save the selection as a named point set

Point sets are personal by default but can be shared across users on the same building.

## Binary Points

Binary (on/off) points are displayed as a status timeline rather than a numeric trend. This makes it easy to visualize equipment run times, valve states, and alarm conditions alongside analog data.

## Filters

The Explorer supports conditional filtering to show only the data matching a specific condition — useful for isolating fault conditions or comparing behavior during occupied vs. unoccupied hours.

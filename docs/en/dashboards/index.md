# Dashboard Structure

## What is a Dashboard?

A dashboard is a configurable monitoring page composed of widgets. It provides a synthesized view of operational data, energy performance, fault status, and task progress for a building.

Each user has a **personal dashboard** and can access the building's **default dashboard** and dashboards created by teammates.

## Grid Layout

Dashboards use a grid-based layout:

- **4 columns × 4 rows** per page
- Widgets are **1–4 columns wide** and **1 row tall**
- Multiple pages can be added to a single dashboard for organizing different analyses

## Pages

A dashboard can have multiple pages. Each page is configured independently with:

| Setting | Description |
|---|---|
| Title | Label shown in the page tab |
| Auto-load | Whether the page loads automatically (disable for resource-heavy pages) |
| Maximum entities | Limits automatic loading of large families |
| Maximum time range | Prevents overly long calculation windows |
| Family parameters | Default parameter context for entity-targeted widgets |
| Page order | Controls tab ordering |

## Adding Widgets

Click the **+** button to add a widget to a page. Select the widget type, configure it, and position it on the grid. See [Widget Reference](widgets.md) for all available widget types.

## Dashboard Selection

Use the dropdown at the top of the Dashboard module to switch between:

- Your personal dashboard
- The building's default dashboard
- A teammate's dashboard (read-only)

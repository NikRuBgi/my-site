# Dashboard Templates

## What is a Dashboard Template?

A template is a dashboard page that acts as a **master configuration**. Child dashboards across other buildings inherit the template's layout and widgets. When the parent template is updated, all linked child pages update automatically.

This enables centralized management of standardized dashboards across large portfolios without manually updating each building.

## Requirements

For templates to work correctly across buildings:

- All buildings must follow the **same modeling conventions** — identical tag names, KPI aliases, and parameter names
- For example, outdoor air temperature must be mapped to tag `OA_T` in every building where the template is deployed

Inconsistent modeling will cause template widgets to fail or display no data in buildings that don't match the expected structure.

## Creating a Template

1. Build the dashboard page on the parent building site
2. Open **Page Settings** (edit mode)
3. Enable the **Template** option
4. Save

## Deploying a Template to a Child Building

1. Log into the child building site
2. Open the Dashboard module
3. Add a new page and select the template from the available list
4. Save

Child pages are read-only — they cannot be edited directly. To customize a child page for a specific building, **duplicate the page** first, then modify the copy independently (it will no longer receive parent updates).

## Identifying the Parent

To find which parent template generated a child page, open the page's edit function — it displays the parent site name and page name.

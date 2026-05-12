# Sharing & Importing Dashboard Pages

## Importing Pages from Other Users

Dashboard pages can be imported from teammates within the same building or from other buildings you have access to.

**To import a page:**

1. Open your dashboard in edit mode
2. Select **Import Page**
3. Choose the source: same building or another building
4. Select the page to import
5. Review any compatibility warnings
6. Save to complete the import

## Compatibility Warnings

When importing a page from a different building, Dybee checks whether the source building's modeling is compatible with the target building:

- **Missing entities or families** — a widget targeting an entity that doesn't exist in the target building will be flagged
- **Missing data points** — widgets referencing acquisition points that aren't available will not display data
- **Missing KPIs or rules** — formula-based widgets may fail if the target model doesn't have the same KPIs defined

!!! warning
    Always review compatibility warnings before saving an imported page. Importing without resolving incompatibilities will result in empty or broken widgets.

## Duplicating Pages

Any dashboard page (including imported ones) can be duplicated. Duplicates are fully editable and are independent of the source page — changes to the original do not affect the copy.

This is the recommended approach when you want to use an existing page as a starting point but need to adapt it for a specific building.

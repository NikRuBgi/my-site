# Charts

## Overview

The Charts module allows you to create persistent, named visualizations from any combination of data points and formulas. Charts are collaborative — all users with access to the building can view and use them.

Charts can be embedded in dashboards and reports, and are accessible from the Visualization tab, the Analysis module, and directly from entity pages.

## Creating a Chart

Navigate to **Visualization → Charts → New**:

1. Enter a title and optional description
2. Select a chart type
3. Add data series — select points from the Explorer or write a formula
4. Configure filters (time range, conditional filters)
5. Set Y-axis labels, min/max values, and multi-axis options if needed

## Chart Types

| Type | Best For |
|---|---|
| Line | Continuous trends over time |
| Column | Periodic totals (hourly, daily) |
| Area | Volume or cumulative data |
| Bar | Horizontal comparison |
| Scatter Plot | Correlation between two variables |
| Stepped | On/off or state changes |
| Column Stacked | Multi-source contribution to a total |
| XY Scatter Plot | Regression analysis (linear, polynomial) |
| Occurrence | Frequency distribution / histogram |
| Heatmap | Hourly data across days (ideal for occupancy and usage patterns) |
| Calendar | Daily values shown across a full year |
| Pie Chart | Proportional breakdown |

## Regression Analysis

The XY Scatter Plot type supports **linear and polynomial regression**. Add a regression line to quantify the relationship between two variables — useful for validating baseline assumptions or analyzing equipment efficiency curves.

## Dynamic Date Ranges

Charts support both fixed date ranges and dynamic ranges such as "last 7 days" or "last 24 hours". Dynamic ranges keep the chart current without reconfiguration, making them suitable for dashboard embedding.

## Filters

Apply **temporal filters** (time of day, day of week) or **conditional filters** (show only data when a condition is true) to isolate specific operating modes for comparison.

# Point Configuration & Deployment

!!! info "Analytics Plan"
    This feature requires the Analytics Plan.

## Selecting Points

From the filtered BACnet object list, select the points to acquire. For each point, configure:

| Setting | Description |
|---|---|
| Acquisition interval | How frequently the point is polled (e.g., every 5 minutes) |
| Precision | Number of decimal places stored |
| Historical logging | Enable to store trend data for analysis |

Choose acquisition intervals based on the point's purpose:

- **Status and setpoints** — 15–30 minute intervals are typically sufficient
- **Energy and power readings** — 15-minute intervals for demand analysis
- **Control sequences** — 5-minute or shorter for fault detection accuracy

## Deploying to Dybee-Link

Once points are configured, the settings must be deployed to the on-site Dybee-Link mini-PC.

1. Review the pending configuration changes
2. Click **Deploy**
3. The Dybee-Link downloads the new configuration and begins acquiring the selected points

!!! warning
    Deployment pushes changes to the physical Dybee-Link device. Verify the configuration before deploying, especially acquisition intervals, as high-frequency polling of many points can increase network load.

## After Deployment

Acquired points become available in:

- **Explorer** — for real-time and historical trend visualization
- **Entity Operations** — for assignment to entities in the digital twin
- **Formulas** — as `{point_name}` references in independent formulas

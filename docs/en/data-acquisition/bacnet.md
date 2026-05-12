# BACnet Connection

!!! info "Analytics Plan"
    This feature requires the Analytics Plan.

## Device Discovery

Once the Dybee-Link is online, navigate to **Administration → Data Acquisition** to begin the BACnet setup.

**Step 1 — Discover devices:**
Dybee scans the BACnet network and lists all visible controllers and devices. Select the devices that contain the points you want to acquire.

**Step 2 — Acquire BACnet objects:**
For each selected device, Dybee retrieves the list of available BACnet objects (Analog Input, Binary Input, Analog Value, etc.).

## Filtering Points

The full point list from a BMS can contain thousands of objects. Use the filter tools to narrow down to relevant points:

- Filter by device
- Filter by object type
- Filter by name pattern

Select only the points needed for your entities. Unnecessary points increase network load and data storage without analytical value.

## BACnet Write

Dybee supports BACnet write operations in addition to reads, allowing setpoint adjustments or command triggers directly from the platform when write access is granted by the BMS.

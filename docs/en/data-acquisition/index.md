# Data Acquisition — Overview & Prerequisites

!!! info "Analytics Plan"
    Data acquisition requires the Analytics Plan and Dybee-Link hardware.

## Overview

Dybee acquires real-time operational data from building systems via the **BACnet** protocol. An on-site hardware gateway — the **Dybee-Link** mini-PC — communicates with the building's BMS and forwards data to the Dybee cloud.

## Prerequisites

Before the acquisition interface becomes accessible:

1. **BGI completes baseline site configuration** — the building model structure must be in place before points can be mapped to entities.
2. **Dybee-Link is installed on-site** — the mini-PC must be physically installed and connected to the building network.
3. **IT coordination is complete** — the Dybee-Link requires network access to the BACnet devices and outbound internet connectivity to the Dybee cloud.

## Acquisition Flow

```
BACnet Devices → Dybee-Link (on-site) → Dybee Cloud → Entity Operations
```

Once configured, the Dybee-Link continuously polls the selected BACnet points at defined intervals and logs historical data to the cloud.

## Next Steps

- [BACnet Connection](bacnet.md) — discover devices and objects
- [Point Configuration](points.md) — select points, set intervals, and deploy

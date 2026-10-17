# A · Industrial fuel management system

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="img/fuel-management-dark.svg">
  <img alt="Architecture: Flow meter pulser to Industrial Pi PLC to Node-RED transaction logic to Operator PWA to Thermal receipt to Sync over MQTT / API to ERP records" src="img/fuel-management-light.svg" width="100%">
</picture>

**Status:** Operational (Owner-verified, 17 Oct 2026)

## Challenge

Every litre dispensed has to become an accurate, attributable record — linked to a vehicle, driver and company — even when the site's uplink is down, and without double-counting when it comes back.

## My contribution

Engineering of the edge, application and integration layers: pulse acquisition, transaction logic, operator PWA, receipt printing and ERP synchronisation.

## Approach

- Pulse inputs from the meter's pulser are counted on an industrial Raspberry Pi controller and converted to volume at the edge, so measurement never depends on the network.
- Node-RED flows own the transaction lifecycle: open ticket, live volume, close ticket, persist locally.
- An offline-first PWA gives the operator vehicle and driver registration, live volume and ticket closing on a phone or tablet.
- Closed transactions print as thermal receipts on site and queue for synchronisation to the ERP, with retries and duplicate prevention.
- Transaction history and spreadsheet exports come from the same records, so the printed receipt, the local log and the ERP agree.

## Architecture

- **Flow meter pulser** (field) — Emits pulses proportional to volume dispensed.
- **Industrial Pi PLC** (control) — Counts pulses on GPIO inputs and converts them to volume.
- **Node-RED transaction logic** (edge) — Ticket lifecycle, local persistence and sync queue.
- **Operator PWA** (app) — Registration, live volume and ticket closing, offline-capable.
- **Thermal receipt** (operator) — Printed record handed over at the pump.
- **Sync over MQTT / API** (transport) — Retries and duplicate prevention when the uplink returns.
- **ERP records** (backend) — Transactions land in Frappe for reporting and billing.

## Capabilities

- Vehicle registration
- Driver details
- Company association
- Live fuel volume monitoring
- Pulse-to-volume calculation
- Fuel transaction creation
- Ticket closing
- Printed transaction receipts
- Transaction histories
- Spreadsheet exports
- Remote ERP integration
- Resilient connectivity

## Technologies

raspberry pi, compute module 4, industrial shields plc, piusi k400, gpio pulse inputs, node red, javascript, mqtt, pwa, frappe, thermal printing


# D · Fleet intelligence and telematics platform

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="img/fleet-intelligence-dark.svg">
  <img alt="Project card. D: Fleet intelligence and telematics platform — GPS telematics turned into operational intelligence: live maps, trip history and replay, geofences, driver behaviour, alerts and scheduled reports for fleet operations." src="img/fleet-intelligence-light.svg" width="100%">
</picture>

**Status:** Operational (Owner-verified, 17 Oct 2026)

## Challenge

Raw GPS and device events are noisy and voluminous. Dispatchers and fleet managers need the few events that matter, on a live map, with a history they can trust.

## My contribution

Engineering contribution to a fleet operations platform: telematics integration, event processing, alerting and reporting. Not a claim of sole ownership of every product feature.

## Approach

- Teltonika telematics devices report position and events; fleet data is handled through GpsGate.
- Events are filtered and classified — geofence crossings, harsh braking and acceleration, vehicle state — before they reach a person.
- Live maps, trip history and route replay give dispatch a shared operational picture.
- Alert rules and scheduled reports deliver driver-behaviour and fleet summaries without manual collection.

## Architecture

- **Vehicle telematics unit** (field) — GPS position, ignition and driving events.
- **Cellular uplink** (transport) — Low-bandwidth reporting from the vehicle.
- **Telematics platform** (backend) — Ingest, event filtering and rules.
- **Trip and event history** (data) — Replay, reports and audit.
- **Live map and alerts** (app) — Geofences, behaviour alerts, vehicle state.
- **Dispatch** (operator) — Act on alerts and assign work.

## Capabilities

- GPS fleet tracking
- Live maps
- Trip history
- Route replay
- Geofencing
- Driver behaviour
- Fleet alerts
- Vehicle state
- Scheduled reports

## Technologies

teltonika, gpsgate


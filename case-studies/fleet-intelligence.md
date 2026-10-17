# D · Fleet intelligence and telematics platform

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="img/fleet-intelligence-dark.svg">
  <img alt="Architecture: Vehicle telematics unit to Cellular uplink to Telematics platform to Trip and event history to Live map and alerts to Dispatch / response" src="img/fleet-intelligence-light.svg" width="100%">
</picture>

**Status:** Operational (Owner-verified, 17 Oct 2026)

## Challenge

Raw GPS and device events are noisy and voluminous. Dispatchers and security teams need the few events that matter, on a live map, with a history they can trust.

## My contribution

Engineering contribution to a fleet and security-operations platform: telematics integration, event processing, alerting and reporting. Not a claim of sole ownership of every product feature.

## Approach

- Teltonika telematics devices report position and events; fleet data is handled through GpsGate.
- Events are filtered and classified — geofence crossings, harsh braking and acceleration, vehicle state — before they reach a person.
- Live maps, trip history and route replay give dispatch a shared operational picture.
- Alert rules and scheduled reports deliver driver-behaviour and fleet summaries without manual collection.
- Dispatch, work-order, maintenance-planning and security-response workflows are designed to build on the same vehicle data.

## Architecture

- **Vehicle telematics unit** (field) — GPS position, ignition and driving events.
- **Cellular uplink** (transport) — Low-bandwidth reporting from the vehicle.
- **Telematics platform** (backend) — Ingest, event filtering and rules.
- **Trip and event history** (data) — Replay, reports and audit.
- **Live map and alerts** (app) — Geofences, behaviour alerts, vehicle state.
- **Dispatch / response** (operator) — Act on alerts and assign work.

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

## Scope areas requiring verification

The following are part of the wider platform this project contributes to; owner sign-off on their scope is still pending, so they are listed but not claimed as delivered:

- Dispatch
- Work orders
- Maintenance planning
- Security response workflows


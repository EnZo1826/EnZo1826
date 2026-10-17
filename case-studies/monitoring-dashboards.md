# H · Real-time monitoring and dashboard interfaces

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="img/monitoring-dashboards-dark.svg">
  <img alt="Architecture: Devices and edge nodes to Node-RED to MQTT / WebSockets to InfluxDB to Grafana and custom dashboards to Operator action" src="img/monitoring-dashboards-light.svg" width="100%">
</picture>

**Status:** Operational (Owner-verified, 17 Oct 2026)

## Challenge

Telemetry is only useful if an operator can read it at a glance, find the event that matters and export what a manager asks for — with timestamps in local time.

## My contribution

Dashboard design and implementation, live data plumbing and reporting views.

## Approach

- Grafana over InfluxDB for time-series trends and alarm panels.
- Custom HTML/CSS/JavaScript dashboards fed over WebSockets and MQTT for live tables and status views.
- Sorting, filtering and historical event views on the same data the live screen uses.
- Timezone-aware display (Africa/Windhoek) and downloadable reports.
- Dense, dark, high-contrast layouts designed for control-room use.

## Architecture

- **Devices and edge nodes** (field) — Telemetry and events.
- **Node-RED** (edge) — Normalise and route data.
- **MQTT / WebSockets** (transport) — Live push to screens.
- **InfluxDB** (data) — History for trends and reports.
- **Grafana and custom dashboards** (app) — Tables, alarms, status, exports.
- **Operator action** (operator) — Acknowledge, investigate, report.

## Capabilities

- Custom data tables
- Real-time telemetry
- Alarm dashboards
- Sorting and filtering
- Timezone-aware displays
- Downloadable reports
- System status
- Historical event views

## Technologies

grafana, influxdb, node red, javascript, html css, websockets, mqtt


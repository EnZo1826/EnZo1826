# C · Industrial monitoring and automation

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="img/industrial-monitoring-dark.svg">
  <img alt="Project card. C: Industrial monitoring and automation — PLC-based equipment telemetry, threshold logic and alarms, published over MQTT and WebSockets into historical trends and remote operator dashboards." src="img/industrial-monitoring-light.svg" width="100%">
</picture>

**Status:** Operational (Owner-verified, 17 Oct 2026)

## Challenge

Physical equipment speaks in registers, inputs and pulses. Operators and managers need states, alarms and trends — locally when the network is down and remotely when it is up.

## My contribution

Edge logic, protocol integration, data pipeline and dashboards for remote visibility of physical processes.

## Approach

- Industrial Raspberry Pi PLCs read digital and analog inputs and poll equipment over Modbus.
- Node-RED handles register decoding (signed and unsigned, 16- and 32-bit), threshold evaluation, process timers and machine-state transitions.
- Processing stays local during connectivity interruptions; services recover automatically after a reboot.
- Readings and events publish over MQTT and WebSockets to InfluxDB for history and to dashboards for live view.
- Grafana and custom operator screens show equipment state, alarms, historical trends and network connectivity.

## Architecture

- **Equipment and sensors** (field) — Digital, analog and Modbus sources.
- **Industrial Pi PLC** (control) — I/O acquisition and Modbus polling.
- **Node-RED edge logic** (edge) — Decoding, thresholds, timers, states, alarms.
- **MQTT / WebSockets** (transport) — Live telemetry and events.
- **InfluxDB** (data) — Time-series history.
- **Grafana and HMI screens** (app) — Live state, trends and alarm views.
- **Operator action** (operator) — Respond to alarms and process states.

## Capabilities

- Real-time equipment telemetry
- Digital and analog input handling
- Modbus register processing
- Threshold-based logic
- Process timers
- Alarm handling
- Network connectivity monitoring
- Historical trends
- Remote dashboards
- Operator interfaces

## Technologies

industrial shields plc, raspberry pi, node red, modbus, mqtt, websockets, grafana, influxdb, linux


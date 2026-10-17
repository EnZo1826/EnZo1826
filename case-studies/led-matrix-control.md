# E · Intelligent LED matrix control

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="img/led-matrix-control-dark.svg">
  <img alt="Project card. E: Intelligent LED matrix control — Microcontroller-driven HUB75 RGB LED matrices that display live process values, text and alarm states commanded over MQTT." src="img/led-matrix-control-light.svg" width="100%">
</picture>

**Status:** Operational (Owner-verified, 17 Oct 2026)

## Challenge

Operators on the ground need to read a process value or a warning from a distance, in daylight, and the display has to follow live data without anyone touching it.

## My contribution

Display firmware and the MQTT command interface that lets industrial data drive physical signage.

## Approach

- RP2040 (Pimoroni Interstate75 / Pico W) and ESP32-S3 boards drive HUB75 P4 64×32 RGB panels, including four-panel 2×2 layouts.
- MicroPython firmware handles multi-panel matrix mapping, centring, brightness and rendering.
- Node-RED publishes values and commands over MQTT; the display subscribes and renders text, flow rates and status.
- Configurable high/low thresholds change colours, and alarm modes flash for warning conditions.
- Background and text colours are configurable remotely over the same command channel.

## Architecture

- **Process data** (field) — Values from PLCs and sensors.
- **Node-RED** (edge) — Formats values and commands.
- **MQTT** (transport) — Display commands and live values.
- **RP2040 / ESP32-S3** (edge) — MicroPython render loop, thresholds, alarm modes.
- **HUB75 LED matrix** (app) — Four-panel 2×2 RGB display.
- **Operator on the ground** (operator) — Reads values and warnings at a distance.

## Capabilities

- Four-panel matrix operation
- Remote text commands
- Flow rate displays
- Warning conditions
- Customisable background and text colours
- Configurable flashing alarms
- Multi-panel rendering
- Live industrial data visualisation

## Technologies

rp2040, pico w, esp32 s3, micropython, hub75, interstate75, mqtt, node red


# B · Security checkpoint and visitor management

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="img/security-checkpoint-dark.svg">
  <img alt="Project card. B: Security checkpoint and visitor management — An offline-capable checkpoint PWA for registering visitors and vehicles, tracking check-in and check-out, and synchronising every movement to an ERP backend." src="img/security-checkpoint-light.svg" width="100%">
</picture>

**Status:** Operational (Owner-verified, 17 Oct 2026)

## Challenge

Gate staff need a fast, simple tool that keeps working when the connection drops, while the backend still needs a complete, traceable record of who and what entered and left — and from which device.

## My contribution

Design and implementation of the checkpoint application, its offline synchronisation and the backend integration.

## Approach

- A mobile-first PWA captures visitor and vehicle registrations, check-in and check-out at the gate.
- Transactions are stored locally first and synchronised through REST APIs, with per-record sync state so nothing is silently lost.
- Each device is identified, so every record shows where it was captured.
- Time-on-site and visitor status are derived from the transaction log rather than typed in.
- The backend is a Frappe / ERPNext integration, so checkpoint data sits alongside the organisation's other operational records.

## Architecture

- **Gate officer** (operator) — Registers visitors and vehicles at the checkpoint.
- **Checkpoint PWA** (app) — Mobile-first capture with local storage.
- **Local sync queue** (edge) — Per-record sync state, retries, device identity.
- **REST API** (transport) — Authenticated submission of transactions.
- **Frappe / ERPNext** (backend) — Stores visits and movements with an audit trail.
- **Reports and status** (app) — Who is on site, time on site, history.

## Capabilities

- Visitor registration
- Vehicle registration
- Check-in and check-out
- Visitor status
- Time-on-site calculation
- Notes and transaction metadata
- Device identification
- Synchronisation tracking
- Remote backend integration
- Operational transaction management

## Technologies

frappe, erpnext, nodejs, javascript, rest api, pwa


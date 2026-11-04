# Buzz Logistics Operations Dashboard — Prototype

A responsive, static front-end prototype for a Buzz Logistics partner/operations dashboard. It is intentionally independent of the public Buzz marketing website and does not require a backend.

## Open it

- Extract the ZIP.
- Open `index.html` in a modern browser, or serve the folder locally with `python -m http.server 8000` and visit `http://localhost:8000`.
- Sign in with the prefilled demo account, or select **Enter demo workspace**. The login is a visual demonstration only; any non-empty valid email/password will enter the demo.

## Included screens

- Login / operations workspace entry
- Overview with delivery KPIs, priority deliveries, activity and capacity
- Deliveries list with filters and search
- Clickable tracking codes with parcel information, journey stages and movement timeline
- Demo status update action
- Dispatch board and courier assignment simulation
- Employee directory with role and availability filters
- Fleet and vehicle register
- Delivery partners
- Service area coverage overview
- Reports and operational support

## Important prototype limitations

- All records are fictional sample data. Names, phone numbers, addresses, delivery values, tracking codes and operating figures are for demonstration only.
- No database, API, authentication provider, live GPS, messaging, payment service or document storage is connected.
- Interactions run in browser memory. Reloading the page resets them. The CSV export is generated locally from the sample data.
- The login screen does not authenticate users. Do not use real credentials.
- No real delivery should be dispatched or marked delivered from this prototype.

## Suggested production architecture

Before using this for real operations, connect:

1. Secure authentication with role-based access (owner/admin, dispatcher, hub manager, partner manager, courier, support, read-only auditor).
2. A delivery/order API and persistent event history. Tracking status should be event-driven and auditable; do not overwrite history when a status changes.
3. Courier and partner profiles, onboarding, identity/business verification, document expiry reminders and approval workflows.
4. Dispatch rules, capacity checks, service-zone eligibility, assignment acceptance/rejection and reassignment.
5. Vehicle records, insurance/roadworthiness expiry, maintenance and driver-to-vehicle assignments.
6. Proof of pickup/delivery, timestamp, geolocation, recipient confirmation and exception evidence.
7. Notifications, escalation rules, incident management, operational audit logs and reporting.
8. Data protection, retention, access controls, backups and security review appropriate to Nigerian operations.

## Vercel deployment

This is plain HTML/CSS/JavaScript. Import the folder/repository into Vercel with Framework Preset **Other**, no build command, and output directory `.`. `vercel.json` supplies basic headers and clean URL configuration. The current build can also be deployed as a static folder on any static host.
# Buzzdashboard

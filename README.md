# Buzz Logistics Partner Workspace — Prototype

A static HTML/CSS/JavaScript prototype for a shared Buzz + logistics partner visibility portal.

## Product direction

This is **not** a logistics company's CRM, fleet manager or internal operations suite. It is a shared workspace focused on Buzz orders and the information Buzz and its delivery partners need to exchange:

- Overview of Buzz deliveries assigned to the partner
- Clickable tracking codes with package information, courier reference and chronological product journey
- Shared event history and delivery exceptions
- Limited courier / partner-contact directory relevant to Buzz deliveries
- Partner profile information
- API connection request flow and a guided questionnaire for partners using other systems
- Individual and enterprise partner application flows, with stricter enterprise qualification questions
- Sample reporting for Buzz delivery activity

Fleet administration, vehicle registers, route planning, HR management, service-area configuration and other general logistics CRM features have deliberately been removed.

## Run locally

Open `index.html` in a browser, or run a static server from this directory:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Demo access

- Sign-in form is prefilled with a demo email and password.
- Select **Explore the demo workspace** to bypass the form.
- The application screen offers Individual and Enterprise partner applications.
- The Integration page provides an API connection request and an existing-system discovery questionnaire.

## Data and security limitations

This is a front-end-only demonstration. It has no authentication, database, server, file upload, API connection or permanent storage. Any status changes are in-memory and reset on reload. The API connection form is a discovery preview only. **Never enter live API keys, tokens, passwords, identity numbers or sensitive documents into this prototype.**

A production implementation should include:

1. Secure authentication, MFA and role-based access for Buzz administrators and partner users.
2. Server-side encrypted credential vault, least-privilege API scopes, rotation and audit logging.
3. Signed webhook validation, idempotent event ingestion, retries and event reconciliation.
4. A canonical Buzz tracking record and event schema shared across Buzz and partner integrations.
5. Data minimisation, retention rules, consent and access controls for recipient and courier personal information.
6. Enterprise due diligence and secure document collection outside this static demo.

## Deploy to Vercel

Deploy this folder as a static project with Framework Preset **Other**, no build command and output directory `.`.


## Partner onboarding update
The login screen now has a dedicated **Start partner onboarding** option. Applications are grouped into labelled steps with a visible progress bar, current-step label and completed-step indicators. Applicants can return to earlier completed sections without losing their entries.

Enterprise application sections cover legal details, business details, services and coverage, capacity and fleet, international shipping, systems/integration, and additional information. Questions include Nigerian states and cities covered, main service (international, domestic, both or other), vehicle types, years in delivery operations, current fleet size, daily/monthly capacity, international shipment capability, countries and routes covered, and a free-text additional-information field. Individual applications use an appropriately scaled version of the same operational questions.

The final application screen clearly states that Buzz Logistics is strictly for delivering goods and products purchased through the Buzz app, not unrelated third-party consignments. The login panel also uses a photographic delivery/warehouse background image loaded from Unsplash; an internet connection is required for that image.

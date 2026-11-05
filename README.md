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


## Partner onboarding (phased)
Sign-in has a **Start partner onboarding** option that opens a full-width screen with no side panel.
1. **The basics:** three short sections (about you, what you deliver with, how much you can take on). Open them in any order. Only name and phone are needed to move on.
2. **Meet the team:** pick a day and time for a short call.
3. **After the meeting:** the rest (coverage, fleet and capacity, international, systems for companies, documents), also in any order. Unlocks the final step once the meeting is done. The demo has a link to pretend it happened.
4. **Join Buzz:** confirmation, with a note that Buzz Logistics only delivers goods bought through the Buzz app.

The app uses the same blue theme and slow breathing gradient as the website. No photo is loaded from the internet.

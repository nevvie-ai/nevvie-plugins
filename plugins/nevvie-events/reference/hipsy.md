# Hipsy: what's possible (checked 2026-10-27)

Sources: docs.hipsy.nl and its source repo, Hipsy's own WordPress plugin, the Hipsy help center.

## API: read only

`https://api.hipsy.nl/v1`, header `Authorization: Bearer <key>`, 120 requests a minute.
Organisations (`/organisations/index`), events (`/organisation/{slug}/events`, `period=upcoming|
past|all`, `concepts=1` includes concept events), orders (`/organisation/{slug}/orders?event=<id>`),
reviews, current account. **No endpoint creates or changes events or tickets**: listing happens
in the dashboard. Zapier offers triggers only (new paid order, new event).

## Dashboard (hipsy.nl/app)

Server-rendered: everything below is done in the browser, by Claude with the owner watching or by
the owner.

Per event:
- **Bewerken**: title, date, text, photo, location; `privé evenement` (not in Hipsy search).
- **Instellingen**: ticket sales; `Notificaties ticketverkoop` (none / every sale / **Dagrapport**);
  information for participants (goes in Hipsy's order mail); `Vragen voor deelnemers` (custom
  questions, newsletter opt-in); `Evenement is onzichtbaar (concept modus)`.
- **Tickets**: `Ticket toevoegen` (normal, **Combi ticket** for duo/couple/group with its own price,
  donation); event limit (`Ticketlimieten wijzigen`) or per-ticket limit; `Onzichtbaar` tickets;
  ticket groups; sale start/end per ticket; VAT per ticket; `Kortingscode & Waardebonnen`.
- **Deelnemers**: resend tickets; `E-mail Deelnemers` (one message to all participants);
  `Exporteer` (CSV).
- **Verkopen**: orders; `Terugboeken` per order (refunds are manual).

Organisation: `Exporteren` (all participants incl. newsletter opt-ins), `Koppelingen` (API keys),
`Profiel` (slug). Not documented: duplicating events, recurring dates, waitlists.

Couples: make a single ticket with the limit, then a combi ticket of 2 singles with its own price;
the limit on the single ticket counts both, so a couple uses two places. Singles can be made
invisible so only the combi shows.

Fees: €0.80 service fee per ticket (buyer or organiser pays) + €0.35 per order (buyer). PayPal
+6.1% (buyer); credit card +2% / +3.9% (organiser; can be switched off per event).

## Hipsy's event policy

Events must serve personal development, connection or awareness. **Not allowed: sex parties,
erotic dance parties, orgies; nudity or explicit content in images or promotion; illegal or
regulated substances (ayahuasca and psilocybin are named); links to external ticket shops.**
Tantra facilitators can be asked for background checks. Violations can remove events and **block
the organiser**. So: every public Hipsy text and image follows this policy, framed around
connection, consent and learning. Explicit practical information belongs in the participant email,
which Hipsy doesn't publish. When an owner's own text crosses the line, flag it and let them decide.

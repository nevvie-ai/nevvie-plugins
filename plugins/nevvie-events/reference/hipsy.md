# Hipsy: what's possible (checked 2026-10-27)

Sources: docs.hipsy.nl and its source repo, Hipsy's own WordPress plugin, the Hipsy help center.

## API: read only

`https://api.hipsy.nl/v1`, header `Authorization: Bearer <key>`, 120 requests a minute.
Organisations (`/organisations/index`), events (`/organisation/{slug}/events`, `period=upcoming|
past|all`, `concepts=1` includes concept events), orders (`/organisation/{slug}/orders?event=<id>`),
reviews, current account. **No endpoint creates or changes events or tickets**: listing happens
in the dashboard. Zapier offers triggers only (new paid order, new event).

## Dashboard (hipsy.nl/app), as seen on a real run (2026-10-28)

Everything here is done in the browser, by Claude with the owner watching or by the owner.

**Events list** `hipsy.nl/app/events`: per event status (Concept or live), date, tickets sold and
revenue. Use it to keep `events/README.md` current, with or without an API key.

**Create page** `hipsy.nl/app/events/create`:
- Naam van het evenement; Datum (calendar: month arrows, or month and year dropdowns); Begintijd
  and Eindtijd (hours and minutes in separate boxes); switches *meerdere dagen* (then an end date
  appears) and *online*.
- Locatie: Google address autocomplete; type the address and pick the suggestion.
- *Extra informatie*: one **plain-text** box, no bold or headings. Put headings on their own line
  and use "- " for lists. Public, so it follows the policy below.
- Cover afbeelding: upload, or pick one from an earlier event; 16:9, 1920 × 1080.
- *Dit is een privé evenement* switch.
- Thema's, max 3; main groups Workshops, Ceremonies, Dans, Muziek, Festivals & Retraites,
  Lezingen & Voorstellingen, Overig (Tantra sits under Workshops). Gesproken taal (several
  allowed), Genderdoelgroep, Leeftijd, Doelgroep landen.
- Buttons: **Opslaan als concept** and *Evenement publiceren*. **Always use Opslaan als concept.**
- After the first save Hipsy asks how people sign up: **Tickets** or *Contactformulier*.

**Event pages** `hipsy.nl/app/events/<id>/overview | details | participants | tickets | settings`.

**Tickets** (`…/tickets`): event limits at the top (max per event, per order, per email).
*Ticket toevoegen* → Normaal ticket / Donatie / Combiticket.
- Normal ticket: name, description, group, price, *Entree ticket* switch, max tickets (untick
  *Evenement limiet* to give it its own limit), max per order, *Negeer evenement limiet*, status
  (Beschikbaar / Uitverkocht / Onzichtbaar / Niet beschikbaar), sale start (right away / date /
  after another ticket), sale end (end of event / start of event / date).
- Combiticket: pick existing tickets with a count each (at least two in total); the price starts
  as their sum, the pencil overrides it; it counts against the limits of the tickets inside.
  Same-gender couples need their own combi.
- Also: ticket groups, *Kortingscodes & Waardebonnen*. Hipsy shows the service fee per ticket.

**Settings** (`…/settings`), five tabs:
- `settings`: Registratiemogelijkheid, *Evenement is onzichtbaar (concept modus)*, contact and
  notification email, terms (PDF), co-organisers, *Evenement verwijderen*.
- `settings/tickets`: service fee on top of the price, credit card, buyers can request an
  invoice, reviews after the event, *Notificaties ticketverkoop* (none / every sale / Dagrapport),
  extra invoice text.
- `settings/communication`: **Informatie na aanschaffen tickets** (+ optional PDF). Hipsy sends
  this in the order confirmation: **this is the welcome email.** Put the filled-in
  `emails/welcome.md` here. Only buyers see it, so practical and explicit details that the public
  listing can't carry go here.
- `settings/form-questions`: Hipsy newsletter, own newsletter, optional buyer fields (gender,
  birth date, address, phone, diet, remark…), up to 3 open questions, each optionally required.
- `settings/ticketshop-design`: colours.

Also: `Deelnemers` (resend tickets, *E-mail Deelnemers*, CSV export) and `Verkopen` (orders,
manual refunds per order): totals only, never copy names.

Organisation: `Exporteren`, `Koppelingen` (API keys), `Profiel` (slug). Public pages:
`hipsy.eu/event/<id>-<slug>` and the shop `hipsy.eu/shop/<id>-<slug>`.

**Browser practicalities**
- Switch states can be read from `aria-checked`.
- Text typed with form tools may need one real keystroke afterwards before the page registers it.
- Never trigger *Evenement verwijderen*: its confirmation dialog blocks the browser.
- Check which browser is already signed in to Hipsy (Claude in Chrome usually is; the app's
  built-in browser may not be) before asking the owner to sign in.

Fees: €0.80 service fee per ticket (buyer or organiser pays) + €0.35 per order (buyer). PayPal
+6.1% (buyer); credit card +2% / +3.9% (organiser; can be switched off per event).

## Hipsy's event policy

Source: Hipsy help center, `beleidsrichtlijnen-voor-evenementen` (checked 2026-10-27). Events must
serve personal development, connection or awareness. Violations can remove events and **block
the organiser**, so a listing is checked against this list before it goes on Hipsy.

**Policy checklist** (public parts: title, *Extra informatie*, cover image, themes):
1. **Purpose:** it reads as personal development, connection, learning or awareness, not as an
   evening of pleasure alone.
2. **No sex party, erotic dance party or orgy** in words or framing ("play party", "sex-positive
   party", explicit percentages of play, playroom/BDSM room as the selling point).
3. **No explicit sexual content** in the text: name connection, consent, touch, sensuality,
   intimacy; leave explicit sexuality, kink details and nudity out of the public text.
4. **Image:** no nudity, nothing sexual or suggestive; 16:9.
5. **Substances:** no illegal or regulated substances (ayahuasca and psilocybin are named);
   plant-medicine events only with legal substances, with responsible-use information.
6. **Tickets only through Hipsy:** no links to other ticket shops or payment pages.
7. **Safety:** consent and boundaries are stated (a fixed part of every listing).

Whatever is cut from the public text for points 2–3 can go in the welcome text
(`settings/communication`), which only buyers see. Tantra facilitators can be asked for background
checks; that is the owner's business, not a listing change.

# Hipsy template (same for every organiser)

Every field Hipsy has for an event, where its value comes from, and the walkthrough. Hipsy's pages
are the same for every organiser; what differs per business lives in their `offer/hipsy-defaults.md`.
Mapped from a real organiser account on 2026-10-28. Details of each page: `hipsy.md`.

**Where a value comes from**
- *recipe*: the event type in `offer/<recipe>.md`. Same every time.
- *event*: the event file in `events/`. Different per date.
- *default*: the business's usual choice, in `offer/hipsy-defaults.md`. Asked only when different.
- *ask*: asked in chat, one question at a time (walkthrough below).

## 1. Bewerken (the event itself)

New: `hipsy.nl/app/events/create`. Existing: `hipsy.nl/app/events/<id>/details`.

| Field | Source | Notes |
|---|---|---|
| Naam van het evenement | recipe: `<Event name> · <Level>` | Per `offer/listing-template.md` if they have one |
| Datum | event | Calendar: month arrows, or month and year dropdowns |
| Begintijd / Eindtijd | recipe programme (first and last time) | Hours and minutes are separate boxes |
| Dit evenement duurt meerdere dagen | recipe (on for retreats) | Then an end date appears |
| Dit evenement vindt online plaats | default (usually off) | |
| Locatie | default: their address → pick the Google suggestion | |
| Extra informatie | recipe listing text, filled for this date | **Plain text only**: headings on their own line, "- " for lists. Public: follows Hipsy's policy |
| Cover afbeelding | event: the Canva image | 16:9, 1920 × 1080. Upload, or pick one from an earlier event. No nudity |
| Dit is een privé evenement | default (usually off) | On = not shown on Hipsy, only by link |
| Thema's (max 3) | default per event type | Groups: Workshops, Ceremonies, Dans, Muziek, Festivals & Retraites, Lezingen & Voorstellingen, Overig |
| Gesproken taal | recipe `Language:` | Several allowed |
| Genderdoelgroep | default | |
| Leeftijd | default | |
| Doelgroep landen | default | |
| Bottom buttons | **Opslaan als concept** | Never *Evenement publiceren*: the owner makes it live |

After the first save Hipsy asks how people sign up: **Tickets** or *Contactformulier* (default).

## 2. Tickets

Page: `hipsy.nl/app/events/<id>/tickets`.

- **Event limits** at the top: max per event, per order, per email (default; often left open with
  limits on the tickets).
- **Ticket toevoegen** → *Normaal ticket*, *Donatie*, *Combiticket*.
- Normal ticket: name, description, group, price, *Entree ticket* (on), max tickets (untick
  *Evenement limiet* for its own limit), max per order, *Negeer evenement limiet*, status
  (Beschikbaar / Uitverkocht / Onzichtbaar / Niet beschikbaar), sale start (right away / date /
  after another ticket), sale end (end of event / start of event / date).
- Combiticket: existing tickets with a count each (at least two); price starts as their sum, the
  pencil overrides it; counts against the limits of the tickets inside. Same-gender couples need
  their own combi.
- Ticket groups keep many types readable; *Kortingscodes & Waardebonnen* for discounts.
- Which tickets, prices and numbers: recipe + `offer/tickets.md`, shown as "same as last time?".

## 3. Instellingen (five tabs)

| Tab | Fields | Source |
|---|---|---|
| `settings` | Registratiemogelijkheid; **concept mode** (on until the owner goes live); contact and notification email; terms PDF; co-organisers; *Evenement verwijderen* (never touched by Claude) | default |
| `settings/tickets` | service fee on top; credit card; buyer invoice; reviews; *Notificaties ticketverkoop* (none / every sale / Dagrapport); invoice text | default |
| `settings/communication` | **Informatie na aanschaffen tickets** (+ PDF): Hipsy's order confirmation text = **the welcome email** | `emails/welcome.md` filled for this event, plus anything moved out of the public listing |
| `settings/form-questions` | Hipsy newsletter; own newsletter; optional buyer fields (gender, birth date, address, phone, diet, remark…); up to 3 open questions, each optionally required | default per event type |
| `settings/ticketshop-design` | colours | default (usually unchanged) |

## 4. Tracking (read only)

- Events list `hipsy.nl/app/events`: status (Concept / live), date, tickets, revenue → `events/README.md`.
- Overzicht `…/<id>/overview`: sales for one event.
- Deelnemers, Verkopen: names and orders. Totals only; never copy names.
- Public pages: `hipsy.eu/event/<id>-<slug>`, shop `hipsy.eu/shop/<id>-<slug>`.

## Walkthrough: a new event in chat

One question per message; each answer filled in right away; whatever the recipe, the defaults or
the last event of the same type already knows is shown, not asked.

1. **Which event?** From the recipes. A new type gets a recipe first.
2. **Which date?** Free weekends from their planning. Co-decider agreed?
3. **Anything different this time?** Facilitator, times, theme, overnight option.
4. **Tickets:** last time's set and prices: "same as last time?"
5. **Image:** the recipe's Canva design.
6. **Preview:** listing, tickets, welcome text and posts in one message, exactly as on Hipsy.
7. **Draft on Hipsy:** Claude fills sections 1–3, saves as concept, sends the link.
8. **Live:** the owner switches concept mode off. Claude updates `events/README.md`.

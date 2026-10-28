# The business folder (contract)

Every skill in this plugin reads and writes the owner's business folder in this shape. The
folder is plain text files, either in their Google Drive (synced to the computer with Google
Drive for desktop, kept available offline; the default) or in a git repository.

This folder is the contract between the plugin (same for everyone) and the business (theirs
alone). Paths are relative to the folder root.

Default place: Google Drive → My Drive → `Claude` → `<business name>`. Images, posters and
Google Sheets can sit next to it in `Claude`. On Windows that is under the Google Drive drive
(often `G:\My Drive\Claude`); on a Mac under `~/Library/CloudStorage/GoogleDrive-<account>/My Drive/Claude`.

| Path | Holds |
|---|---|
| `CLAUDE.md` | Who the business is in a few lines, who decides what, and a map of this folder |
| `about/owner.md` | The owner, partners, who decides dates, prices, tickets |
| `about/brand.md` | Brand(s), audience, tone, values, channels (Hipsy, newsletter, socials) |
| `about/voice.md` | How the owner writes; grows from every correction |
| `offer/README.md` | The offer at a glance: levels, formats, how events build on each other |
| `offer/<recipe>.md` | One recipe per event type (format below) |
| `offer/tickets.md` | Ticket rules: types, prices, age bands, couples/singles, screening |
| `offer/listing-template.md` | The owner's structure for a Hipsy listing (optional; default below) |
| `events/YYYY-MM-DD-<recipe>.md` | One file per dated event (format below) |
| `emails/<name>.md` | Participant email templates: `welcome`, `reminder`, `thank-you` |
| `place/` | The venue: address, route, facilities, house rules, prices (when they have one) |

**Never in the folder:** participants' personal data, passwords, API keys, exports of orders.

## Recipe (`offer/<recipe>.md`)

Everything that stays the same each time this event runs. Sections, in this order:

- Title line `# Recipe: <name>`
- `## Format`: level, programme with times, language, capacity, facilitators
- `## Tickets`: table `Ticket | Price | Quantity | Notes`
- `## Listing text`: the owner's own text, which is adapted per date, never rewritten without them
- `## What to bring`
- `## Emails`: which templates go out, plus anything specific to this event
- `## Promotion`: channels and timing
- `## Learned`: one dated line per event that ran

Missing information is written as **TODO**, never guessed.

## Event (`events/YYYY-MM-DD-<recipe>.md`)

Only what is specific to that date. Starts with:

```
# <Event title> · <date>
- Recipe: offer/<recipe>.md
- Status: draft | approved | listed | done
- Date and times:
- Hipsy: <event id> · <link>
- Image: <where the poster is>
```

Then `## Listing` (the final text as it goes on Hipsy), `## Tickets` (if different from the
recipe), `## Promotion` (the posts as approved), `## Sales` (totals only), `## Learned`.

## Default listing structure (when there is no `offer/listing-template.md`)

1. Title: `<Event name> · <Level>`
2. Short description, 2–4 sentences: what they will experience and why it matters; no practicalities
3. For whom, including the experience needed (or that none is needed)
4. What to expect, concretely
5. How it works: arrival, programme, breaks, partners
6. Safety and consent
7. Practical: date, time, location, price, level, for whom, overnight/food/duo/solo
8. What to bring (only what is really needed)
9. Tickets: short invitation to book

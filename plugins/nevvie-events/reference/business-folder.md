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
| `CLAUDE.md` | First line `Language: Nederlands` or `Language: English` (the owner's working language). Then who the business is, who decides what, and a map of this folder |
| `about/owner.md` | The owner, partners, who decides dates, prices, tickets |
| `about/brand.md` | Brand(s), audience, tone, values, channels (Hipsy, newsletter, socials) |
| `about/voice.md` | How the owner writes: the voice profile, every line backed by a quote (`voice` skill) |
| `about/voice-samples/` | Their own texts verbatim, one per file, first line `format: … · status: approved/rejected · source: …` |
| `about/voice-edits.md` | What they changed in drafts: before, after, why, date |
| `offer/README.md` | The offer at a glance: levels, formats, how events build on each other |
| `offer/<recipe>.md` | One recipe per event type (format below) |
| `offer/tickets.md` | Ticket rules: types, prices, age bands, couples/singles, screening |
| `offer/listing-template.md` | The owner's structure for a Hipsy listing (optional; default below) |
| `offer/hipsy-defaults.md` | This business's usual Hipsy choices: the *default* fields of the plugin's Hipsy template (location, themes, settings per tab, form questions), their ticket patterns per past event. Made by `hipsy-scan` or asked in `setup`. (Older folders may call it `offer/hipsy-template.md`: read it the same way.) |
| `events/README.md` | Overview of every event: date, event, status, Hipsy id + link, tickets sold, revenue (totals only), event file |
| `events/YYYY-MM-DD-<recipe>.md` | One file per dated event (format below) |
| `emails/<name>.md` | Participant email templates: `welcome`, `reminder`, `thank-you` |
| `place/` | The venue: address, route, facilities, house rules, prices (when they have one) |

Files are written in the owner's working language; section headings may be in that language too
(match them by meaning). Folder and file names stay as listed here.

**Never in the folder:** participants' names, emails or other personal data, passwords, API keys,
exports of orders. Totals only.

## Event statuses

`draft` (being prepared) · `approved` (owner said yes) · `listed` (on Hipsy as concept, hidden) ·
`live` (visible, owner switched concept off) · `done` (after the date).

## Recipe (`offer/<recipe>.md`)

Everything that stays the same each time this event runs. Sections, in this order:

- Title line `# Recipe: <name>`
- `## Format`: level, programme with times, `Language:` of the event (what participants read),
  capacity, facilitators
- `## Tickets`: table `Ticket | Price | Quantity | Notes`
- `## Image`: the Canva design to copy for a new date (link or name)
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
- Status: draft | approved | listed | live | done
- Date and times:
- Hipsy: <event id> · <link>
- Image: <Canva design link> · <exported 1920 × 1080 file>
```

Then open points (**TODO** lines), `## Listing` (the final public text as it goes on Hipsy),
`## Moved to the welcome email` (lines taken out of the public text for Hipsy's policy, for the
owner to review), `## Tickets` (as set on Hipsy), `## Promotion` (the posts as approved),
`## Sales` (totals only), `## Learned`.

## Hipsy defaults (`offer/hipsy-defaults.md`)

Hipsy's fields and pages are the same for every organiser: they live in the plugin
(`hipsy-template.md`). This file holds only the business's values for the fields marked
*default* there, grouped like the template (Bewerken, Tickets, Instellingen), plus their ticket
patterns per past event and any **TODO** questions.

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

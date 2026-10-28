---
name: new-event
description: The owner wants to plan or prepare an event ("Frisky Friday on 14 November", "a retreat in spring", "zet de academy van maart klaar"). Walks them through it one question at a time and prepares everything for their yes: listing, tickets, welcome text, image and posts.
---

Work by the `guide` skill: one question at a time, nothing goes out without their yes, no tech words.

# New event

Read `${CLAUDE_PLUGIN_ROOT}/reference/business-folder.md`, `${CLAUDE_PLUGIN_ROOT}/reference/hipsy.md`,
`${CLAUDE_PLUGIN_ROOT}/reference/hipsy-template.md` (every Hipsy field and its source, the same for
everyone) and the owner's `offer/hipsy-defaults.md` (their values; if it's missing and they already
use Hipsy, run `hipsy-scan` first).

**Pre-fill everything** from the recipe, their Hipsy defaults and the last event of the same type.
Ask only what's left, one question per message, in this order:

1. **Which event?** From the recipes. A new type gets a recipe first, built with them.
2. **Which date?** Offer free weekends from their planning. If someone co-decides dates
   (`about/owner.md`), ask whether they agreed.
3. **Anything different this time?** Facilitator, times, theme, overnight option.
4. **Tickets:** show last time's set and prices as a table: "same as last time?" Ask only what
   changes. Couples as combi tickets on the singles' limits.
5. **Image:** the recipe's Canva design (see Image below); which one?
6. **Preview:** in one message, exactly as it will appear: the public listing (in the order of
   `offer/listing-template.md` or the default), the tickets, the welcome text, the posts.

Create `events/YYYY-MM-DD-<recipe>.md` (status `draft`) after step 2 and fill it as you go. On their
yes: status `approved`, add the row to `events/README.md`, and offer to put it on Hipsy
(`publish`).

**Hipsy's policy** (checklist in `${CLAUDE_PLUGIN_ROOT}/reference/hipsy.md`; `publish` checks it
again as a gate): when their own text crosses it (sexuality, play parties, nudity, substances),
propose a softened public line, move the original to the welcome text
(`settings/communication`, only buyers see it), list both under `## Moved to the welcome email`
in the event file, and mark it **TODO** for their review. Never soften silently.

**Image (Canva):** if the Canva connector is connected, copy or autofill the recipe's design with
the new date, export PNG 1920 × 1080, put it next to the event, and use the same image for the
cover and the posts. Without Canva: ask them to export it and drop it in their folder. Check every
image against the policy (no nudity) before it goes anywhere.

Never send a list of questions. Missing information stays **TODO** and is asked, never guessed.

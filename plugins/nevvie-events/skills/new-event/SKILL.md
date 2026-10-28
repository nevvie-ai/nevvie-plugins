---
name: new-event
description: The owner wants to plan or prepare an event ("Frisky Friday on 14 November", "a retreat in spring", "zet de academy van maart klaar"). Turns a recipe and a date into a complete event, ready for their yes: listing text, tickets, poster, promotion posts and participant emails.
---

Work by the `guide` skill: one question at a time, nothing goes out without their yes, no tech words.

# New event

Read `${CLAUDE_PLUGIN_ROOT}/reference/business-folder.md` for where things live and the file
formats, and `${CLAUDE_PLUGIN_ROOT}/reference/hipsy.md` for what Hipsy allows.

1. **Recipe.** Find it in `offer/`. No recipe yet: build one with them from what they already have
   (documents, their Hipsy listings), one question at a time. That's the slow part, done once.
2. **Date.** Check it against their calendar (if connected) and `events/`. If `about/owner.md`
   says someone else co-decides dates, ask whether they agreed.
3. **Event file.** Create `events/YYYY-MM-DD-<recipe>.md`, status `draft`.
4. **Listing.** Build the Hipsy text from the recipe's listing text, in the order of
   `offer/listing-template.md` (or the default structure), with this date's details. Their words,
   not new marketing language. Check it against Hipsy's policy; flag anything that crosses it.
5. **Tickets.** From the recipe and `offer/tickets.md`: types, prices, quantities, sale windows;
   couples as combi tickets.
6. **Poster.** If Canva is connected: their template for this event type, filled for this date.
   Otherwise name which existing image to use.
7. **Promotion.** One text per channel in the recipe (newsletter, Instagram, Facebook, FetLife…),
   in `about/voice.md`, each with a placeholder for the Hipsy link.
8. **Show everything in one message**, exactly as it will appear. On yes: status `approved`, save,
   and offer to put it on Hipsy (the `publish` skill).

Anything missing stays **TODO** in the event file and is asked, never guessed.

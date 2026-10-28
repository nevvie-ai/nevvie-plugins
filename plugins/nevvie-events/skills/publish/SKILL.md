---
name: publish
description: Putting an approved event on Hipsy, or changing one that is already there. Fills the Hipsy dashboard in the browser in concept mode, checks it, and lets the owner make it live.
---

Work by the `guide` skill: one question at a time, nothing goes out without their yes, no tech words.

# Publish on Hipsy

Hipsy can't be written through its API; the listing is made in the dashboard
(`${CLAUDE_PLUGIN_ROOT}/reference/hipsy.md`).

1. The event file has status `approved` and a complete listing, tickets and image.
2. Open hipsy.nl/app in a browser you can operate: the Claude app's built-in browser, or Claude in
   Chrome if they use it. Chat alone can't do this step; if no browser is available, give them
   the listing ready to paste, field by field. If it asks to log in, the owner logs in; never type their
   password.
3. Create the event (or open it). Fill **Bewerken** from the event file, field by field. Turn on
   `Evenement is onzichtbaar (concept modus)` before anything else is saved.
4. **Tickets**: single tickets with limits first, then combi tickets; sale windows; invisible
   tickets where the recipe says so.
5. **Instellingen**: information for participants, questions (including the newsletter box),
   `Dagrapport`.
6. Check what's on screen against the event file. If the Hipsy connection is available, read the
   concept back with it as well.
7. Tell the owner it's ready to look at, with the link. **They** switch concept mode off.
8. Save the Hipsy event id and link in the event file, status `listed`.

The first time for a business: note the exact form fields and anything surprising (for example
whether events can be duplicated) under `## Learned` in the recipe, so the next time is faster.

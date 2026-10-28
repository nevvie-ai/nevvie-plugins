---
name: publish
description: Putting an approved event on Hipsy, or changing one that is already there. Fills the Hipsy dashboard in the browser as a hidden concept, following the owner's Hipsy template, and lets the owner make it live.
---

Work by the `guide` skill: one question at a time, nothing goes out without their yes, no tech words.

# Publish on Hipsy

Hipsy can't be written through its API; the listing is made in the dashboard. Pages, fields and
browser tips: `${CLAUDE_PLUGIN_ROOT}/reference/hipsy.md`. Field by field, with each value's source:
`${CLAUDE_PLUGIN_ROOT}/reference/hipsy-template.md`. Their values: `offer/hipsy-defaults.md`.

1. The event file has status `approved` and a complete listing, tickets, welcome text and image.
2. **Policy check (gate), right before writing anything to Hipsy:** check the title, the public
   text, the cover image and the themes against the policy checklist in
   `${CLAUDE_PLUGIN_ROOT}/reference/hipsy.md`, point by point. Report it to the owner in one short
   message: "passes" or each flag with a proposed fix. **Nothing goes on Hipsy while a flag is
   open**; the owner decides each fix (move to the welcome text, soften, or leave out). Note the
   result and date in the event file.
3. **Browser:** use the one already signed in to Hipsy (try Claude in Chrome first, then the
   built-in browser). Only if neither is, ask the owner to sign in; never type their password.
   Chat alone can't do this step: then give them the listing ready to paste, field by field.
4. **Create page** `hipsy.nl/app/events/create`: every field from the event file and their
   defaults; plain text in *Extra informatie*; cover image upload; **Opslaan als concept**, never
   *Evenement publiceren*. Choose **Tickets** when asked.
5. **Tickets:** singles with their limits first, then combi tickets; invisible tickets and sale
   windows as their defaults say.
6. **Settings tabs:** `settings` (concept mode on, contact email), `settings/tickets`
   (notifications etc. per their defaults), `settings/communication` (the filled-in welcome text,
   including the bring list and anything moved out of the public text), `settings/form-questions`.
7. Check what's on screen against the event file (and via the API if connected), including that
   the public text is still the checked version.
8. Write the Hipsy id and link in the event file and in `events/README.md`, status `listed`.
   Send the owner the link. **They** switch concept mode off; then status `live`.

Anything new about Hipsy's pages goes back into the plugin (tell Nevvie); anything new about this
business's choices goes in `offer/hipsy-defaults.md`, not in the recipes.

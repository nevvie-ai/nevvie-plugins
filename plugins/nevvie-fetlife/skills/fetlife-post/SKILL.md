---
name: fetlife-post
description: "Putting an approved event on FetLife, or the FetLife channel's setup step (\"post it on FetLife\", \"zet het op FetLife\", setup's channel stage for FetLife). Prepares a FetLife-ready text in the owner's voice, checks FetLife's rules, and gives it ready to paste; the owner posts it herself."
---

Work by the `guide` skill: one question at a time, nothing goes out without their yes, no tech words.

# FetLife

Rules and fields: `${CLAUDE_PLUGIN_ROOT}/reference/fetlife.md`. **Claude never operates or reads
FetLife itself**: the owner posts.

## Setup step (once)

1. Do they have a FetLife account for the business, older than three months, that takes part in
   the community? If not, say what FetLife requires; creating it is theirs.
2. Their usual choices, asked one at a time when the first event needs them: which profile or
   group posts it, how they show the address, dress code wording, how they mention tickets.
   Write `offer/fetlife-defaults.md`.
3. First use: map the event form fields from their screen (screenshot or field names) into
   `offer/fetlife-defaults.md`.

## Post an event

1. The event file has status `approved`.
2. **Text:** write the FetLife version with the `voice` skill. FetLife allows more than Hipsy, so
   start from the owner's original recipe text (including what was moved out of the Hipsy
   listing), written as a community event, not a sales pitch.
3. **Rules check (gate):** the seven points in `fetlife.md`, plus: is this event already on
   FetLife (no duplicates)? Verdict "Ready for FetLife" or "Not yet: <n> open points"; ask about
   the first open point only.
4. **Ready:** give the text field by field in the order of their form, each in its own block to
   copy, plus the image to upload. She posts it.
5. She pastes the event link back: write it in the event file's `## FetLife` section
   (status `posted`, rules check date) and in `events/README.md`.

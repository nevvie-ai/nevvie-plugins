---
name: hipsy-scan
description: Learn a business's usual Hipsy choices from their existing events, or refresh the events overview ("scan my Hipsy", "things changed on Hipsy", first setup of a business that already sells on Hipsy). Read only. Writes offer/hipsy-defaults.md and events/README.md.
---

Work by the `guide` skill: one question at a time, nothing goes out without their yes, no tech words.

# Hipsy scan (read only)

Hipsy's fields are the same for everyone (`${CLAUDE_PLUGIN_ROOT}/reference/hipsy-template.md`).
This scan only learns **this business's values**.

1. Use the browser that is already signed in to Hipsy (try Claude in Chrome first, then the
   built-in browser). If neither is, ask the owner to sign in; never type their password.
2. `hipsy.nl/app/events`: every event with status, date, tickets sold, revenue → `events/README.md`
   (one row per event; event file or "made before this folder"; `Last checked: <date>`).
3. Only when `offer/hipsy-defaults.md` is missing or they say things changed: open the most recent
   event of each type (`details`, `tickets`, the settings tabs) and read their values. Change
   nothing; save nothing.
4. **Never** open participant or order details beyond totals; never copy names or emails.
5. Write `offer/hipsy-defaults.md`: for each *default* field of the template, their value; their
   ticket patterns per past event; their settings per tab. Unclear points become **TODO**
   questions.
6. Tell the owner in one or two sentences what you found, then ask the single most useful TODO.

A new business without Hipsy events: skip the scan; `setup` asks the defaults instead.

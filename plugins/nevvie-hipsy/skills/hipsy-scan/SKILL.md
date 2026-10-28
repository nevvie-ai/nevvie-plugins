---
name: hipsy-scan
description: "The Hipsy channel's setup step, and a refresh of what's on Hipsy (\"scan my Hipsy\", \"things changed on Hipsy\", setup's channel stage for Hipsy). Checks account and sign-in, then reads their existing events and usual choices. Read only. Writes offer/hipsy-defaults.md and events/README.md."
---

Work by the `guide` skill: one question at a time, nothing goes out without their yes, no tech words.

# Hipsy scan (read only)

Hipsy's fields are the same for everyone (`${CLAUDE_PLUGIN_ROOT}/reference/hipsy-template.md`).
This scan only learns **this business's values**.

0. **Account:** no Hipsy organiser account yet? Creating it is theirs (hipsy.nl, sign up as
   organiser); guide them, never fill it in. No events yet: skip to step 5 and ask the *default*
   fields of the template one at a time when the first event needs them.
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

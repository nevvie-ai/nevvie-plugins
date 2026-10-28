---
name: check-setup
description: "Something doesn't work or the owner feels stuck (\"het werkt niet\", \"I can't find it\", \"Claude can't see my files\", \"Hipsy won't open\", a skill or style seems missing). Tests every piece of their setup, finds the first broken one, and gives the one next step for their computer."
---

Work by the `guide` skill: one question at a time, nothing goes out without their yes, no tech words.

# Check setup

Check in this order and stop at the **first** thing that fails (instructions per computer:
`${CLAUDE_PLUGIN_ROOT}/reference/devices.md`):

1. **Local session?** A cloud session can't reach their folder or this plugin's full setup.
2. **Right folder?** The session is inside their business folder (has `CLAUDE.md`), inside Google
   Drive, and the files are available offline.
3. **Plugin up to date?** Its skills are present (you are running one). If they mention something
   new that you don't have: quit the app completely, reopen, new session.
4. **Languages set?** `Language:` and `Event language:` at the top of `CLAUDE.md`.
5. **Channels?** Each channel in `about/brand.md` has its plugin enabled; for channels Claude
   operates in the browser (Hipsy), a browser is available and signed in (`hipsy.nl/app/events`
   shows their events, not a login page).
6. **Connections?** Canva / Gmail / Google Drive tools present when the task needs them.
7. **Saving works?** Write a small change to a file and read it back.

Then tell them in one or two sentences what's wrong and the **one** next step for their system,
and wait for "done". Tick the matching line in `CLAUDE.md` → `## Setup` once it works.

If everything passes and it still doesn't work: describe exactly what you see in one message
they can forward to Nevvie (nevvieconsulting@gmail.com), with no personal data of participants.

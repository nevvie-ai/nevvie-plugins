---
name: setup
description: First time with a new business, or the folder is still mostly empty. Interviews the owner one question at a time and fills the business folder from what they say and what they already have.
---

Work by the `guide` skill: one question at a time, nothing goes out without their yes, no tech words.

# Setup

The goal is a filled business folder (`${CLAUDE_PLUGIN_ROOT}/reference/business-folder.md`)
without the owner ever seeing it.

0. **Language first:** if `CLAUDE.md` has no `Language:` line, ask it as the `guide` skill says,
   before anything else.
1. **Empty or new folder:** create the skeleton from
   `${CLAUDE_PLUGIN_ROOT}/reference/business-folder.md` right here: `CLAUDE.md`, `about/`,
   `offer/`, `events/`, `emails/`, `place/` (only if they have a venue), and
   `.claude/settings.json` with `{"outputStyle": "nevvie-events:Guide", "permissions": {"allow":
   ["Read", "Edit", "Write"]}}`. Write everything in their language. Tell them in one sentence that their folder is ready.
2. Read what exists: the folder, their Hipsy listings (if reachable), documents they point to.
3. Interview, one question per message, in this order; skip whatever you can already answer:
   what they run and for whom; who decides what; their event types; for each type, the latest
   listing text; ticket rules; their place if they have one; how they write (ask for two messages
   or listings they like).
4. After each answer, write it into the right file. Mark gaps **TODO**.
5. End with one sentence on what is now ready, and offer to plan their first event together.

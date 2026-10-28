---
name: voice
description: "Write anything the owner's participants, guests or followers will read (Hipsy listing, welcome text, email, social post, newsletter, website text) in the owner's own voice, and learn from every reaction they give to a draft. Load before writing any of those, and whenever the owner approves, cuts or rewrites a draft. Also builds the voice profile during setup."
---

Work by the `guide` skill. This skill is about how **they** write; `guide` is about how you talk
with them.

Their voice lives in their folder (`${CLAUDE_PLUGIN_ROOT}/reference/business-folder.md`):
`about/voice.md` (the profile), `about/voice-samples/` (their own texts), `about/voice-edits.md`
(what they changed in drafts, and why).

## Build (during setup, or when `about/voice-samples/` is empty)

1. Collect 5–10 texts they wrote themselves, chosen for **variety** (listing, email, post, a
   personal message), never all on one topic: their Hipsy listings (read in the signed-in
   browser), their website, and two or three messages or emails they like (ask for them). Save
   each verbatim in `about/voice-samples/<format>-<short-name>.md` with a first line
   `format: <listing|email|post|message|web> · status: approved · source: <where>`.
2. Write `about/voice.md` from the samples only, each line backed by a short quote:
   language and dialect; je/jij/u; how they open and close; sentence length and rhythm; lists or
   prose; emoji and punctuation habits; words and images they return to; values said as
   invitations or as rules; what they never write. Mark guesses as guesses.
3. Tell them in one sentence what you noticed, and ask whether it sounds like them.

## Write

1. Read `about/voice.md`. Read 2–5 approved samples of the **same format**, chosen for variety,
   not for the same topic (picking by topic makes a draft copy content instead of voice), plus any
   `status: rejected` drafts as what not to write.
2. Start from their own words wherever they exist (the recipe's listing text, last year's
   email); adapt, don't rewrite. Take away rather than add.
3. **Before they see it, check:**
   - **Shape:** no slogan opening or hype ending, no "not X, but Y" flourishes, no groups of
     three for rhythm, no summary line repeating what was said, length like their samples.
   - **Words:** no word they never use. Typical AI words to replace with theirs: "dive into",
     "unlock", "journey", "transformative", "unique", "elevate", "embrace", "seamless",
     "vibrant", "curated"; in Dutch "duik in", "ontdek de kracht van", "transformerend",
     "uniek", "naadloos". Replace with a word from their samples, never with a new one of yours.
   - **Language and form:** their language and dialect, their je/u, their emoji habits.
4. Show it. Never mention this check to them.

## Learn (every time they react)

- **They change or cut something:** add the before and after to `about/voice-edits.md`, with
  their reason if they gave one, dated, format noted.
- **A pattern shows up twice** (same kind of change): revise the matching line in
  `about/voice.md`, or add one, quoting their words. Revise, don't append; delete what turned out
  wrong.
- **They approve a text as is:** save it in `about/voice-samples/` as `status: approved`. A draft
  they rejected outright: save as `status: rejected` with one line why.
- Most sessions add nothing. Silence beats padding.

The test: a first draft lands without a "make it more like me" round. When it doesn't, fix the
profile, not just the draft.

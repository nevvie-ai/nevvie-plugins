# Channels (the agreement every channel plugin follows)

The base plugin (`nevvie-events`) prepares the event once. **Channel plugins** put it somewhere:
`nevvie-hipsy` (tickets on Hipsy), `nevvie-fetlife` (the event on FetLife), later social posts or a
newsletter. A business enables the channels it uses; `about/brand.md` lists them under
`Channels:`.

Every channel plugin provides:

1. **A rules check** for that platform, run as a gate right before anything goes on it. Verdict:
   "Ready for <channel>" or "Not yet: <n> open points". Nothing goes out while a point is open.
2. **A defaults file** in the business folder: `offer/<channel>-defaults.md` (their usual choices on
   that platform).
3. **A section in the event file:** `## <Channel>` with the text as it goes on that platform, the
   link or id, its status (`draft`, `ready`, `listed`/`posted`, `live`) and the date of the rules
   check.
4. **A publish skill** for that platform, and a setup step (account, sign-in, defaults) that the
   base `setup` calls in its channel stage.

What differs per platform stays in the channel plugin: its fields, its rules, how much may be said
in public, and whether Claude may operate it in the browser or only prepares the text for the owner
to paste.

The same event can need a different public text per channel (Hipsy allows far less than FetLife).
`new-event` writes one public text per enabled channel, each in the owner's voice, each checked by
its own channel.

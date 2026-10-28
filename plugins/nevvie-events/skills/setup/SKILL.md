---
name: setup
description: "First time with a business, the folder is new or mostly empty, the owner says \"set me up\" / \"help me start\", or CLAUDE.md shows an unfinished Setup list. Takes them from zero to a working business folder, one step at a time, adapted to their computer, so they never need outside help."
---

Work by the `guide` skill: one question at a time, nothing goes out without their yes, no tech words.

# Setup

Goal: a working business folder (`${CLAUDE_PLUGIN_ROOT}/reference/business-folder.md`) and
everything around it, without the owner getting stuck. Instructions per computer:
`${CLAUDE_PLUGIN_ROOT}/reference/devices.md`.

**Progress is saved.** `CLAUDE.md` has a `## Setup` checklist (below). Tick each stage when it
works and continue from the first open one in any later session. Never redo a ticked stage
unless they ask. An existing folder without the list (set up before this version): add the list,
tick every stage the folder already covers, and continue with the first open one.

## Stage 0: check where you are (silently)

Detect system, folder, cloud vs local, browser and connectors as `devices.md` says.
- **Cloud session:** tell them, in one short message in Dutch and English, that this has to run
  on their own computer, with the steps to start a local session. Stop.
- **No business folder yet** (no `CLAUDE.md`, and not inside Google Drive): continue with Stage 1,
  then Stage 2 moves them into Drive.

## Stage 1: languages

1. **Working language** (how you talk with them and write their folder), asked in both
   languages: "In welke taal wil je werken: Nederlands of English? / Which language would you like
   to work in?" → `Language: <answer>`.
2. **Event language** (what their participants read; recipes can override per event): "In welke
   taal schrijf je meestal voor je deelnemers?" → `Event language: <answer>`.

## Stage 2: their folder in Google Drive

If the session isn't already inside Google Drive: teach Google Drive for desktop for **their
system** (devices.md), one step per message, waiting for "done" each time; then: make the folder
**My Drive → Claude → <business name>**, make it available offline, and start a new local session
on it. Stop this session there; the next one continues here.

When inside the folder: create the skeleton (`CLAUDE.md` with the top lines and the Setup list,
`about/`, `offer/`, `events/`, `emails/`, `place/` only if they have a venue,
`.claude/settings.json` as below, so the plugins travel with the folder to any computer: Claude
offers to install them when the folder is opened there).

```json
{
  "extraKnownMarketplaces": {
    "nevvie-plugins": { "source": { "source": "github", "repo": "nevvie-ai/nevvie-plugins" } }
  },
  "enabledPlugins": {
    "nevvie-events@nevvie-plugins": true,
    "nevvie-hipsy@nevvie-plugins": true,
    "nevvie-fetlife@nevvie-plugins": true
  },
  "outputStyle": "nevvie-events:Guide",
  "permissions": { "allow": ["Read", "Edit", "Write"] }
}
```

Enable only the channels they use (Stage 4 adds or removes them). In an existing folder, merge
these keys into its settings; never drop keys that are already there. Write the two language lines and `Device: <Windows|Mac>` at the
top of `CLAUDE.md`.

## Stage 3: the business

Interview, one question per message, skipping what you can already read: what they run and for
whom; who decides what (dates, prices, tickets); their event types; for each type the latest
listing text; ticket rules; their venue if they have one. Write each answer into the right file;
gaps are **TODO**.

## Stage 4: channels

Ask where they publish events (Hipsy, FetLife, …) and write `Channels:` in `about/brand.md`. For
each channel: check its plugin is enabled (its skills are present; if not, tell them which plugin
to add, with the steps from devices.md), then run that channel's setup step (account is theirs;
sign-in; defaults). See `${CLAUDE_PLUGIN_ROOT}/reference/channels.md`.

## Stage 5: their voice

Run the `voice` skill's Build step: their own texts first (their public event listings, website, two or three
messages they like), then the profile.

## Stage 6: connections

Offer, one at a time, with the steps from devices.md: **Canva** (posters for new dates),
**Gmail** (email drafts). Skipping is fine; note it.

## Stage 7: first event

Offer to plan their first event together (`new-event`). Setup is done when it is `approved`.

## The Setup list in `CLAUDE.md`

```
## Setup
- [ ] Languages
- [ ] Folder in Google Drive (available offline)
- [ ] Business basics
- [ ] Channels (Hipsy / FetLife: plugin, account, sign-in, defaults)
- [ ] Voice
- [ ] Connections (Canva, Gmail)
- [ ] First event
```

When something fails at any stage, run `check-setup` before asking them anything.

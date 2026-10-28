# Devices and setup steps (Windows and Mac)

Used by `setup` and `check-setup` to teach the owner, in their working language, one step per
message. Detect the system yourself; never ask which computer they have.

## Detect (silently)

- **System:** your environment tells you the platform (win32 / darwin / linux). If unsure, run
  `uname -s` (Mac: `Darwin`) or check `$OS` / `ver` (Windows).
- **Folder:** the current working directory. Inside Google Drive when the path contains
  `My Drive` / `Mijn Drive` (Windows, usually under a drive letter like `G:`) or
  `Library/CloudStorage/GoogleDrive-` (Mac). Business folder = it has `CLAUDE.md`.
- **Cloud session:** a path like `/home/…` or `/root/…` on a Linux machine that isn't theirs means a
  cloud session: their folder and the plugin aren't there. Tell them to start a **local** session
  (below) and stop.
- **Browser:** Claude in Chrome is available when its browser tools are present in this session;
  the app's built-in browser when its tools are present. Signed in to Hipsy: open
  `hipsy.nl/app/events`; a login page means not signed in.
- **Connectors:** Google Drive, Gmail, Canva are connected when their tools are present.

## Start a local session on their folder

Claude desktop app → **Code** → new session → choose **Local** (not cloud) → pick the folder
(Google Drive → My Drive → `Claude` → their business folder) → accept the trust question.

## Google Drive for desktop

**Windows**
1. Download "Google Drive for desktop" from google.com/drive/download and install it.
2. Sign in with the Google account that holds their business files.
3. In File Explorer, **Google Drive (G:)** appears (the letter can differ) → **My Drive**.
4. Right-click the business folder → **Offline access** → **Available offline**. A green tick
   shows when it's done.

**Mac**
1. Download "Google Drive for desktop" from google.com/drive/download, open the installer, allow it
   in System Settings if macOS asks.
2. Sign in with the Google account that holds their business files.
3. In Finder, **Google Drive** appears in the sidebar under Locations → **My Drive**.
4. Right-click (Control-click) the business folder → **Offline access** / **Available offline**.

If the folder isn't there: Drive for desktop is signed in with a different Google account
(Drive for desktop → settings → account).

## Claude in Chrome (for Hipsy)

1. In Google Chrome, open the Chrome Web Store and search "Claude" (by Anthropic), **Add to
   Chrome**.
2. Pin it, open it, sign in with the **same Claude account** as the desktop app.
3. In that Chrome, sign in to Hipsy once (hipsy.nl). Claude never types their password.

Without Chrome: the app's built-in browser works too; they sign in to Hipsy there once.

## Connectors (Canva, Gmail, Google Drive)

In the Claude app: **Settings → Connectors** (or Customize → Connectors) → find **Canva** /
**Gmail** / **Google Drive** → **Connect** → sign in on the page that opens. Then start a new
session.

## The plugin itself

- Installed through the app: **Customize → Plugins → Add marketplace** `nevvie-ai/nevvie-plugins`
  → install **Event Assistant for Hipsy organisers**.
- Updates arrive on their own when a session starts. If something new doesn't show up: **quit the
  Claude app completely** (Windows: also from the tray; Mac: Cmd+Q), open it again, start a new
  session.

## When they're stuck

Run `check-setup`: it tests each piece above and gives the one next step for their system.

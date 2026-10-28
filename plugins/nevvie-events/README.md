# Event Assistant for Hipsy organisers (`nevvie-events`)

Plan, list and sell events on Hipsy by talking to Claude.

- **Guide** (a skill, and an output style for the Code tab): one question at a time, nothing goes out without a yes, no tech words. Cowork and chat ignore output styles, so the skill carries it everywhere.
- Skills: `guide`, `voice`, `setup`, `check-setup`, `hipsy-scan`, `new-event`, `publish`, `this-week`, `follow-up`, `learn`.
- Reference: setup steps per computer (Windows, Mac), the business-folder contract, the Hipsy template (every field, same for all organisers), and what Hipsy allows (API, dashboard, policy checklist).
- Install: `/plugin install nevvie-events --marketplace nevvie-ai/nevvie-plugins` (or open a business folder whose settings enable it).
- The Hipsy connection (read sales and orders) is added with the Nevvie Hipsy server; until then sales are read in the dashboard.

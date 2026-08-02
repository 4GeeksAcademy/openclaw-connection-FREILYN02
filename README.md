# Connect Your Agent: Telegram, Google Drive & Calendar

Configuration project connecting an OpenClaw agent ("Zyro") to Telegram
for messaging and to Google Drive and Google Calendar through the
Zapier MCP.

## Setup Overview

1. **OpenClaw** — Running instance on a VPS (Ubuntu 22.04), agent "Zyro"
   configured with identity, able to receive messages and invoke tools.
2. **Telegram** — Bot created with BotFather (@Zyro_freilyn_bot),
   connected via `openclaw channels add --channel telegram --token <token>`.
   Token stored only in OpenClaw's secure config, never in this repo.
3. **Zapier MCP** — Enabled in Zapier, connected to OpenClaw via OAuth
   using `mcporter`. 15 tools available.
4. **Google (via Zapier)** — Google Drive and Google Calendar enabled
   as apps on the Zapier MCP server, authorized with a test Google
   account.

## Reference Workflow

1. User sends a Telegram message asking the agent to create a document.
2. Agent creates the document in Google Drive via Zapier.
3. Agent creates a calendar event to review that document.
4. Agent confirms completion on Telegram.

## Evidence

See `/screenshots` for:
- OpenClaw channels list showing Telegram connected
- Zapier MCP server showing Google Drive and Google Calendar connected
- Full Telegram thread (request → confirmation)
- New Google Drive document
- New Google Calendar event

See `notes.md` for configuration notes and issues encountered.
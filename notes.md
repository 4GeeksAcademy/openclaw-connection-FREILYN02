# Notes - Connect Your Agent: Telegram, Google Drive & Calendar

- Telegram bot created with BotFather (@Zyro_freilyn_bot) and connected
  using `openclaw channels add --channel telegram --token <token>`.
- Pairing was required (`openclaw pairing approve telegram <code>`)
  before the bot would respond; this also auto-configured the user's
  Telegram as command owner.
- Zapier MCP was connected to OpenClaw via OAuth using mcporter,
  following the setup prompt Zapier generates when choosing "OpenClaw"
  as the agent. Google Drive and Google Calendar apps were enabled
  within the MCP server.
- Each Google app (Drive and Calendar) required a separate OAuth
  authorization from the browser.
- A test Google account connected in Zapier was used for Drive/Calendar
  actions, avoiding sensitive personal data.
- End-to-end flow tested via Telegram: requested creating a Drive
  document and scheduling a calendar event to review it; the agent
  executed both actions through Zapier MCP and confirmed via Telegram.


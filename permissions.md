# Permissions

Logger requires specific permissions to function correctly and log events in your Discord server. This page explains each permission, why it is needed, and how to troubleshoot common issues.

## Required Bot Permissions

### `View Channels`
Allows Logger to see all channels in your server. Without this, the bot cannot read events or send logs to channels.

### `Send Messages`
Lets Logger send messages in log channels. This is required for the bot to deliver log notifications and status updates.

### `Embed Links`
Enables Logger to send rich embed messages, which are used for all log entries. Without this, logs will not display correctly.

### `Manage Webhooks`
Allows Logger to create, edit, and delete webhooks in your channels. Webhooks are used to send logs with custom avatars and names for better clarity.

---

## Why Are These Permissions Needed?

- **View Channels:** Logger must be able to see the channels you want to log events from or send logs to.
- **Send Messages:** Logger posts log entries and status messages in your chosen channels.
- **Embed Links:** All logs are sent as embeds for better formatting and readability.
- **Manage Webhooks:** Logger uses webhooks to send logs with custom formatting and to avoid hitting message rate limits.

---

## Best Practices

- Grant permissions at the channel level for more control (e.g., only allow Logger in log channels).
- Avoid giving Logger Administrator unless absolutely necessary.
- Double-check channel-specific overrides if logs are missing from certain channels.

---

## Troubleshooting

- If logs are missing, check that Logger has all required permissions in both the server and the specific log channels.
- Make sure no channel overrides are blocking Logger from sending messages or embeds.
- If webhooks are not working, ensure Logger has `Manage Webhooks` in the target channel.
- For persistent issues, try removing and re-adding the bot, or contact support.

---

For more help, see the [Troubleshooting](troubleshooting.md) page or join the support server.
# Troubleshooting

This page covers common issues with Logger and how to resolve them. If you still need help, contact support or check the rest of the documentation.

## Bot Not Logging

- **Check Bot Permissions:** Logger needs `View Channels`, `Send Messages`, `Embed Links`, and `Manage Webhooks` in every log channel. See [Permissions](permissions.md).
- **Check Webhook Permissions:** Logger must have `Manage Webhooks` in the log channel. If missing, logging will fail.
- **Bot Offline:** Make sure Logger is online in your server. If not, try reinviting the bot or check the [status page](https://loggerapp.xyz/status).
- **Channel Overrides:** Channel-specific permission overrides can block Logger from sending messages or embeds. Double-check channel settings.
- **Role Hierarchy:** Logger’s role must be above the roles it needs to log (for actions like role changes).

## Duplicate Logs

- **Multiple Webhooks:** If you see duplicate logs, check for multiple Logger webhooks in the same channel. Remove extras if needed.
- **Multiple Bots:** Make sure you don’t have more than one logging bot enabled for the same events.

## Webhook Issues

- **Webhook Not Created:** Logger needs `Manage Webhooks` to create webhooks. If missing, grant the permission and try again.
- **Webhook Deleted:** If a webhook is deleted manually, Logger will recreate it the next time it needs to log an event.

## Event Not Logging

- **Event Not Enabled:** Use `/setup` to enable logging for the event or preset you want.
- **Suppressed Channel/User:** Check if the channel or user is suppressed with `/suppress`.

## Still Need Help?

- [Support Server](https://loggerapp.xyz/support)
- [Documentation](https://loggerapp.xyz/docs)
# Webhooks

Logger uses Discord webhooks to deliver log messages to your channels. Webhooks allow Logger to avoid message rate limits. Logger manages all webhooks automatically—no manual setup is required.

## Why Does Logger Use Webhooks?

- **Bypass Rate Limits:** Webhooks have separate rate limits from normal bot messages, so Logger can deliver logs quickly even during busy events.
- **Channel Flexibility:** Logger can create a webhook in any channel you choose for logging, without needing to send messages as the bot user.
- **Security:** Logger only creates and uses webhooks it needs. Unused webhooks are deleted automatically.

## How Logger Manages Webhooks

- Logger creates a webhook in each channel you select for logging.
- If you stop logging in a channel, Logger will delete the webhook if it is no longer needed.
- You do not need to create, edit, or delete webhooks yourself—Logger handles everything.

## Permissions Required

- Logger needs the `Manage Webhooks` permission in any channel you want to use for logging.
- Without this permission, Logger cannot create or remove webhooks, and logging will not work.

## Security Considerations

- Logger never exposes webhook URLs to users.
- Webhooks are only used for sending log messages—no sensitive data is shared.
- If you remove Logger from your server, all webhooks it created will stop working.

---

If you have questions or issues with webhooks, check the [Permissions](permissions.md) page or contact [support](https://loggerapp.xyz/support).
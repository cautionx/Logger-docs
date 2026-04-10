## `/stop`

The `/stop` command disables logging for specific events or groups of events (presets) in your server. It also cleans up unused webhooks when possible.

### Subcommands

#### `/stop individual_event`
Turn off logging for a single event type.

**Options:**
- `event` (required): The event to stop logging (e.g., Message Delete, Channel Create, etc.)

**How it works:**
1. Select the event you want to stop logging.
2. Logger will remove the configuration for that event and, if no other events use the webhook, delete the webhook.
3. You’ll get a confirmation message.

#### `/stop preset`
Turn off logging for a group of related events (preset).

**Presets include:**
- Message (bulk, delete, edit)
- Role (create, update, delete)
- Member (join, update, leave, kick)
- Emoji (create, update, delete)
- Channel (create, update, delete)
- Moderation (ban, unban)
- Invite (creation, deletion)
- All (everything shown)

**Options:**
- `preset` (required): The group of events to stop logging.

**How it works:**
1. Select a preset.
2. Logger will remove the configuration for all events in the preset and, if no other events use the webhook, delete the webhook.
3. You’ll get a confirmation message listing the removed events.

---

### Example Usage

- `/stop individual_event event:message_delete`
- `/stop preset preset:message`

---

### Permissions Required
- You must have the `Manage Server` permission to use `/stop`.

---

### Troubleshooting
- If you see a warning about no logging setup found, make sure you have configured logging with `/setup` first.
- If you want to check which events are currently enabled, use `/setup list`.
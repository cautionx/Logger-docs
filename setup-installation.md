## `/setup`

The `/setup` command helps you configure logging channels for specific events or groups of events (presets) in your Discord server.

### Subcommands

#### `/setup via_individual_event`
Enable logging for a single event type in a specific channel.

**Options:**
- `event` (required): The event to log (e.g., Message Delete, Channel Create, Member Join, etc.)
- `destination` (required): The text channel where logs for this event will be sent.

**How it works:**
1. Select the event you want to log.
2. Choose the destination channel.
3. Logger will create or use a webhook in that channel and start logging the selected event.
4. If the event is already enabled, you’ll get a warning and instructions to disable it with `/stop individual_event`.

#### `/setup via_preset`
Enable logging for a group of related events (preset) in a specific channel.

**Presets include:**
- Message (bulk, delete, edit)
- Role (create, update, delete)
- Member (join, update, leave/kick)
- Emoji (create, update, delete)
- Channel (create, update, delete)
- Moderation (ban, unban)
- Invite (creation, deletion)
- All (every event Logger supports)

**Options:**
- `preset` (required): The group of events to log.
- `destination` (required): The text channel where logs for these events will be sent.

**How it works:**
1. Select a preset.
2. Choose the destination channel.
3. Logger will create or use a webhook in that channel and start logging all events in the preset.
4. If any events in the preset are already enabled, you’ll get a warning and instructions to disable them with `/stop preset`.

#### `/setup list`
Lists all currently configured log channels and which events are enabled in each.

**How it works:**
1. Run `/setup list`.
2. Logger will show a summary of all events and their assigned channels, including which are enabled or disabled.

---

### Permissions Required
- You must have the `Manage Server` permission to use `/setup`.
- Logger needs `Manage Webhooks` and `View Channel` permissions in the destination channel.

### Troubleshooting
- If setup fails, check that Logger has the required permissions in the selected channel.
- If you see a warning about an event already being enabled, use `/stop` to disable it before reassigning.

---

For more details on event types, see [Event Types](events.md). For permissions, see [Permissions](permissions.md).


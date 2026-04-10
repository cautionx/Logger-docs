## `/suppress`

The `/suppress` command allows you to exclude (ignore) logs for specific channels or users for certain event types. This is useful if you want to prevent Logger from logging activity in certain channels or from certain users.

### Subcommands

#### `/suppress channel`
Exclude logs for a specific channel and event type.

**Options:**
- `action` (required):
	- `Add`: Start ignoring logs for the selected channel and event type.
	- `Remove`: Stop ignoring logs for the selected channel and event type.
	- `List`: Show all currently ignored channels for the selected event type.
- `type` (required): The event type to suppress (e.g., Message Delete, Channel Create, etc.).
- `target` (optional): The channel to modify (required for Add/Remove).

**How it works:**
1. Choose the event type and channel.
2. Select Add or Remove to update the ignore list, or List to view ignored channels.
3. Logger will update its configuration and confirm the change.

#### `/suppress user`
Exclude logs for a specific user and event type.

**Options:**
- `action` (required):
	- `Add`: Start ignoring logs for the selected user and event type.
	- `Remove`: Stop ignoring logs for the selected user and event type.
	- `List`: Show all currently ignored users for the selected event type.
- `type` (required): The event type to suppress.
- `target` (optional): The user to modify (required for Add/Remove).

**How it works:**
1. Choose the event type and user.
2. Select Add or Remove to update the ignore list, or List to view ignored users.
3. Logger will update its configuration and confirm the change.

---

### Example Usage

- `/suppress channel action:add type:message_delete target:#off-topic`
- `/suppress user action:add type:message_delete target:@Spammer`
- `/suppress channel action:list type:message_delete`

---

### Permissions Required
- You must have the `Manage Server` permission to use `/suppress`.

---

Suppressed channels and users will not have their actions logged for the selected event types until removed from the ignore list.
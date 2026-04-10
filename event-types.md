# Event Types

Logger can track a wide range of server events. You can enable or disable each event individually or as part of a preset using the `/setup` command.

---


## Individual Event Types

- **Bot Add:** When a bot joins the server
- **Channel Create:** When a channel is created
- **Channel Delete:** When a channel is deleted
- **Channel Update:** When a channel is updated (name, topic, etc)
- **Emoji Create:** When a custom emoji is created
- **Emoji Delete:** When a custom emoji is deleted
- **Emoji Update:** When a custom emoji is updated
- **Guild Member Add:** When a member joins the server
- **Guild Member Leave/Kick:** When a member leaves or is kicked
- **Guild Member Update:** When a member’s roles or nickname changes
- **Guild Ban Add:** When a member is banned
- **Guild Ban Remove:** When a ban is removed
- **Guild Update:** When server settings are updated
- **Invite Create:** When an invite is created
- **Invite Delete:** When an invite is deleted
- **Message Bulk Delete:** When multiple messages are deleted at once
- **Message Delete:** When a message is deleted
- **Message Update:** When a message is edited
- **Role Create:** When a role is created
- **Role Delete:** When a role is deleted
- **Role Update:** When a role is updated
- **Voice State Change:** When a user joins/leaves/mutes in voice

---

## Presets (Quick Groups)

Presets are groups of related events for fast setup:

- **Message:** message_delete, message_update, message_bulk_delete
- **Role:** role_create, role_delete, role_update
- **Member:** member_join, member_leave, member_update, bot_join
- **Emoji:** emoji_create, emoji_delete, emoji_update
- **Channel:** channel_create, channel_delete, channel_update
- **Moderation:** guild_ban_add, guild_ban_remove
- **Invite:** invite_create, invite_delete
- **All:** every event Logger supports

---

## How to Enable/Disable Events

1. Use `/setup via_individual_event` to enable or disable a single event.
2. Use `/setup via_preset` to enable or disable groups of related events.
3. Use `/stop` to turn off logging for specific events or presets.

For more details on configuring events, see the [Setup](setup.md) page.
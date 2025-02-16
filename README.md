# Hexxecutor Documentation

Hexxecutor is a Roblox admin tool that allows authorized users to execute Lua code on the server. It includes features like rank-based permissions, keyword blacklists, and Discord webhook notifications.

---

## Configuration

### Webhook Configs
- **`Webhook`**: Primary Discord webhook URL.
- **`Webhook2`**: Secondary Discord webhook URL.
- **`fallbackWebhook`**: Fallback webhook URL used if primary and secondary fail.
- **`useWebhook2`**: If `true`, both primary and secondary webhooks are used.
- **`useWebhook2First`**: If `true`, the secondary webhook is used first.

### Debug and Logging
- **`debugMode`**: Enables debug prints in the console.
- **`doServerLog`**: Logs admin actions in the console and sends them to the webhook.
- **`sendDocumentationToWebhook`**: Sends documentation to the webhook(s) (studio only).

### Rank System
- **`ranksExperimental`**: Enables the rank system.
- **`keywordBlacklist`**: Enables keyword blacklisting for ranks.
- **`rankList`**: List of available ranks.
- **`Ranks`**: Assigns player UserIds to ranks.
- **`customKeywordBlacklist`**: Enables custom keyword blacklists for each rank.
- **`keywordBlacklist`**: Defines blacklisted keywords for each rank.

---

## Rank Assignments
Ranks are assigned in the `Ranks` table using player UserIds. Example:
```lua
Ranks = {
    Owner = { }, -- UserIds for Owners
    Developer = {  }, -- UserIds for Developers
    Admin = {  }, -- UserIds for Admins
    Moderator = { 5019537481, 2330582728 } -- UserIds for Moderators
}
```

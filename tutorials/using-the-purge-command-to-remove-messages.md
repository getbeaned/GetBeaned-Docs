---
description: >-
  The purge command is a level 2+ (trusted) command to remove messages matching
  one or more criteria.
---

# Using the purge command to remove messages

This command is available in two modes. The **shortcut** mode and the **custom** mode. The shortcut mode allows you to remove certain types of messages easily, while the custom mode lets you choose messages to remove in a much more powerful and specific fashion.

### Shortcut mode

General syntax: `+purge [type of removal] <number of messages to search>`



#### Embeds

Remove message that contains embeds:

![This is an embed that would get removed \(rich embed\)](../.gitbook/assets/2019-06-22.18-54-00.png)

![Link previews are also removed by the embed filter](../.gitbook/assets/2019-06-22.18-56-41.png)

#### Files

Remove messages with attachments linked to them.

#### Images

Remove messages containing images. 

#### All

Remove any message. For example, to remove the last 10 messages, use `+purge all 10`

#### User

Remove messages from a specific user. For example, to remove the last 10 messages of @User, type `+purge user @User 10`

#### Contains

Remove messages containing a substring \(at least 3 chars long\).  For example, to remove every message containing OwO, type `+purge contains OwO`

#### Bot

Remove messages from bots and bot commands. To remove messages from bots only, use `+purge bot` while you can use `+purge bot + 35` to remove messages that either are from bots or start with + in the last 35 messages.

#### Emoji

Delete messages containing custom emojis. 

#### Reactions

Remove reactions from messages that have them. This **does not** remove messages, just reactions.

### Custom mode

Need more power to remove messages. Behold the custom mode!

This command uses a powerful "Command Line" syntax. Most options support multiple values to indicate 'any' match. If a value has spaces, it must, as always, be quoted.   
The messages are by-default deleted only if all options are met \(AND\). You can use the `--or`flag that will delete messages if any of the conditions is met.

The following options are valid. They all take arguments.

| Option | Explanation |
| :--- | :--- |
| `--user` | A mention or a name of the user to |
| `--contains` | A substring to search for in the message |
| `--starts` | A substring that a message must start with |
| `--ends` | A substring that a message must end with |
| `--search` | The number of messages to search for on the channel. Default to 100, max is 2000. |
| `--after` | Messages must come after this message ID |
| `--before` | Messages must come before this message ID |

You can also use the following flags, with no arguments.

| Flag | Explanation |
| :--- | :--- |
| `--bot` | Check if the message author is a bot |
| `--embeds` | Check if the message contains an embed |
| `--files` | Check if the message contains files |
| `--emoji` | Check if the message has custom emojis |
| `--reactions` | Check if the messages has reactions |
| `--or` | Use the logical OR for all options |
| `--and` | Use the logical AND for all options \(Default\) |

Here are some examples to get you started.

* `+purge custom --emoji --starts "lol" --starts "xd"` Remove messages that contains custom emojis and start with lol or xd.
* `+purge custom --starts "Bonjour" --ends "au revoir" -- or`Remove messages that start with "Bonjour" or end with "au revoir". 
* `+purge custom --reactions`Remove messages that have been reacted to.
* `+purge custom --embeds --bot` Remove messages from bots that also contain embeds.

 




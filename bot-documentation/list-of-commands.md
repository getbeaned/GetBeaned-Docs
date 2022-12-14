# List of commands

On this page, we'll use the default prefix of `+`. Of course, your server prefix may have been changed on the web interface. In any case, add the correct prefix before starting a command.

{% hint style="info" %}
To understand the list of commands, you'll have to remember the following:

* Arguments between brackets are `[required]`
* Arguments in greater-than signs are `<optional>`
* Arguments in curly braces are`{greedy}`, meaning you can have one or more argument of the same type.

For example, in the command `+ban {users} <reason>`, you can ban one or more users with an optional reason.
{% endhint %}

{% tabs %}
{% tab title="Users" %}
| Command                 | Explanation                                                                                                                     |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| `+help`                 | Get a link to this webpage                                                                                                      |
| `+urls <target_member>` | Get the server online logs, and webpages about a specific user.                                                                 |
| `+invite`               | Get a bot invite link to [install GetBeaned on your server](../tutorials/tutorial-setting-up-your-server-for-the-first-time.md) |
| `+info`                 | Show some information about the bot like the author and essential commands                                                      |
| `+level`                | Command to see your [permissions level](levels-and-permissions.md) on a server.                                                 |
| `+ping`                 | Check the health of the connection between the bot and Discord.                                                                 |
| `+permissions_check`    | Run a quick check of the bot permissions on the channel, useful to figure out why the bot isn't working properly.               |
| `+hierarchy [user]`     | Inspect the hierarchy between you and another user and inform you of any problems that may arise using commands on them.        |
| `+doctor`               | Make the bot deeply check it's configuration and report any potential problem found.                                            |
| `+channel_id`           | Gives you the ID of a channel. Used to configure logs.                                                                          |
| `+suggest`              | Suggest a feature to add to the bot. Can also be used to report bugs.                                                           |
{% endtab %}

{% tab title="Trusted" %}
Trusted users can also use normal Users commands

| Command                               | Explanation                                                                                                                                      |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `+note {users} [reason]`              | Add a simple note to the user profile. Doesn't do anything by itself, this mostly serves as a reminder from staff or for very minor infractions. |
| `+warn {users} <reason>`              | Warns users on the server. While warns by themselves don't do anything, thresholds apply to warns and users may get kicked if they reach it.     |
| `+message_info`                       | Inspect a message sent by an user and display some information like the automod logs for this message, the user profile, etc.                    |
| `+snipe`                              | Recover the last deleted message from the channel. Useful if you had seen some spam on the channel that quickly got deleted.                     |
| `+purge {arguments}`                  | Remove messages in bulk. See the [command documentation](../tutorials/using-the-purge-command-to-remove-messages.md) for more information.       |
| `+rename [user] <nickname>`           | Rename a user with an optional nickname. If nickname is not specified, removes the nickname                                                      |
| `+inspect [user/message/channel/...]` | Provides information about a given ID or name, and try to guess what that object is.                                                             |
| `+fake_message [user] [message]`      | Sends a message "as if" the specified user sent it. Used as a test for the `+snipe` command.                                                     |
{% endtab %}

{% tab title="Moderators" %}
Moderators can also use any command Trusted users can.

| Command                            | Explanation                                                                                                                                                                                                                                          |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `+ban <duration>{users} <reason>`  | Ban the users provided in the command, with an optional reason.                                                                                                                                                                                      |
| `+softban {users} <reason>`        | Ban and unban the users given to remove the recent messages they sent. You may add a reason to be displayed.                                                                                                                                         |
| `+kick {users} <reason>`           | Kick the users from your server. They will be able to rejoin using a new invite link.                                                                                                                                                                |
| `+mute <duration>{users} <reason>` | Mute users on the server. They won't be able to speak until unmuted or until they leave and rejoin the server. **This command requires a specific GetBeaned\_Muted role, that can be setup by server admins with the `+create_muted_role` command.** |
| `+unmute {muted_users} <reason>`   | Remove the GetBeaned\_Muted role from users, to let them talk again.                                                                                                                                                                                 |
| `+unban {banned_users} <reason>`   | Unban users from your server. They'll be able to rejoin using a new invite.                                                                                                                                                                          |
| `+automod_debug [message]`         | Analyse the message provided in the message argument. This will return a score for you to use.                                                                                                                                                       |
| `+automod_logs [message]`          | Returns the automod logs for a given message ID                                                                                                                                                                                                      |
{% endtab %}

{% tab title="Admins" %}
Admins can also use any command Moderators can.

| Command                                | Explanation                                                                                                                                                                                                                                                                                                                                                                                                                           |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `+add_admin {roles_or_users}`          | <p>Add the specified users to the admin rank on the bot, allowing them to access admin commands and edit server settings on the Web interface. <br>There are three ways to add admins (the <code>Administrator</code> permission, using roles or using users). If you want the admins you add <strong>to be able to edit settings</strong> on the web interface, <strong>you need to add them using users and not roles.</strong></p> |
| `+add_moderator {roles_or_users}`      | <p>Add the specified user to the moderator role on the bot. To remove users or roles from the ranks, use the web interface. <br>You can also give the Ban permission to users to make them moderators.</p>                                                                                                                                                                                                                            |
| `+add_trusted_member {roles_or_users}` | <p>Add members to the Trusted rank, giving them access to the Trusted commands. <br>You can also give the kick permission to users to make them Trusted.</p>                                                                                                                                                                                                                                                                          |
| `+create_muted_role`                   | <p>Create or update a GetBeaned_Muted role to enable the <code>+mute</code>and <code>+unmute</code> commands on your server.<br> If you messed up the role permissions, re-running the command should fix the role.</p>                                                                                                                                                                                                               |
| `+import_bans`                         | Import your server bans on the Web interface for easy viewing and complete history. This can only be run once per server, and the command may take some time to run.                                                                                                                                                                                                                                                                  |
| `+dehoist_users`                       | Run the configured DeHoister on every member on the server.                                                                                                                                                                                                                                                                                                                                                                           |
{% endtab %}

{% tab title="Bot staff" %}
The commands shown are are only available to bot moderators.

If you aren't sure, you **aren't** a bot moderator.

| Command                 | Explanation                                                                                |
| ----------------------- | ------------------------------------------------------------------------------------------ |
| `+pm [user] [message]`  | Use the bot to send a private message to a user.                                           |
| `+end_pm`               | End your DM session with an user                                                           |
| `+cache_status`         | Show the status of the caches used by the bot.                                             |
| `+cache_cleanup`        | Cleanup the cache by removing expired entries immediately. May help freeing some ram.      |
| `+update_analytics`     | Send an updated Guild count to some bot lists. No personal information is sent by the bot. |
| `+refresh_user {users}` | Refresh users account information on the web interface.                                    |
| `+jsk`                  | See the [Jishaku docs](https://jishaku.readthedocs.io/en/latest/cog.html#commands)         |
{% endtab %}

{% tab title="Other" %}
VIPs are special users of the bot. While they don't get any special moderation level, they can access some commands reserved to them. There are sevral ways of becoming a VIP, most of them are detailed in the [VIP Servers](vip-servers.md) docs. Commands for VIP **must** be ran in the #vips channel of the GetBeaned Support Server

| Command             | Condition                  | Explanation                                                                                                                                                 |
| ------------------- | -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `+make_vip [guild]` | VIP and owner of the guild | Give a given guild ID VIP perms on the bot. This will allow the guild to use special parameters. For more info, see the [VIP Servers](vip-servers.md) docs. |
{% endtab %}
{% endtabs %}

# List of commands

On this page, we'll not use the default prefix of `+`. Of course, your server prefix may have been changed on the web interface. In any case, add the correct prefix before starting a command.

{% hint style="info" %}
To understand the list of commands, you'll have to remember the following:

* Arguments between brackets are `[required]`
* Arguments in greater-than signs are `<optionnal>`
* Arguments in curly braces are`{greedy}`, meaning you can have one or more argument of the same type.

For example, in the command `+ban {users} <reason>`, you can ban one or more users with an optional reason. 
{% endhint %}

{% tabs %}
{% tab title="Users" %}
| Command | Explanation |
| :--- | :--- |
| `+help` | Get a link to this webpage |
| `+urls <target_member>` | Get the server online logs, and webpages about a specific user. |
| `+invite` | Get a bot invite link to [install GetBeaned on your server](tutorial-setting-up-your-server-for-the-first-time.md) |
| `+info` | Show some information about the bot, as the author and essential commands |
| `+level` | Command to see your [permissions level](levels-and-permissions.md) on a server. |
| `+ping` | Check the health of the connection between the bot and Discord. |
| `+permissions_check` | Run a quick check of the bot permissions on the channel, useful to figure out why the bot isn't working properly. |
| `+hierarchy [user]` | Inspect the hierachy between you and another user and inform you of any problems that may arise unning commands on them. |
| `+doctor` | Make the bot deeply check it's configuration and report any potential problem found. |
| `+channel_id` | Gives you the ID of a channel. Used to configure logs. |
{% endtab %}

{% tab title="Trusted" %}
Trusted users can also use normal Users commands

| Command | Explanation |
| :--- | :--- |
| `+note {users} [reason]` | Add a simple note to the user profile. Don't do anything by itself, this mostly serve as a remainder from staff or for very minor infractions. |
| `+warn {users} <reason>` | Warns users on the server. While warns by themselves don't do anything, thresholds apply to warns and users may get kicked if they reach it. |
| `+kick {users} <reason>` | Kick the users from your server. They will be able to rejoin using a new invite link. |
| `+message_info` | Inspect a message sent by an user and display some informations like the automod logs for this message, the user profile, ... |
| `+snipe` | Recover the last deleted message from the channel. Useful if you had seen some spam on the channel that quickly got deleted. |
| `+purge {arguments}`  | Remove messages in bulk. See the [command documentation](using-the-purge-command-to-remove-messages.md) for more information. |
{% endtab %}

{% tab title="Moderators" %}
Moderators can also use any command Trusted users can.

| Command | Explanation |
| :--- | :--- |
| `+ban {users} <reason>` | Ban the users provided in the command, with an optionnal reason. |
| `+softban {users} <reason>` | Ban and unban the users given to remove the recent messages they sent. You may add a reason to be displayed. |
| `+mute {users} <reason>` | Mute users on the server. They won't be able to speak until unmuted or until the leave and rejoin the server. **This command required a specific GetBeaned\_Muted role, that can be setup by server admins with the `+create_muted_role` command.** |
| `+unmute {muted_users} <reason>` | Remove the GetBeaned\_Muted role from users, to let them talk again. |
| `+unban {banned_users} <reason>` | Unban users from your server. They'll be able to rejoin using a new invite. |
| `+automod_debug [message]` | Analyse the message provided in the message argument. This will return a score for you to use. |
{% endtab %}

{% tab title="Admins" %}
Admins can also use any command Moderators can.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Command</th>
      <th style="text-align:left">Explanation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>+add_admin {roles_or_users}</code>
      </td>
      <td style="text-align:left">
        <p>Add the specified users to the admin rank on the bot, allowing them to
          access admin commands and edit server settings on the Webinterface.</p>
        <p>There are three ways to add admins (the <code>Administrator</code>permission,
          using roles or using users). If you want the admins you add <b>to be able to edit settings</b> on
          the web interface, <b>you need to add them using users and not roles.</b>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>+add_moderator {roles_or_users}</code>
      </td>
      <td style="text-align:left">
        <p>Add the specified user to the moderator role on the bot. To remove users
          or roles from the ranks, use the webinterface.</p>
        <p>You can also give the Ban permission to users to make them moderators.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>+add_trusted_member {roles_or_users}</code>
      </td>
      <td style="text-align:left">
        <p>Add members to the Trusted rank, giving them access to the Trusted commands.</p>
        <p>You can also give the kick permission to users to make them Trusted.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>+add_banned_member {roles_or_users}</code>
      </td>
      <td style="text-align:left">Ban users or roles from using GetBeaned commands.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>+crate_muted_role</code>
      </td>
      <td style="text-align:left">Create or update a GetBeaned_Muted role to enable the <code>+mute</code>and <code>+unmute</code> commands
        on your server. If you messed up the role permissions, re-running the command
        should fix the role.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>+import_bans</code>
      </td>
      <td style="text-align:left">Import your server bans on the webinterface for easy viewing and complete
        history. This can only be run once per server, and the command may take
        some time to run.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>+dehoist_users</code>
      </td>
      <td style="text-align:left">Run the configured DeHoister on every member on the server.</td>
    </tr>
  </tbody>
</table>
{% endtab %}

{% tab title="Bot staff" %}
The commands shown are are only available to bot moderators.

If you aren't sure, you **aren't** a bot moderator.

| Command | Explanation |
| :--- | :--- |
| `+pm [user] [message]` | Use the bot to send a private message to a user. |
| `+cache_status` | Show the status of the caches used by the bot. |
| `+cache_cleanup` | Cleanup the cache by removing expired entries immediatly. May help freeing some ram. |
| `+update_analytics` | Send an updated Guild count to some bot lists. No personnal information is sent by the bot. |
| `+refresh_user {users}` | Refresh users account information on the webinterface. |
{% endtab %}
{% endtabs %}


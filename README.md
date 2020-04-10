# Welcome to the GetBeaned documentation

## GetBeaned is a Discord Moderation bot.

GetBeaned is the only bot you'll ever need to moderate your server. Why? The primary feature is the **AutoModerator**. It's not like Dyno or MEE6 automod, it is way more advanced and has got less false-positives.

### How does it work?

The automoderator works by calculating a multiplicator, that represents how likely a user has a tendency to spam. Using multiple data points, such as the Discord Nitro status of the user, the account age and how long ago the user joined, GetBeaned is able to have a pretty good estimate of the spam-potential of an user.

After calculating the multiplicator, GetBeaned will then look at the specific message to determine if it could be considered as spam, using factors such as the presence of CAPS, swear words, failed @everyone pings, etc.

Finally, by multiplying the multiplicator and the message score, GetBeaned applies actions corresponding to the specific total score.

$$
multiplicator * message\ score = message\ total\ score
$$

### What does that mean in practice?

Have you ever been on a server, and then tried to send messages quickly one after another or just with a few CAPITAL letters, only to see it get removed by a very strict moderation bot, while, at the same time in another channel, a user is spamming mentions without getting banned? Well, if you don't want that to happen on your server,  **GetBeaned is the solution!**

A user that has just joined and tries to post invite links should be treated as a spammer while a trusted user that has been present for a year shouldn't. And that's what the GetBeaned AutoModerator does.

### More information on the bot configuration.

You can configure GetBeaned on the webinterface by logging in with Discord. The defaults provided are quite good, just enabling Thresholds and Automod should get you started!

{% hint style="info" %}
More settings are provided for advanced configuration. For best performance and to minimise the risk of false positives, we recommend enabling AutoMod and Thresholds, then enable AutoInspect and AutoTriggers as needed.
{% endhint %}

But, if you need, more than 60 settings are available. So, customising the bot shouldn't be a problem.

### Need support?

Not a problem, we are here to help on the [support server](https://discordapp.com/invite/cPbhK53)

### Contributing:

#### If you are a developer:

The bot code is open-sourced on [GitHub](https://github.com/getbeaned) and Pull Requests are welcomed with great pleasure.  
An API is available on request to access the data on the GetBeaned website to improve overall detection. Please contact Eyesofcreeper\#0001 if you are interested.

#### If you are a Discord server owner:

Please[ install the bot](tutorials/tutorial-setting-up-your-server-for-the-first-time.md) and spread the word. Don't forget to report spambots or new types of spam that aren't currently detected by the GetBeaned algorithms.

#### If you are a Discord user:

If my bot has helped you, [donations](https://www.paypal.me/duckduckhunt) are welcome to help fund the server costs! If you find any bugs, feel free to report them on the support server or contact me on Discord : Eyesofcreeper\#0001

 




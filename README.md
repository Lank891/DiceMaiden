# Dice Maiden
<p align="center">
 <a href="https://discordbots.org/bot/377701707943116800" >
  <img src="https://discordbots.org/api/widget/377701707943116800.svg" alt="Dice Maiden" />
</a>
<br>Dice bot for Discord
</p>

# Quick Install
Follow the link to add the bot to your discord server : 

https://discordapp.com/api/oauth2/authorize?client_id=572301609305112596&scope=bot&permissions=11264

This will authorize the bot for your server and you should see it in your default public channel. The bot will have permissions to read, send and manage messages.

**NOTE:** When you first add the bot to your server, it may show up as offline. This is normal! It can take some time for your server to be cached by the bot.

# Manual Install
If you wish to host this yourself, utilize dice_maiden_lite.rb. Dice Maiden requires ruby version 2.3+. There are a handful of gems required as well which are listed in the Gemfile. You will also need to create a bot which can be done at the [discord developer section](https://discordapp.com/developers/applications/me)

# How to use
Below are examples of the dice roll syntax.

`!roll 2d6 + 3d10` : Roll two six-sided dice and three ten-sided dice.

`!roll 3d6 + 5` : Roll three six-sided dice and add five. Other supported static modifiers are add (+), subtract (-), multiply (*), and divide (/). **NOTE:** These static modifiers must be applied to the end of the roll syntax and after other modifiers.

`!roll 3d6 e6` : Roll three six-sided dice and explode on sixes. 

`!roll 3d10 d1` : Roll three ten-sided dice and drop one die. The lowest value will be dropped first.  **NOTE:** These dice are dropped before any dice are kept with the following `k` command. Order of operations is : roll dice, drop dice, keep dice

`!roll 3d10 k2` : Roll three ten-sided dice and keep two. The highest value rolled will be kept. 

`!roll 4d6 r2` : Roll four six-sided dice and reroll any that are equal to or less than two. 

`!roll 6d10 t7` : Roll six ten-sided dice and any that are seven or higher are counted as a success. The dice in the roll are not added together for a total. Any die that meets or exceeds the target number is added to a total of successes. 

`!roll 5d10 t8 f1` : f# denotes a failure number that each dice must match or be beneath in order to count against successes. These work as a sort of negative success and are totaled together as described above. In the example roll, roll five ten-sided dice and each dice that is 8 or higher is a success and subtract each one. The total may be negative. If the option is given a 0 value, that is the same as not having the option at all thus a normal sum of all dice in the roll is performed instead.

`!roll 4d10 kl3` : Roll four ten-sided dice and keep the lowest three dice rolled. **NOTE:** This modifier will only work with comments and math modifiers

`!roll purge 10`: Purge the last 10 messages from channel. The purge value can be between 2 to 100 messages and requires the user to have the "manage messages" role.

`!roll 4d6 ! Hello World!`: Roll four six-sided dice and add comment to the roll.

`!roll 6 4d6` : Roll 6 sets of four sixe-sided dice. A size of a set can be between 2 and 20.

`!roll s 4d6` : Simplify roll output by not showing the tally.

`!roll 4d6 ! unsort` : Roll four six-sided dice and unsort the tally.

`!roll help` : Displays basic usage instructions.

These commands can be combined. For example: 

`!roll 10d6 e6 k8 +4` : Roll ten six-sided dice , explode on sixes and keep eight of the highest rolls and add four.


# Support
Found a bug? Have a feature request? Create an issue on github. Thanks!

You can also join the Discord Support server: https://discord.gg/4T3R5Cb

If you wish to support the bot and donate, you can do so via Patreon [here](https://patreon.com/dicemaiden) or paypal via donate bot [here](https://donatebot.io/checkout/534632036569448458?buyer=176097017926385664)!

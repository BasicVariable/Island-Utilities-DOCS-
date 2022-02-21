# Island-Utilities-DOCS-
https://discord.gg/6ASdpBjbDX / Basic#2142

# How to use:
```
1. Download the bot from the latest pin in #downloads
2. Extract the zip
3. Place all of ATB's files inside the "TradeBot" folder
4. Open the config outside of the "TradeBot" folder and edit it to your liking
5. Run the index-win.exe file (either in command prompt or by just double clicking it)
```

# How to get tokens:
```
> "roli_token"
1. Go to "https://www.rolimons.com/tradeadcreate"
2. Login to Rolimons (if you aren't already) and inspect the web page
3. Go to the network tab and refresh the page 
4. Click the first request called "tradeadcreate" and scroll down to the request headers section
5. Find cookie section of the header then copy the "_RoliVerification" token until the "_RoliData" token starts 
6. Paste the token (including the "_RoliVerification" section of it) in the string that follows "roli_token": in the config.json file

> "bot_token"
1. Go to "https://discord.com/developers/applications" and login to your discord account
2. Press "New Application" and name the bot anything you'd like
3. Click the three bars at the top right of the screen and click the "Bot" tab
4. Create a bot and click "reveal token"
5. Copy the token and paste it into the string that follows "bot_token": in the config.json file
```

# Documentation
```
> "rbx_cookie"
Your Roblox cookie

> "discord_id"
Your discord id (I can't help you if you don't know what this is...)

> "bot_token"
Your discord bot's secret token

> "WL_key"
Your WL_key (given to you when you purchase the bot)

> "display_on"
When set to true the bot will display your Roblox account as online 

> "prefix"
The prefix to IU commands (EX: "!"help)

> "discord_id"
Your discord id as a number (prevents other people from using specifc commands)

> "embed_color"
The color of the embedded notifications in HEX CODE (https://www.htmlcsscolor.com/hex/00B3FF)

> "notify_completeds"
When set to true the bot will post completeds in the set discord channel

> "check_interval"
How frequently the bot will check for completeds in seconds

> "discord_channel"
The Discord channel ID in which the bot will post certain notifications (depends on what its under -> completeds or trade ads)

> "tag"
The tag or format the bot will use to mention people/a person
Specific user format - <@DISCORDID>
Specific role format - <@&ROLEID>

> "notifiy_inbounds"
When set to true the bot will check for new inbounds and inbound wins

> "rs_wins_int"
The time in seconds the bot has to wait before restating cached "win" trade

> "check_outbounds"
When set to true the bot will check outbounds for losses

> "cache_interval"
The amount of time, in seconds, in which the bot will cache new outbound/inbound trades

> "check_interval"
The amount of time, in seconds, in which the bot will check cached outbounds/inbounds

> "profit_deviance"
The minimum amount of value from what the bot would offer for the outbound to be declined or inbound to be notified
EX -> Original offer: 15k for 15.5k | Offer after 2hrs: 15k for 15.2k 
If the bot was set to decline at 200 profit deviance this trade would be declined or no longer alerted as a win with the inbound checker

> "avoid_younger_then"
The number of seconds the bot has to wait before checking a trade (from the moment it was cached)
EX -> a trade was cached at 6:18
If this option was set to wait 60 seconds before checking a newly cached trade it wouldn't check it for a loss 

> "avoid_older_then"
How old a trade has to be, in seconds, for the outbound checker to no longer check it for losses

> "min_under"
The minimum amount an item has to be under rap for the bot to revalue the item (in outbounds)

> "post_ads"
When enabled the bot will attempt to post tradeads to Rolimons.com

> "rwait_min" 
The minimum amount of time, in seconds, the bot will wait to attempt to create another add

> "rwait_max"
The maximum amount of time, in seconds, the bot will wait to attempt to create another add

> "item_ids"
The items you want to offer in the Ad (added with the perfered item's assetid)

> "r_items"
The items you want to request in the Ad (added with the perfered item's assetid)

> "r_tags"
The rolimons tags used on the requesting side of the Ad (added as a string and all lowercase letters)

> "posttop"
Enabling this (by setting it from false to true) will force the bot to add your top 4 items (sorted by rolimons value) to the offer side of the trade Ad

> "restate"
Enabling this (by setting it from false to true) will restate your last outbound (in which you still have the items for) as a trade Ad (usefull for trade bots)

> "configure_config"
When set to true the bot will automatically configure the bot when a new completed is found

> "proxies"
The proxies the bot will use (rotating ip proxies are preferred)

> "offer_values"
Allows you to set what certain items specifically get (at the minimum), the format is "itemid":opitgets

> "send"
The types of trades you'd like the configured bot to send

> "configure_sendables"
When set to true the bot will automatically decide whether your bot will send upgrades, downgrades, and mixed trades

> "min_inv"
The minimum about of items (you'd be able to have) before the bot would configure your bot to send downgrade/mixed trades

> "max_inv"
The maximum about of items (you'd be able to have) before the bot would configure your bot to send upgrade/mixed trades

> "dnt"
A list of items you'd like the configured bot to not trade

> "dntf"
A list of items you'd like the configured bot to not trade for

> "dnt_to"
A list of people you'd like the configured bot avoid sending trades to

> "dnt_rap"
When set to true the auto-config will automatically blacklist all rap items from being traded

> "plug"
When set to true the configured bot will scrape rbx_flip

> "otf_value"
When set to true the configured bot will only trade for valued items

> "otf_rap"
When set to true the configured bot will only trade for rap items

> "dnt_items_under"
The minimum amount of value items in your inv need to be traded 

> "overvalue_algo"
When set to true the bot will configure an overvalue amount for rap items under 5k

> "proj_algo" - "configure_ratio"
When set to true the bot will create an owned proj ratio for your (marked) projecteds

> "rid_projs"
When set to true the bot will configure projecteds to be the only items traded (prioritize them to be traded off)

> "lb_projs_by"
The amount you'd like the bot to lb your projecteds
```

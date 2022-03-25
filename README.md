# Island-Utilities-DOCS-
https://discord.gg/6ASdpBjbDX / Basic#2142

# How to use:
```
1. Download the bot from the latest pin in #downloads
2. Extract the zip
3. Place all of your selected bot's files inside the "TradeBot" folder
4. Open the config outside of the "TradeBot" folder and edit it to your liking (please be sure to go over every setting I wrote the DOCs for a reason)
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
6. Go back to the sub-menu that you got through step 3 and pess "OAuth2" then press "URL Generator"
7. Click the "Bot" check-mark under scopes and give the bot "Administrator" permisisons.
8. Copy the Generated link and use it to invite the bot to your server
```

# Documentation
```
> "rbx_cookie" [config > auth]
Your Roblox cookie.

> "roli_token" [config > auth]
Your rolimons token, used to send trade ads.

> "bot_token" [config > auth]
Your discord bot's secret token.

> "WL_key" [config > auth]
Your WL_key (given to you when you purchase the bot).

> "IU_Proxies" [config > auth]
Your proxies, in a user:pass@host:port format, that will be used to get new rap values.

> "run_file" [config > trade_bot]
Your selected trade bot's file that is used to start it, be sure to include its file type extension-ex: .exe (if your bot doesn't have this please DM Basic#2142).

> "config_file" [config > trade_bot]
Your selected trade bot's config file, be sure to include its file type extension-ex: .json .txt .exe.

> "display_on" [config]
When set to true the bot will display your Roblox account as online.

> "prefix" [config > discord_bot]
The prefix to IU commands (EX: "!"help).

> "discord_id" [config > discord_bot]
Your discord id as a number (prevents other people from using specifc commands).

> "embed_color" [non-specific]
The color of the embedded notifications in HEX CODE (https://www.htmlcsscolor.com/hex/00B3FF).

> "notify_completeds" [config > completed_notifier]
When set to true IU will post completeds in the set discord channel.

> "check_interval" [config > completed_notifier]
How frequently IU will check for completeds in seconds.

> "discord_channel" [non-specific]
The Discord channel ID in which IU will post certain notifications (depends on what its under -> completeds or trade ads).

> "tag" [non-specific]
The tag or format IU will use to mention people/a person.
Specific user format - <@DISCORDID>
Specific role format - <@&ROLEID>

> "notifiy_inbounds" [config > inbound_notifier]
When set to true IU will check for new inbounds and inbound wins.

> "only_send_wins" [config > inbound_notifier]
When set to true IU will only notify trades that are considered wins by IU's valuing system.

> "rs_wins_int" [config > inbound_notifier]
The time in seconds IU has to wait before restating cached "win" trade.

> "check_outbounds" [config > outbound_checker]
When set to true IU will check outbounds for losses.

> "cache_interval" [non-specific]
The amount of time, in seconds, in which IU will cache new outbound/inbound trades.

> "check_interval" [non-specific]
The amount of time, in seconds, in which IU will check cached outbounds/inbounds.

> "avoid_younger_then" [config > outbound_checker]
The number of seconds IU has to wait before checking a trade (from the moment it was cached).
EX -> a trade was cached at 6:18
If this option was set to wait 60 seconds before checking a newly cached trade it wouldn't check it for a loss 

> "avoid_older_then" [config > outbound_checker]
How old a trade has to be, in seconds, for IU to no longer check it for losses/wins.

> "profit_deviance" [config > valuing]
The minimum amount of value from what the bot would offer for the outbound to be declined or inbound to be notified.
EX -> Original offer: 15k for 15.5k | Offer after 2hrs: 15k for 15.2k 
If IU was set to decline at 200 profit deviance this trade would be declined or no longer alerted as a win with the inbound checker

> "min_under" [config > valuing]
The amount of rap an item has to be from it's minimum rap requirement for IU to revalue it.

> "upgrade_multiplier" [config > valuing]
The mutiplier for items in upgrade trades.

> "downgrade_multiplier" [config > valuing]
The mutiplier for items in downgrade trades.

> "mixed_multiplier" [config > valuing]
The mutiplier for items in mixed trades.

> "offer_values" [config > valuing]
The custom values for items you are offering.
EX:
{
  "item": 0,
  "overwritten_value": 99999999
}

> "request_values" [config > valuing]
The custom values for items you are requesting.
EX:
{
  "item": 0,
  "overwritten_value": 99999999
}

> "overvalue_offer_smalls" [config > valuing]
The minimum amount an item (on the offering side) has to be to have it's rap added to the set amount you'd like to add.

> "undervalue_request_smalls" [config > valuing]
The minimum amount an item (on the requesting side) has to be to have it's rap subtracted to the set amount you'd like to subtract.

> "projecteds" [config > valuing]
The multipler you'd like to use on projecteds you are offering and requesting.

> "post_ads" [config > auto_ad]
When enabled IU will attempt to post tradeads to Rolimons.com

> "posttop" [config > auto_ad]
Enabling this (by setting it from false to true) will force IU to add your top 4 items (sorted by rolimons value) to the offer side of the trade Ad.

> "restate" [config > auto_ad]
Enabling this (by setting it from false to true) will restate your last outbound (in which you still have the items for).

> "rwait_min" [config > auto_ad] 
The minimum amount of time, in seconds, IU will wait to attempt to create another add.

> "rwait_max" [config > auto_ad]
The maximum amount of time, in seconds, IU will wait to attempt to create another add.

> "item_ids" [config > auto_ad]
The items you want to offer in the Ad (added with the perfered item's assetid).

> "r_items" [config > auto_ad]
The items you want to request in the Ad (added with the perfered item's assetid).

> "r_tags" [config > auto_ad]
The rolimons tags used on the requesting side of the Ad (added as a string and all lowercase letters).

> "configure_config" [config > auto_config]
When set to true IU will automatically configure ATB's config (this feature only works for ATB-Acier Trade Bot).

> "keep_base_config" [config > auto_config]
When set to true IU will keep a majority of the config (the way you set it) except for the do_not_trade, do_not_trade_for, only_trade_for_rap, only_trade_for_value, users_dont_send_to, proxies_list, cookie, userid, static_offer_values, and static_request_values. These settings will be applied based on your IU config (this feature only works for ATB-Acier Trade Bot).

> "proxies" [config > auto_config]
The proxies ATB will use (rotating ip proxies are preferred).

> "use_proxies" [config > auto_config]
When set to false ATB won't use proxies.

> "offer_values" [config > auto_config]
Allows you to set what certain items (on the offering side) specifically get (at the minimum), the format is "itemid":opitgets.

> "request_values" [config > auto_config]
Allows you to set what certain items (on the requesting side) specifically get (at the minimum), the format is "itemid":opitgets.

> "send" [config > auto_config]
The types of trades you'd like ATB to send.

> "configure_sendables" [config > auto_config]
When set to true IU will automatically decide whether your bot will send upgrades, downgrades, and mixed trades.

> "min_inv" [config > auto_config]
The minimum about of items (you'd be able to have) before IU would configure your bot to send downgrade/mixed trades.

> "max_inv" [config > auto_config]
The maximum about of items (you'd be able to have) before IU would configure your bot to send upgrade/mixed trades.

> "dnt" [config > auto_config]
A list of items you'd like ATB to not trade.

> "dntf" [config > auto_config]
A list of items you'd like ATB to not trade for.

> "dnt_to" [config > auto_config]
A list of people you'd like ATB avoid sending trades to.

> "dnt_rap" [config > auto_config]
When set to true the auto-config will automatically blacklist all rap items from being traded.

> "plug" [config > auto_config]
When set to true ATB will scrape rbx_flip.

> "otf_value" [config > auto_config]
When set to true ATB will only trade for valued items.

> "otf_rap" [config > auto_config]
When set to true ATB will only trade for rap items.

> "dnt_items_under" [config > auto_config]
The minimum amount of value items in your inv need to be traded.

> "overvalue_algo" [config > auto_config]
When set to true IU will configure an overvalue amount for rap items under 5k.

> "proj_algo" - "configure_ratio"  [config > auto_config]
When set to true IU will create an owned proj ratio for your (marked) projecteds.

> "rid_projs" [config > auto_config]
When set to true IU will configure projecteds to be the only items traded (prioritize them to be traded off).

> "lb_projs_by" [config > auto_config]
The amount you'd like IU to lb your projecteds.
```

![MaxBans](https://i.imgur.com/1oUe2e4.png)

This is a **FORK** of [MaxBans from Netherfoam](https://dev.bukkit.org/projects/maxbans), wich was a project he has been writing for his server, MaxGamer. He struggled to find a banning plugin that wasn't a joke, and the good plugins were all designed for Premium servers anyway. Nothing gave them the tools that SHOULD have been out there - Like temp mutes, temp IP, bans, duplicate IP lookups, and good autocompletion!

It is thoroughly tested on an Offline-Mode server, so you can bet it's rock solid and feather light!

### <span id="anchor-1"></span>Databases 

- MySQL
- SQLite (Flatfile)

### <span id="anchor-2"></span>Best Features 

Here are the top ten features of MaxBans over other banning plugins:

1.  Full UUID support
2.  Ability to view players' previous username(s) - date of change
3.  Full server lockdown - Prevent anyone from joining with a custom
    message (Such as bot attacks)
4.  Offline player name auto completion
5.  Warnings system
6.  Duplicate IP detection
7.  DNSBL lookups to stop proxys!
8.  Multiline kick messages! No more running off the screen!
9.  Notifications when a banned player tries to join!
10. All times are relative! (Eg. "You're banned for 4 minutes 6
    seconds", not "You're banned til 5:43pm CST")
11. Customize every colour!
12. Block commands like /me when muted!

### <span id="anchor-3"></span>Commands

- /unban \<name, IP or UUID\>
- /ban \<name, IP or UUID\> \<reason\>
- /ipban \<name, IP or UUID\> \<reason\>
- /tempban \<name, IP or UUID\> \<number\>
  \<minutes\|hours\|days\|weeks\|etc\> \<reason\>
- /tempipban \<name, IP or UUID\> \<number\>
  \<minutes\|hours\|days\|weeks\|etc\> \<reason\>
- /mute \<name or UUID\>
- /tempmute \<name or UUID\> \<number\>
  \<minutes\|hours\|days\|weeks\|etc\>
- /kick \<name, \* for everyone or UUID\>
- /checkip \<name or UUID\>
- /uuid
- /togglechat
- /dupeip \<name, IP or UUID\>
- /checkban \<name, IP or UUID\>
- /warn \<name or UUID\> \<reason\>
- /clearwarnings \<name or UUID\> \<reason\>
- /unwarn \<name or UUID\> - Removes a players most recent warning
- /unmute \<name or UUID\>
- /history \[name\] \[number of records\] - Displays a history of bans,
  kicks, mutes & more dealt
- /mbreload - Reloads the plugin
- /mbdebug - Outputs debug information for me if you're having issues!
- /mbwhitelist \<name or UUID\> - Allows the given user to bypass IP
  bans (Not regular bans! Eg, use for players with siblings who need to
  be IP banned)
- /ipreport - Basically, a mass /dupeip, on everyone who is online
- /lockdown \[reason\]
- /forcespawn - Teleports someone to the spawn (Twice, so /back won't
  work)
- /mbreload - Reloads maxbans
- /mbimport - Imports vanilla minecraft (And others) bans.
- /mbexport - Export bans to vanilla, MySQL or SQLite databases. (Allows
  swapping SQLite \<-\> MySQL), and others ban plugins.
- /rangeban \<ip1-ip2\> \[reason\] - Bans the IP range from ip1 to ip2
  for the supplied reason.
- /temprangeban \<ip1-ip2\> \<time\> \<hours/min/sec\> \[reason\] -
  Temporary variant of above
- /unrangeban \<ip\> - Removes any RangeBan which overlaps with the
  given IP. Eg, if 127.0.0.1-127.0.0.5 is banned, unbanning 127.0.0.3
  will lift the whole ban on 127.0.0.1-127.0.0.5.

Almost any command may have -s added in it to prevent announcing it, for
example:\
\
\
/tempban NewGuy101 -s 1 hour MaxBans is Awesome!

\- Nobody will see the announcement that NewGuy101 was temp banned, just
the fact he "has left the game."

If you want an in-depth analysis of each command, try here:\
\
<http://dev.bukkit.org/server-mods/maxbans/pages/command-tutorial/>

### <span id="anchor-4"></span>Configuration Guide

<http://dev.bukkit.org/server-mods/maxbans/pages/config-tutorial/>

This is an in-depth guide on how to configure MaxBans :) If I've missed
anything, ask in the comments!

### <span id="anchor-5"></span>Common Issues

<http://dev.bukkit.org/server-mods/maxbans/pages/common-issues/>

This is a list of common issues people have with MaxBans, such as plugin
conflicts.

### <span id="anchor-6"></span>Features that will *never* implement

- Fines (Use your economy to do this!)
- Jails
- Regional bans
- Ban weightings

### <span id="anchor-7"></span>Ban Listing Webpage

Check out this guy's work for an amazing webpage setup to view MaxBans
while using MySQL.

Demo (dont download from here):
[http://yive.me/maxbans/](https://web.archive.org/web/20230119013506/https://yive.me/maxbans/).

Its updated and is working on latest version of MaxBans! 

You can download the updated version from
here: <https://github.com/FabioZumbi12/maxbans-php>

- Added pagination;
- Fixed other ban pages not loading;

### <span id="anchor-8"></span>Metrics

This plugin uses Hidendra's plugin metrics system
([http://mcstats.org/plugin/maxbans](https://mcstats.org/plugin/maxbans))
which tracks server information including:

- A unique ID
- Java version
- Online/Offline mode
- Plugin & Server version
- OS name, version, architecture
- Number of CPU cores
- Players online
- Metrics version

These stats can be disabled using the PluginMetrics config file
(BukkitServer/plugins/PluginMetrics/config.yml).

### <span id="anchor-9"></span>GeoIP Lookup

MaxBans will download a GeoIP.csv file, which allows it to look up the
country of origin for IP addresses. The file is downloaded directly from
maxmind GeopIP site. The file is only downloaded once (Unless it is
renamed/removed).


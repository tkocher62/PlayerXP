# PlayerXP

This is a plugin for my game server that adds a leveling system to the game. As users perform in game actions, they gain experience (xp). After reaching a certain amount of xp, the player will level up. This plugin acts as a baseline for other plugins. Using the API provided, other plugins can take advantage of this leveling system for their own purposes. See below for a full list of features and videos.

# Installation

**[EXILED](https://github.com/galaxy119/EXILED) must be installed.**

Place the `PlayerXP.dll` file in your `Exiled/Plugins` folder.

# Features
* Grants xp to players for completing game tasks.
* Scale factor for all xp values.
* All xp rates are configurable, as well as all messages displayed to users for gaining xp.
* Players will be given small configurable messages on their screen to notify them when they gain xp, as well as level up.
* Fully configurable karma system.
  * Players will gain karma for doing good deeds.
  * Players will lost karma for doing bad deeds such as killing unarmed Class-D or Scientists.
  * Karma is an xp multiplier, all players start with a karma of 1.00.
  * Players with karma below a certain amount can be denied the ability to play SCP.
  * This system can be toggled on and off.
* Commands that can be run through RA console **or** client console by using the prefix `.` to check the level, xp, and server ranking of a user, as well as the server leaderboard.
* Commands to calculate a server leaderboard based off a configurable size and check a player's level.
* Levels get increasingly harder to achieve, the amount in which is takes to achieve the next level can be modified.
* When a player is killed, the victim gets a message displaying the killers level.
* All data transfer between servers.

# API
Developers can access and modify data about each player through the API. After referencing this assembly, add the namespace `PlayerXP.API` to your file. You will then be able to access several useful methods to retrieve and modify data through the `PXP` class.

# Commands

**Commands that can be run from both RA console and player console. These commands must use the prefix `.` if they are being run through the player console.**

| Command        | Value Type | Description |
| :-------------: | :---------: | :------ |
| LVL / LEVEL | PLAYER NAME / STEAMID64 | Displays a user's level and xp. Will also display their server ranking. Not specifying a name will default to yourself. |
| LB / LEADERBOARD | SIZE | Displays the top users in the server. If no size is specified it will output the top 5. Maximum leaderboard size is 15. |

**Commands that can only be run through RA console.**

| Command        | Description |
| :-------------: | :------ |
| XPTOGGLE | Toggles XP gaining/saving. |
| XPSAVE | Forces a file save from the current round cache. |

# Videos

### Checking Level

![](https://github.com/tkocher62/PlayerXP/blob/master/gifs/level.gif)

### Gaining XP

![](https://github.com/tkocher62/PlayerXP/blob/master/gifs/kill.gif)

### Checking Leaderboard

![](https://github.com/tkocher62/PlayerXP/blob/master/gifs/leaderboard.gif)

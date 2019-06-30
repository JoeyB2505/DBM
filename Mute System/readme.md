# Mute System (No Database Needed!)

### A muting system with a timer that doesn't reset after the bot has restarted!

Usage: `<p>mute {@user/UserID} {Reason} | {Time}`

**Reason is required**

Example: `<p>mute @Owl Hello world | 7d 5h 3m` / `<p>mute 1234567890123 Hello world!`

If no time is provided, then it will mute forever. Time can be provided in days (`d`), hours (`h`), and minutes (`m`). The time is stored in the folder `./data/mutes` in a UNIX timestamp

----

`run_script_new.js` is an action needed (It is from the DBM Network made by MrG0ld [Original Mod](https://raw.githubusercontent.com/MrG0ld/DBM-Gold-Mods/master/actions/run_script.js))

`Mute_CMD.json` = Main command that adds a mute role to a user and sends a message into the log channel<br> (Log channel can be changed in action #22; Role can be changed in action #23)

`Unmute_CMD.json` = Unmutes a user and gets rid of timer if there is one

`MuteAutoCheck_EVENT.json` = Runs every so often (Default 60 seconds, can be changed) that loops through the mutes folder

`MuteTimer_EVENT.json` = It is called by the MuteAutoCheck and it checks each and every file if there is and if the time has passed, it auto unmutes the muted users.

A folder named `mutes` may be needed in `./data` in your bot's project directory

**Note: There still may be some bugs, if there are, please message me Owl#6120**

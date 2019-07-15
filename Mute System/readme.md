# Mute System (No Database Needed!)

### A muting system with a timer that doesn't reset after the bot has restarted! (Also gives the user the Muted role if they try to rejoin

#### The Mute command
Usage: `<p>mute {@user/UserID} {Reason} | {Time}`

**Reason is required**

Example: `<p>mute @Owl Hello world | 7d 5h 3m` / `<p>mute 1234567890123 Hello world!`

If no time is provided, then it will mute forever. Time can be provided in days (`d`), hours (`h`), and minutes (`m`).

#### The Unmute command

Unmutes the user (removes the muted role and if they've been muted by the `<p>mute` command for a specific time, it will remove the timer)

Usage: `<p>unmute {@user/UserID}`<br>
Example: `<p>unmute @Owl` / `<p>unmute 123456123`


----

`run_script_new.js` is an action needed. The action itself is just a nicer version of the "Run Script" (It is from the DBM Network made by MrG0ld [Original Mod](https://raw.githubusercontent.com/MrG0ld/DBM-Gold-Mods/master/actions/run_script.js))

`Mute_CMD.json` = Main command that adds a mute role to a user and sends a message into the log channel<br> (Log channel can be changed in action #22; Role can be changed in action #23)

`Unmute_CMD.json` = Unmutes a user and gets rid of timer if there is one

`AutoUnmuteCheck_EVENT.json` = Runs every so often (Default 20 seconds, can be changed) that loops through the muted users

`AutoUnmute_EVENT.json` = It is called by the AutoUnmuteCheck event and it checks if the user has a mute (From the bot) and check if timer is up! If it is up, then unmutes the user.


**Note: There still may be some bugs, if there are, please message Owl#6120 on discord**

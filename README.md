# Klabot ![alt text](https://i.imgur.com/cbEmj2G.png)

Klabot is a really useless Discord Bot created using DiscordJS and quickDB

# Requirements

- NodeJS v16.6 or higher
- DiscordJSv13 `npm install discord.js @discordjs/rest discord-api-types @discordjs/voice sodium`
- QuickDB `npm install quick.db`
- Discord-Player `npm install --save discord-player ` + `npm install --save @discordjs/opus`

You also need a file named `config.json` with your token from the [Discord Developer Portal](https://discordjs.guide/preparations/setting-up-a-bot-application.html#creating-your-bot),the file should look like this:

```json
{
	"token": "YOUR_TOKEN_HERE"
}
```

For the assets you need to place them on a folder called assets, name the image as liK.png, or change the name on the source.
Also you need a bell.mp3 file on the root for the bell sound, or again change the name on the source.

# Usage

You need to register the slash commands to the client, for more info check the guide [Registering slash commands](https://discordjs.guide/interactions/registering-slash-commands.html#guild-commands)

## "Bell" System

Klabot has a system that will play an audio on A voice channel when someone joins B voice channel, at the moment is not really useless, but in a future commands to
allow users join A voice channel if it's unlocked.
For use this, Klabot needs 2 voice channels: Channel where the .mp3 audio will be played ( A channel ),
and the channel where the bot will be looking if someone is in ( B channel)

For set this channels you can use the bell and door commands, example:

```
/set door #voiceChannel
/set bell #voiceChannel

```

If you want to update the channel ID you can just run the door/bell command again.

You don't need to provide the channel ID in this case, just provide what type of channel you want to remove (bell or door).

## Favorite messages

Klabot provides a way to send your favorite messages to a specified channel, to do this you need to specify the channel where all the favorite messages will be sent.
You can do that with the command `/set favmessage #channel`
Example:

```
 /set favmessage #channel
```

The favorite message are those that have an reaction with the pill emoji :pill:

## Removing channels ID

If you want to remove the channels ID, you can use the deleteid command, example:

```
/unset bell
/unset door
/unset favmessage
```

This will delete the channel ID of the key specified from the quick.db database.

## Music Player

You can reproduce music and YouTube videos with the player commands like: `/play`, `/skip`, `/resume`, `/stop`, `/pause`.

## TODO:

- Add a events creation system, so you can schedule reunions, game times, anything with your friends.
- Add a lock and unlock for voice channels making the bell system more useful.
- Move from quickDB to MongoDB

 <p align=center>
 <img src="https://i.imgur.com/b6aCKA2.png"/>
 </p>

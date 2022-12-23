# discord-mic-bot

Discord bot to connect to any audio source on your linux system.

## Description

Currently the discord feature that allows screen share audio
does not work on the linux version. This script creates
a jack audio output that plays through a discord bot.
Audio can be routed into this output through a patchbay
like qpwgraph.

## Usage

For Linux or macOS users, `discord-mic-bot` is the entry point.
(use in .bashrc to have it start running on startup)

running this will start the bot and create the jack output.
Route the audio you desire to share through a patchbay.

If the bot is invited to the server you are in. It will join
and play audio whenever you start a screen share or turn on


## Installation

First, you need to install Python 3.10 or later version and download
discord-mic-bot.

Then, in terminal or command prompt, type:
```sh
cd /path/to/discord-mic-bot
pip3 install -r requirements.txt --upgrade
```

If fail to install
[PyNaCl](https://github.com/pyca/pynacl/issues/637#issuecomment-710127304) or
[NumPy](https://developercommunity.visualstudio.com/content/problem/1207405/fmod-after-an-update-to-windows-2004-is-causing-a.html)

If on Linux, you also need to install libopus and libportaudio.

## Obtaining a bot token

You need to obtain a bot token to log into Discord's server.

1. Go to <https://discord.com/developers/applications> and click on "New
   Application".

2. Inside the settings panel of your new application, click on "Bot".

3. Create a new bot. When asked about permissions, simply leaving blank is
   enough.

4. Click on "Copy Token".

5. Open the file named `token.txt` and paste your token inside that file.

## Obtaining user ID

The bot need your discord user ID to identify when you are starting streams.
This is how to obtain and get this info to the bot:

1. go to "User Settings">"Advanced" and enable "Developer Mode" here.

2. right click your own account in a server list and select "Copy ID"

3. Open `user.txt` and paste the ID.

## Inviting the bot to a Discord server

Note: You need to have the permission to invite a bot to the destination server.
If you don't have such a permission, the destination server **will not be
shown** in step 4. You can also ask an administrator who has such a permission
to help you invite your bot.

1. Go to <https://discord.com/developers/applications> and click on your already
   created application.

2. Click on "Copy Client ID".

3. Go to
   ```
   https://discord.com/oauth2/authorize?client_id=<CLIENT_ID>&permissions=3145728&scope=bot
   ```
   (Replace `<CLIENT_ID>` with your Client ID)

4. Choose your destination server. Then click "Authorize".


## License

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.

You should have received a copy of the [GNU General Public License](LICENSE)
along with this program.

## Acknowledgment

This project is forked from m13243's discord-mic-bot. I used this
repo to share stream audio for a while before editing it to better
suit my specific purpose for it. Thank you m13243 this bot has been
exceedingly useful.
[discord-mic-bot](https://github.com/m13253/discord-mic-bot).

# Google Play Music Discord RPC
> 🎧 Show your Discord friends which song you're listening to!

![Preview](https://raw.githubusercontent.com/makixx/google-play-music-rpc/master/images/preview.png)

## Installation
- Download **Violentmonkey** from https://violentmonkey.github.io/get-it
- Install **my userscript** from https://raw.githubusercontent.com/makixx/google-play-music-discord-rpc/master/google-play-music-rpc.user.js
- Download **Node.js LTS** from https://nodejs.org/en
- Download and **unzip my script** from https://github.com/makixx/google-play-music-discord-rpc/archive/master.zip
- Rename `config.example.js` to `config.js` 
- Open `INSTALL.bat`
- Open `RUN.bat`

You can then use `pm2` to make it run in the background or make a shortcut to the `RUN.bat` file.

## Issues
- ~~The userscript automatically POSTs (using XMLHttpRequest) when there is a song change, but doing this too often causes the browser to not send the request.~~ Fixed by using web sockets. HOW CAN I NOT HAVE THOUGHT OF THAT EARLIER!! GAHH!
- When the page isn't open, the current time and duration wont get updated.
- When a song is changed, the play/pause element goes into pause mode which can have issues considering Discord doesn't instantly update.
<div align="center">
  <p>
    <a href="https://www.npmjs.com/package/selfcord.js"><img src="https://img.shields.io/npm/v/selfcord.js.svg?maxAge=3600" alt="NPM version" /></a>
  </p>
  <p>
    <a href="https://nodei.co/npm/selfcord.js/"><img src="https://nodei.co/npm/selfcord.js.png?downloads=true&stars=true" alt="npm installnfo" /></a>
  </p>
</div>

# About 
This is a selfbot compatible version of discord.js. It changes the gateway IDENTIFY payload to make the Discord Gateway think that it's the official browser that's connecting.
There's still a lot of work to be done to prevent Discord's gateway from thinking that you are a bot.

Currently it is reccomended that you do **not set your game,** also known as the playing tag, since it'll inform the Gateway that you are infact, using the API instead of a browser.

This fork of discord.js provides no gurantees, but you are free to use it.

This fork of discord.js is avaliable on GitHub and NPM. Download it from NPM [here](https://nodei.co/npm/selfcord.js/) or click the images/links above.
You can also use `npm install selfcord.js` in your node project.

## -- discord.js README.md --

### About
discord.js is a powerful [node.js](https://nodejs.org) module that allows you to interact with the
[Discord API](https://discordapp.com/developers/docs/intro) very easily.

- Object-oriented
- Predictable abstractions
- Performant
- 100% coverage of the Discord API

## Installation
**Node.js 8.0.0 or newer is required.**  
Ignore any warnings about unmet peer dependencies, as they're all optional.

Without voice support: `npm install discord.js`  
With voice support ([node-opus](https://www.npmjs.com/package/node-opus)): `npm install discord.js node-opus`  
With voice support ([opusscript](https://www.npmjs.com/package/opusscript)): `npm install discord.js opusscript`

### Audio engines
The preferred audio engine is node-opus, as it performs significantly better than opusscript. When both are available, discord.js will automatically choose node-opus.
Using opusscript is only recommended for development environments where node-opus is tough to get working.
For production bots, using node-opus should be considered a necessity, especially if they're going to be running on multiple servers.

### Optional packages
- [zlib-sync](https://www.npmjs.com/package/zlib-sync) for significantly faster WebSocket data inflation (`npm install zlib-sync`)
- [erlpack](https://github.com/discordapp/erlpack) for significantly faster WebSocket data (de)serialisation (`npm install discordapp/erlpack`)
- One of the following packages can be installed for faster voice packet encryption and decryption:
    - [sodium](https://www.npmjs.com/package/sodium) (`npm install sodium`)
    - [libsodium.js](https://www.npmjs.com/package/libsodium-wrappers) (`npm install libsodium-wrappers`)
- [uws](https://www.npmjs.com/package/uws) for a much faster WebSocket connection (`npm install uws`)
- [bufferutil](https://www.npmjs.com/package/bufferutil) for a much faster WebSocket connection when *not* using uws (`npm install bufferutil`)

## Example usage
```js
const Discord = require('discord.js');
const client = new Discord.Client();

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.on('message', msg => {
  if (msg.content === 'ping') {
    msg.reply('pong');
  }
});

client.login('token');
```

## Links
* [Website](https://discord.js.org/) ([source](https://github.com/discordjs/website))
* [Documentation](https://discord.js.org/#/docs)
* [Discord.js Discord server](https://discord.gg/bRCvFy9)
* [Discord API Discord server](https://discord.gg/discord-api)
* [GitHub](https://github.com/discordjs/discord.js)
* [NPM](https://www.npmjs.com/package/discord.js)
* [Related libraries](https://discordapi.com/unofficial/libs.html)

### Extensions
* [RPC](https://www.npmjs.com/package/discord-rpc) ([source](https://github.com/discordjs/RPC))

## Contributing
Before creating an issue, please ensure that it hasn't already been reported/suggested, and double-check the
[documentation](https://discord.js.org/#/docs).  
See [the contribution guide](https://github.com/discordjs/discord.js/blob/master/.github/CONTRIBUTING.md) if you'd like to submit a PR.

## Help
If you don't understand something in the documentation, you are experiencing problems, or you just need a gentle
nudge in the right direction, please don't hesitate to join our official [Discord.js Server](https://discord.gg/bRCvFy9).

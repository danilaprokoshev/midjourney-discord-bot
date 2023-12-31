# midjourney-discord

node.js client for Midjourney wrapper in Discord.
<div align="center">
	<p>
		<a href="https://discord.gg/GavuGHQbV4"><img src="https://img.shields.io/discord/1082500871478329374?color=5865F2&logo=discord&logoColor=white" alt="Discord server" /></a>
		<a href="https://hub.docker.com/r/erictik/midjourney-discord/tags">
		    <img src="https://img.shields.io/docker/v/erictik/midjourney-discord?color=5865F2&logo=docker&logoColor=white" alt="Docker" />
		</a>
	</p>
</div>

[web ui example](https://github.com/erictik/midjourney-ui/)

## Implemented commands documentation
[Join discord experience](https://discord.gg/GavuGHQbV4)
Generating idea
```
/oh_imagine [ MT : prompt (string)]
```
![prompt_pwz2u1](image/prompt.gif)

Upscaling   
Reply `u1` `u2` `u3` `u4` 

![upscale](image/upscale.gif)

Variations  
Reply  `v1` `v2` `v3` `v4`
![variation](image/variation.gif)

## Example
To run the included example, you must have [Node.js](https://nodejs.org/en) installed. Then, run the following commands in the root directory of this project:


1. clone the repository
```
git clone
```
2. install dependencies
```
npm install
```
3. set the environment variables  
   [How to get your Discord SALAI_TOKEN:](https://www.androidauthority.com/get-discord-token-3149920/)  
   [How to create a Discord bot and add it to your server:](https://www.xda-developers.com/how-to-create-discord-bot/)
```
export SERVER_ID="108250087147832934"
export CHANNEL_ID="109489299228171884"
export SALAI_TOKEN="your-salai-token"
export SALAI_DAVINCI_TOKENTOKEN="Token of Discord bot"
```
4. run the example
```
npm run dev
```

## Install
```
yarn add midjourney-discord
```
or
```
npm install midjourney-discord
```

## Usage
### Docker
Из корневой директории необходимо запустить команду ниже, при этом убедиться, что в этой корневой директории содержится файл .env с описанными выше в README переменными окружения:

```bash
docker build -t midjourney-discord-bot .; docker run -d --env-file .env midjourney-discord-bot
```



### NodeJS
```js
import { MidjourneyBot } from 'midjourney-discord'
const client = new Midjourney({
    ServerId: <string>process.env.SERVER_ID,
    ChannelId: <string>process.env.CHANNEL_ID,
    SalaiToken: <string>process.env.SALAI_TOKEN,
    Debug: true,
  })
await client.start()
```

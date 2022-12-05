# About Telegraf
In this Page we will be talking about Telegraf bot framework and Creating and Running Your Bot

### What is Telegraf?
Telegraf Js Is A Modern Bot Framework Created For Making Nodejs Bots. It is easy to use because of no complexity in code, you can create bot in simple line of code and host it on you server as well as on your terminal ( if you are using an ide like vs code etc )

### Importing Telegraf and Quick Start
Run this command in your terminal :

Using NPM
```
npm i telegraf
```
Or By Using YARN

```
yarn add telegraf
```
Or By Using PNPM
```
pnpm add telegraf
```

<h4>Importing Telegraf in Your Code</h4>

> **Note**<br>
> If You have not downloaded telegraf in the directory where the code is then you will get MODULE_NOT_FOUND error.
```javascript
const { Telegraf } = require('telegraf');
```

### Connecting Telegraf to Bot API
You need a bot token which you can get from <a href='https://telegram.me/botfather'>@BotFather</a>

> **Note**<br>
> Telegraf is a Class. Which is Imported from telegraf library


```javascript
const { Telegraf } = require('telegraf');

const bot = new Telegraf("YOUR_BOT_TOKEN");
```

### Creating Simple Bot
Create bot.js (it can be anything just add .js to last)

<b>Code Structure</b><br>
```
.
├── bot.js
├── node_modules/
├── package.json
├── package-lock.json
```
Here is a simple hello bot given. We will discuss about this code parts further
```javascript
const { Telegraf } = require("telegraf");
const bot = new Telegraf(""); // <-- put your token between the ""

// Handle Bot Start
bot.start((ctx) => ctx.reply("Bot Started!"));

// Hanndle Message
bot.on("message", (ctx) => ctx.reply("Hello World!"));

// Launch the bot.
bot.launch();
```

### Running Your Bot

Run your code in devlopment
```
node bot.js
```
Run your code while devlopment (use nodemon)
Nodemon will restart you bot when you save the changes in the file which will not require you to restart bot again and agin with node bot.js
```
nodemon bot.js
```

Run your code in production (server)
> **Note**<br>
> Install pm2 for first time in the server
```
npm install pm2 -g
pm2 start bot.js
```

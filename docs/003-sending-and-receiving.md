# Sending and Receiving Messages

When you start the bot with <code>/start</code> then Telegraf can add listners to trigger or do some action.

If you send hii then you can listen it and reply Hii.

<b> Lets Look How To Do </b>
<b> Commonly Used Listners </b>
<ol>
  <li><a href="https://telegraf.js.org/classes/Telegraf-1.html#on">bot.on("message")</a>
    <li><a href="https://telegraf.js.org/classes/Telegraf-1.html#on">bot.action("action")</a> <code>Used for InlineQueries</code>
    <li><a href="https://telegraf.js.org/classes/Telegraf-1.html#hears">bot.hears("hii")</a>
      <li><a href="https://telegraf.js.org/classes/Telegraf-1.html#command">bot.command("hii")</a>
        <li><a href="https://telegraf.js.org/classes/Telegraf-1.html#on">bot.on("message")</a>
</ol>

You can see more methods at [Telegraf.Telegraf](https://telegraf.js.org/classes/Telegraf-1.html)

### Receiving & Sending Message on Listner with Context Method
```javascript
const handle = async (ctx)=>{
ctx.replyWithMarkdown("*Hii*"); // Sends Hii (for markdown see 004.page)
}
bot.hears("hii",handle); // If the incoming message is hii
// or
bot.hears("hii,async (ctx)=>{
ctx.replyWithMarkdown("*Hii*"); // Sends Hii (for markdown see 004.page)
});
```
**Ctx full form is Context.It contains the message related data and methods.(for more refer 005)**
### Send Message From Telegram API
You can also use the api method given by [Telegram](https://core.telegram.org/bots/api)
You can do all methods given in Telegram by [bot.telegram](https://core.telegram.org/bots/api)
```javascript
const bot = new Telegraf("TOKEN");
bot.telegram.sendMessage(chatid,text,extraOptions={})
```
### Replying to a message
```javascript
bot.hears('reply',ctx=>{// use async when you need to await for something
// ctx.message contains all thing of the message sent !
ctx.replyWithMarkdown("*Replied*",{reply_to_message_id:ctx.message.message_id});
})
```
### Force Reply
> **Note**
> This can be useful if your bot is running in privacy mode in group chats.
When you send a message, you can make the user’s Telegram client automatically specify the message as reply. That means that the user will reply to your bot’s message automatically (unless they remove the reply manually). As a result, your bot will receive the user’s message even when running in privacy mode in group chats.
You can force a reply like this:
```javascript
bot.help(async (ctx) => {
  await ctx.reply("Hi! I can only read messages that explicitly reply to me!", {
    // Make Telegram clients automatically show a reply interface to the user.
    reply_markup: { force_reply: true },
  });
});
```

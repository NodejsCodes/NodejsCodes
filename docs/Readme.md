
<h3>Here are the docs in this folder. Navigate through them and learn !</h3>
Example Bots 🤖 : <a href="https://github.com/NodejsCodes/NodejsCodes/example">Here</a>

[![Stars](https://img.shields.io/github/stars/NodejsCodes/NodejsCodes?style=flat-square&color=yellow)](https://github.com/NodejsCodes/NodejsCodes/stargazers)
<br>
# Introduction to Bots
Bots are small applications that run entirely within the Telegram app. Users interact with bots through flexible interfaces that can support any kind of task or service.

### How do Bots Work?
Telegram bots are special accounts that do not need a phone number to set up.
Bots are connected to their owner’s server, which processes inputs and requests from users.
Telegram’s intermediary server handles all encryption and communication with the Telegram API.
Developers communicate with this server via an easy HTTPS-interface with a simplified version of the Telegram API – known as the [Bot API](https://core.telegram.org/bots/api).

<h4>How Are Bots Different from Users?</h4>
Bots are able to process inputs and requests in ways that user accounts can’t, but there are several differences between a bot and a normal user.

<ul>
  <li>Bots don’t have ‘last seen’ or online statuses – instead they show a ‘bot’ label in the chat.
  <li>Bots have limited cloud storage – older messages may be removed by the server shortly after they have been processed.
  <li>Bots can't start conversations with users. A user must either add them to a group or send them a message first. People can search for your bot’s username or start a chat via its unique t.me/bot_username link.
  <li>By default, bots added to groups only see relevant messages in the chat (see <a href="https://core.telegram.org/bots/features#privacy-mode">Privacy Mode</a>).
  <li>Bots never eat, sleep or complain (unless expressly programmed otherwise).
</ul>


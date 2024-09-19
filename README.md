![](https://discord.com/assets/9e8e58d39a70852721ae2a0db31ff892.svg)

## Discord Library Opensource

an open-source library that enables real-time communication with the Discord API using WebSockets. Perfect for developers creating Discord bots, this library simplifies event management and allows for seamless updates and customizations to your projects.

### Usage

```js
// Get started by editing `bot/client.js`

const { Client } = require('../src/package');
const bot = new Client(process.env['DISCORD_BOT_TOKEN'], {
    intents: [
      'GUILDS'
    ]
})

bot.on('ready', async() => {
    console.log(`${bot.user.username}'s Online.`)
})

bot.on('messageCreate', Message => {
    if(Message.content === 'opensource') {
        Message.reply({ content: 'An opensource project is good 😁.' })
    }
})

bot.connect();
```

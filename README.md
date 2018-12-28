# Discord Webhooks
![version](https://img.shields.io/npm/v/webhook-discord.svg "Version")
![npm](https://img.shields.io/npm/dt/webhook-discord.svg "Total Downloads")
A simple Javascript file for nicely formatting Discord webhooks

# Usage
It's simple

To initialise:
```js
const webhook = require("webhook-discord")

const Hook = new webhook.Webhook("WEBHOOK URL")
```

## Presets

To send an info message:
```js
Hook.info("kurt cobain","Info")
```

To send a warning message:
```js
Hook.warn("kurt cobain", "olha o rock")
```

To send an error message:
```js
Hook.err("kurt cobain","Error")
```

To send a success message:
```js
Hook.success("kurt cobain","sucesso broll")
```

## Custom messages

To send custom messages, you should make use of the MessageBuilder.

```js
const webhook = require("webhook-discord");

const Hook = new webhook.Webhook("WEBHOOK URL");

const msg = new webhook.MessageBuilder()
                .setName("kurtcobain")
                .setColor("#aabbcc")
                .setText("rock sucesso broll!")
                .addField("This", "is")
                .addField("my", "rock!")
                .setImage("Image url")
                .setTime();

Hook.send(msg);
```

# Installation
Either use npm:
```
npm install webhook-discord
```
Or clone from source:
```
git clone https://github.com/JoeBanks13/webhook-discord.git
```

# License

MIT



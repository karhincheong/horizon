# Horizon Nightly
🎑 Horizon Nightly is the dev branch of Horizon, the official Discord bot for the International Junior Honour Society community server. It is a work in progress, and is often updated with new features and bug fixes.

## Getting started with local development
To get started with developing the bot locally, you need to clone this repository via

```bash
git clone https://github.com/cytronicoder/horizon.git
```
Then, you need to switch to the `dev` branch:

```bash
cd horizon
git checkout dev
```

You can then start developing the bot by installing the dependencies via

```bash
yarn install
```

Before you can start the bot, you will need to create a Discord bot token. You can do this by going to the [Discord Developer Portal](https://discordapp.com/developers/applications/me) and creating a new bot. Then, create an `.env` file and add the following lines to it:

```bash
TOKEN=<your bot token>
```

Additionally, you will need the client and guild ID in the `.env` file:

```bash
CLIENT_ID=<your client ID>
GUILD_ID=<your guild ID>
```

You will also need a `config.json` file in the `root` directory. This file contains the bot's configuration:

```json
{
    "cooldown_duration": 10000
}
```

Note that `config.json` is not required. If it is not present, the default cooldown duration will be used. The default cooldown duration is 10 seconds. Additionally, this is still an experimental feature, and new values may be added in the future.

Finally, you can start the bot by running

```bash
node deploy-commands.js && node .
```
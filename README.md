# MediBot Telegram Bot

A MediBot seeks to provide instant, personalized healthcare assistance and information through natural language conversation, improving accessibility and convenience for users seeking medical knowledge and support anytime, anywhere via [Telegram bot](https://core.telegram.org/bots/api)

## Screenshots

### Demo

![demo](https://github.com/Sakal05/medibot/blob/7f5c7694704276ce8abe9fb02109c1fde7cee1cb/adsjl341klkdklfslk23cvb.png)

## Features

- [x] Support markdown in answers
- [x] Reset conversation with the `/reset` command
- [x] Typing indicator while generating a response
- [x] Automatic conversation summary to avoid excessive token usage
- [x] Track token usage per user
- [x] Get personal token usage statistics via the `/stats` command
- [x] Vision support

## Prerequisites

- Python 3.9+
- A [Telegram bot](https://core.telegram.org/bots#6-botfather) and its token (see [tutorial](https://core.telegram.org/bots/tutorial#obtain-your-bot-token))
- An [OpenAI](https://openai.com) account (see [configuration](#configuration) section)

## Getting started

### Configuration

Customize the configuration by copying `.env.example` and renaming it to `.env`, then editing the required parameters as desired:

| Parameter                   | Description                                                                                                                                                                                                                   |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `OPENAI_API_KEY`            | Your OpenAI API key, you can get it from [here](https://platform.openai.com/account/api-keys)                                                                                                                                 |
| `OPENAI_MODEL`              | Your OpenAI Model. Ex: gpt-4o                                                                                                                                                                                                 |
| `ASSISTANT_PROMPT`          | System Prompt to help personalized the bot experience                                                                                                                                                                         |
| `MAX_TOKENS`                | Maximum Token for openAI usage.                                                                                                                                                                                               |
| `BOT_LANGUAGE`              | Bot Language. Default will be set to en (English language)                                                                                                                                                                    |
| `TELEGRAM_BOT_TOKEN`        | Your Telegram bot's token, obtained using [BotFather](http://t.me/botfather) (see [tutorial](https://core.telegram.org/bots/tutorial#obtain-your-bot-token))                                                                  |
| `ADMIN_USER_IDS`            | Telegram user IDs of admins. These users have access to special admin commands, information and no budget restrictions. Admin IDs don't have to be added to `ALLOWED_TELEGRAM_USER_IDS`. **Note**: by default, no admin (`-`) |
| `ALLOWED_TELEGRAM_USER_IDS` | A comma-separated list of Telegram user IDs that are allowed to interact with the bot (use [getidsbot](https://t.me/getidsbot) to find your user ID). **Note**: by default, _everyone_ is allowed (`*`)                       |

### Installing

Clone the repository and navigate to the project directory:

```shell
git clone https://github.com/Sakal05/medibot.git
cd medibot
```

#### From Source

1. Create a virtual environment:

```shell
python -m venv venv
```

2. Activate the virtual environment:

```shell
# For Linux or macOS:
source venv/bin/activate

# For Windows:
venv\Scripts\activate
```

3. Install the dependencies using `requirements.txt` file:

```shell
pip install -r requirements.txt
```

4. Use the following command to start the bot:

```
python bot/main.py
```

## Credits

- [ChatGPT](https://chat.openai.com/chat) from [OpenAI](https://openai.com)
- [python-telegram-bot](https://python-telegram-bot.org)
- [jiaaro/pydub](https://github.com/jiaaro/pydub)
